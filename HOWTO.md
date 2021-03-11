# HOWTO.md

## Fragen

- Braucht man https://github.com/ard-data/2020-rki-archive ?

- wo ist setup.sh ?

## Anleitung zur Installation der Abhängigkeiten unter macOS 10.15
```
brew install google-cloud-sdk

virtualenv -p pythone venv3
source venv3/bin/activate

pip install git+https://github.com/h2oai/datatable
pip install pytz
pip install ndjson
pip install python-dateutil
pip install psutil

# for rki-analyze.py
pip install numpy
pip install matplotlib

# for scratch.py
pip install flask
pip install dash
pip install pandas

mkdir ard-data
mkdir archive_ard
mkdir archive_v2

# for rki-analyze.py und scratch.py
mkdir dumps
mkdir archive
mkdir archive_csv

export CORONA=`pwd`
./update.sh
./rki-analyze.py
./scratch.py
```
