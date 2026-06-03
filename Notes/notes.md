## Backend Node.js (Express)
### Mise en place :
- serveur Express
- routes HTTP
- CORS pour autoriser le frontend
- JSON parsing

```JS
const	express = require("express");
const	app = express();

app.use(cors());
app.use(express.json());
```

## Base de données (MariaDB)
### Création :
- de base ```travel_db```
- de tables :
	- ```voyages```
	- ```users```
	- ```reservations```

## Connexion entre Node.js et DB
```JS
const	mysql = require("mysql2");

const	db = mysql.createConnection({
	host: process.env.DB_HOST,
	user: process.env.DB_USER,
	password: process.env.DB_PASSWORD,
	database: process.env.DB_NAME
});

module.exports = db;
```

## API REST
```JS
app.get("/voyages", (req, res) => {
	const sql = "SELECT * FROM voyages";

	db.query(sql, (err, result) => {
		if (err) {
			console.log(err);
			return (res.status(500).json(err));
		}
		res.json(result);
	});
});
```

## Frontend + fetch()
- Appelle le API
- Récupère des voyages
- Afficher les voyages dynamiquement