# Example of parameterized query in Python using SQLite
import sqlite3

conn = sqlite3.connect('example.db')
c = conn.cursor()

# Safe method to query data
user_id = 'example_user_id'
c.execute("SELECT * FROM users WHERE id = ?", (user_id,))
