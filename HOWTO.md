# install

- Braucht man https://github.com/ard-data/2020-rki-archive ?

- wo ist setup.sh ?

```
brew install google-cloud-sdk

virtualenv -p pythone venv3
source venv3/bin/activate

pip install git+https://github.com/h2oai/datatable
pip install pytz
pip install ndjson
pip install python-dateutil

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
mkdir dumps
mkdir archive
mkdir archive_csv

./update.sh
./rki-analyze.py
./scratch.py
```
