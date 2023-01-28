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

### Hiding Django Secrets

```env
**Inside of your .env file**
SECRET_KEY=qolwvjicds5p53gvod1pyrz*%2uykjw&a^&c4moab!w=&16ou7 # <- Example key, SECRET_KEY=yoursecretkey
```

```python
import os
import dotenv # <- New

# Add .env variables anywhere before SECRET_KEY
dotenv_file = os.path.join(BASE_DIR, ".env")
if os.path.isfile(dotenv_file):
    dotenv.load_dotenv(dotenv_file)

# UPDATE secret key
SECRET_KEY = os.environ['SECRET_KEY'] # Instead of your actual secret key
```