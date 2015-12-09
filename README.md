The ALCDEF 2.0 to JSON Converter is a tool for conversion astronomic data stored in ALCDEF 2.0 format to more popular and generic JSON data interchange format.

- ALCDEF format: http://minorplanetcenter.net/light_curve
- JSON format: http://json.org/
  - The keys are in lower case
  - Boolean strings from alcdef represented as booleans (lower case in JSON)
  - Strings are plain copied with commas replaced with dots and double quotes escaped
  - Doubles including the Julian Date represented as doubles
  - In the flat mode, data entries are suffixed with their index numbers
  - In the nested mode, data entries are put into arrays, where each entry is an object with subfields of data represented as key-value pairs

Flags
=====
The program currently accepts the following flags:
* --fromFile (upcoming) or --fromDir - **required**, stands for the address of the directory with input ALCDEF files
* --toFile or --toDir (upcoming) - **required**, stands for the address of an output file (created automatically if does not exist)
* --flatMode - **optional**, if not used, the nested mode is applied

Example use case
========
```
alcdef2json --fromDir C://alcdef2json/alcdef --toFile C://alcdef2json/json/alcdefs.json --flatMode
```
