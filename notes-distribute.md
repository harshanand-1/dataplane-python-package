### Steps to distribute

1. Update toml with latest version

2. In repo root directory build package
```shell
python3 -m pip install --upgrade build
rm -rf ./dist && python3 -m build
```

3. Remove previous version and distribute new package
```shell
python3 -m pip install --upgrade twine
python3 -m twine upload dist/*
```

4. Testing impport times - lazy loading:
```shell
pip install dataplane==0.0.12
python -v import_try.py
```