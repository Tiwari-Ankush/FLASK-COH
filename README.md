# FLASK-COH

for activating venv
.\venv\Scripts\activate.ps1

for setting up database;
pip install flask-sqlalchemy

sqlalchemy-
    Flask-SQLAlchemy is an extension for the Flask web framework that simplifies the integration of SQLAlchemy, a popular Object-Relational Mapping (ORM) library, into Flask applications. SQLAlchemy provides a powerful and flexible way to interact with databases using Python code, and Flask-SQLAlchemy enhances this by providing a convenient way to use SQLAlchemy within Flask projects.


Key features of Flask-SQLAlchemy include:
>>>>>
Database Models: Define database tables as Python classes, and SQLAlchemy will automatically generate SQL statements to create and manipulate the tables.

Querying: Perform database queries using SQLAlchemy's query API, allowing you to use Python methods and expressions instead of raw SQL.

Sessions and Transactions: Flask-SQLAlchemy handles the lifecycle of database sessions and transactions within the context of Flask's request-response cycle. This helps manage the database connection efficiently and avoids common issues like connection leaks.

Migrations: Flask-SQLAlchemy can work in tandem with migration libraries like Alembic to help manage database schema changes over time.



    SQLALCHEMY_DATABASE_URI >>
    https://flask-sqlalchemy.palletsprojects.com/en/2.x/config/
    sqlite:////tmp/test.db


creating a database>>
   python in cmd (in currently activated virtual venv)
       >> then

    >>>from app import db
    >>>db.create_all() 
    if above two lines are not working then, use below lines>>

    >>> from app import app, db
    >>> with app.app_context():
    ...    db.create_all() 
    "it will create a database in instance directory"
    
    remember>>
        In this format, you're entering the with block using the ... continuation prompt, and you can press Enter to continue entering the code.

        Remember to replace 'app' with the actual name of your Flask application instance, and ensure that you have imported the necessary modules (app and db) correctly in your code.