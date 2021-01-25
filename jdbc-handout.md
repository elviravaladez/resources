# JDBC

## Classes / Objects

- `DriverManager`: a class that manages the class we use to connect to the
  database
- `Connection`: an instance of this class represents a connection to MySQL
- `Statement`: an object created from the the connection object, represents a
  single SQL query (i.e. statement)
- `ResultSet`: a representation of query results
- `SQLException`: indicates an error occured while talking to the database
  (connection, or SQL syntax error)

## How to Use It

1. Connect to the database; obtain a connection object

    - register a driver (`DriverManager.registerDriver`)
    - `DriverManager.getConnection` and pass along credentials
    - happens once (constructor or factory)

1. Create a statement object

    - `connection.createStatement()`

1. Execute the statement with our sql based on it's type

    - `.execute` for `CREATE ...` or `DELETE`
    - `.executeUpdate` for `INSERT`, `UPDATE` statements, use
      `Statement.RETURN_GENERATED_KEYS` to obtain generated ids
    - `.executeQuery` for `SELECTS`

1. Work with the results of the query; the resultset object

    - `.next` method to move through the results

## Database Credentials

It's not a good idea to have usernames and passwords in our code base, so we'll
create a class that is not tracked w/ version control to handle this, `Config`.
It has only properties and getters for a url, username, and password.
