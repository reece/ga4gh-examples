ga4gh-examples: sample code demonstrating the GA4GH API
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

This directory contains scripts and jupyter notebooks that demonstrate
using the GA4GH API.

Do something roughly like this: ::

  mkvirtualenv ga4gh

  git clone git@github.com:ga4gh/compliance.git
  git clone git@github.com:ga4gh/server.git

  cd server
  pip install -r requirements.txt
  python setup.py develop
  python scripts/prepare_compliance_data.py -i ../compliance/test-data -o ga4gh-example-data
  python server_dev.py &

Connect to http://127.0.0.1:8000/ (e.g., in a browser) to ensure that
the dev server is functional.

Then, in another directory: ::

  workon ga4gh
  git clone git@github.com:reece/ga4gh-examples.git
  pip install jupyter plotly
  jupyter notebook --notebook-dir=nb
  
