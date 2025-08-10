### Database Initialization Instructions

To create the database tables without encountering the `RuntimeError: Working outside of application context`, follow this step in a Python shell:

```
>>> from server import app, db
>>> with app.app_context():
...     db.create_all()
```