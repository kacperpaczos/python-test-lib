## Konfiguracja środowiska wirtualnego

1. Stwórz nowe środowisko wirtualne:
   ```shell
   python3 -m venv venv
   ```

2. Włącz środowisko wirtualne:
   ```shell
   source venv/bin/activate
   ```

3. Zainstaluj niezbędne pakiety:
   ```shell
   pip install wheel setuptools twine pytest
   ```

## Wykonywanie testów

1. Przeprowadź testy:
   ```shell
   python setup.py pytest
   ```

## Kompilacja i instalacja

1. Skompiluj pakiet:
   ```shell
   python setup.py bdist_wheel
   ```

2. Zainstaluj pakiet z pliku wheel:
   ```shell
   pip install /dist/mypythonlib-0.1.0-py3-none-any.whl
   ```

Plik wheel znajduje się w folderze "dist". Możesz także opublikować pakiet w repozytorium PyPI i zainstalować go stamtąd.

## Jak korzystać
Możesz zainstalować pakiet lokalnie z pliku *.whl lub używając PIP.
Aby zintegrować pakiet z twoim projektem, zaimportuj go w następujący sposób:
```python
import mypythonlib
from mypythonlib import myfunctions
