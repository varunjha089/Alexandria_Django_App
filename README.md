# Alexandria Django App
https://training.talkpython.fm/courses/details/getting-started-with-django

### Creating virtual Environment

Create the virtual environment using the command and replace the `{environnment name}` with something reasonable
```Powershell
python -m venv {environment name}
```

Install the required dependencies
```Powershell
pip install -r requirements.txt
```

### Running with `uvicorn`

```powershell
python -m uvicorn Alexandria.asgi:application
```

To learn more about `uvicorn` click [here](https://docs.djangoproject.com/en/4.1/howto/deployment/asgi/uvicorn/)

## Testing Django

```powershell
 python manage.py test tests
 ```