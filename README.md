seneca-mvp
==========

How to build a Minimim Viable Product with Seneca

## Setup

```bash
cp options.example.js options.mine.js
npm install
cd public
bower install
```

## Requirements

InfluxDB must be installed.
Please see http://influxdb.com/docs/v0.6/introduction/installation.html for more information

Once InfluxDB is installed, the msgstats options must be updated in options.mine.js:

```JavaScript
msgstats: {
    pin:{},
    influxOpts:{
      host:'localhost',
      port: 8086,
      username:'root',
      password:'root',
      database:'test_db',
      seriesName:'mvp_test'
    }
  },
```

Edit options.mine.js as needed.


## Run

```bash
node mvp-app.js
```

And open [localhost:3333](http://localhost:3333)


