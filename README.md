# RUMStream

RUMStream is a simple ruby riemann client for BMC EUEM Real User Monitor (RUM), 
formerly Coradiant TrueSight.

## Dependencies

    gem install csv
    gem install riemann-client
    gem install em-http

## Usage

RUMStream assumes you're running riemann on localhost, using default ports. Support is planned
for other hosts, ports, etc.

rumstream takes a single argument, the URL for the event stream. For example, to get all
attributes for all objects, up to 400 events/sec:

    $ ./rumstream "https://$RUMHOST/getstream?usr=$RUMUSER&pwd=$RUMPASS&objects=all&id=1&limit=400"
