# PEPPER: Python Extension for Portable Process Execution and Redirection 


## Installing and Importing Libraries

PEPPER includes its own `pip` installation mechanism, which works the same way as a standard Python interpreter. Third-party packages can be installed using PEPPER's bundled `pip`.

To avoid interfering with the interpreter implementation and PEPPER-specific runtime changes, it is recommended to install external packages into the `build/site-packages` directory.

From the PEPPER root directory, install packages using:

```bash
./python.exe -m pip install --target build/site-packages <package-name>
```

or to upgrade all dependencies: 

```bash
./python.exe -m pip install --target build/site-packages --upgrade <package>
```


For example:

```bash
./python.exe -m pip install --target build/site-packages numpy
```

After installing packages, add the ```build/site-packages``` directory to ```PYTHONPATH`` when running PEPPER as shown below.

Running a Python file:
```bash
PYTHONPATH=build/site-packages ./python.exe <file_name>.py
```

Starting the REPL:

```bash
PYTHONPATH=build/site-packages ./python.exe
```

Then within the script or reply, packages can be imported normally, for example:

```python
import numpy
```
