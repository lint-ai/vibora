## Getting Started

Make sure you are using `Python 3.6+` because Vibora takes
advantage of some new Python features.

1) Install Vibora: `pip install vibora`

> It's highly recommended to install vibora inside a virtualenv.

> In case you have trouble with Vibora dependencies: `pip install vibora[pure]`



2) Create a file called `anything.py` with the following code:

```py
from vibora import Vibora, JsonResponse

app = Vibora()


@app.route('/')
async def home():
    return JsonResponse({'hello': 'world'})

if __name__ == '__main__':
    app.run(host="0.0.0.0", port=8000)
```

3) Run the server: `python3 anything.py`


4) Open your browser at `http://127.0.0.1:8000`


### Creating a project

The previous exercise was just to show off how easily is
to spin up a server.

The recommended way to start a new project is by letting vibora do it for you.
Vibora is also a command-line tool, try it out in your command-line: `vibora new project_name`