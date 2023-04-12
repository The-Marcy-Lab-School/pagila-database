# Pagila (Marcy Lab)


Pagila is a "DVD Rental Store" type example database for PostgreSQL. It provides sample schema and data for use in instructional materials, articles, and demonstrations, and is specifically designed to show case features within PostgreSQL. 



## INSTALLATION STEPS

You must [set up Postgres](https://github.com/The-Marcy-Lab-School/postgres-setup) on your local machine if you havn't done so already.

To install the pagila database, clone down this repo. Using your terminal, `cd` into this project. To ensure you are in the right directory, run `ls` and make sure you see the files `pagila-data.sql`, `pagila-insert-data.sql`, and `pagila-schema.sql`.

Once you are in the correct directory, copy and paste these four lines and run them in your terminal. 

##### For Mac Users
```
psql -c "DROP DATABASE pagila;"
psql -c "CREATE DATABASE pagila;"
psql -d pagila -f pagila-schema.sql
psql -d pagila -f pagila-data.sql
```

##### For Windows Users
```
sudo -u postgres psql -c "DROP DATABASE pagila;"
sudo -u postgres psql -c "CREATE DATABASE pagila;"
sudo -u postgres psql -d pagila -f pagila-schema.sql
sudo -u postgres psql -d pagila -f pagila-data.sql
```


The pagila-data.sql file and the pagila-insert-data.sql both contain the same
data, the former using COPY commands, the latter using INSERT commands, so you 
only need to install one of them. Both formats are provided for those who have
trouble using one version or another.

You can now run SQL queries in `psql` or you can now open your `pagila` database via your TablePlus and run SQL queries. 
