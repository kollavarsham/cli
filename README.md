# kollavarsham-cli [![npm](https://img.shields.io/npm/v/kollavarsham-cli.svg)](https://www.npmjs.com/package/kollavarsham-cli)

The kollavarsham CLI app - convert Gregorian date to Kollavarsham date and vice versa

## Getting Started
Install the module with: `npm install -g kollavarsham-cli`

## Usage

```plain
$ npm install -g kollavarsham-cli

$ kollavarsham --help

              kollavarsham (v0.4.0)
   Based on the Pancanga Perl library by M. YANO and M. FUSHIMI
   http://www.cc.kyoto-su.ac.jp/~yanom/pancanga/message314.html
   ------------------------------------------------------------

kollavarsham [options] [arguments]

options
-------
    -h --help
       Show this help text
    -v --version
       Display the current app version
    -m --mode [0|1]
       0 - Gregorian Calendar Date to Malayalam Calendar Date
       1 - Malayalam Calendar Date to Gregorian Calendar Date
    -c --system ['InPancasiddhantika'|'SuryaSiddhanta']
       Sets system to use as 'InPancasiddhantika' or 'SuryaSiddhanta'. Default is 'SuryaSiddhanta'.
       InPancasiddhantika - Calculations are based on older constants in Pancasiddhantika (AD 505).
       SuryaSiddhanta     - Calculations are based on SuryaSiddhanta (AD 1000ca).
       (Any value other than 'InPancasiddhantika' or 'SuryaSiddhanta' will be discarded)
    -a --showlatitudes
       Display a map of India with the latitudes
    -o --showlongitudes
       Display a map of India with the longitudes
    -t --latitude [number]
       Set the latitude of the location to be used as the basis of the conversions. Should be between -90 and +90
       default: 23.2 (Use option --showlatitudes for help)
    -g --longitude [number]
       Set the longitude of the location to be used as the basis of the conversions. Should be between -180 and +180
       default: 75.8 (Use option --showlongitudes for help)
    -o --output-format ['list'|'verbose']
       list    - for dates on both sides of the entered
       verbose - for detailed view of the output date
       (Any value other than 'list' or 'verbose' will be discarded)
arguments
---------
    Date
        Input date to be converted. Use the following date formats.
        Date format: DD:MM:YYYY when mode is 0 (Gregorian to Malayalam)
        Date format: DD:MM:YYYY when mode is 1 (Malayalam to Gregorian) where
        DD is the day of the Malayalam month
        MM 01 for Chingam, 02 for Kanni, 03 for Thulam, 04 for Vrischikam, 05 for Dhanu, 06 for Makaram,
           07 for Kumbham, 08 for Meenam, 09 for Medam, 10 for Edavam, 11 for Mithunam, 12 for Karkidakam
        YYYY is the Malayalam Year (Kollavarsham)
Examples
--------
    To convert Modern Date to Kollavarsham Date for Location (100 deg east, 90 deg north
    using 'InPancasiddhantika' system and list output:
        kollavarsham -s 'InPancasiddhantika' -t 90 -g 100 -m 0 -o list 23:08:2008
    To convert Modern Date to with default settings (Location: Ujjain and System: SuryaSiddhanta)
        kollavarsham 04:04:2011

```

## Examples
To convert Modern Date to Kollavarsham Date for Location (100 deg east, 90 deg north using 'InPancasiddhantika' system and list output:

```
kollavarsham -s 'InPancasiddhantika' -t 90 -g 100 -m 0 -o list 23:08:2008
```

To convert Modern Date to with default settings (Location: Ujjain):

```
kollavarsham 04:04:2011
```

## Release History
Check out the history at [GitHub Releases](https://github.com/kollavarsham/cli/releases)

## License
Copyright (c) 2014-2016 The Kollavarsham Team. Licensed under the MIT license.
