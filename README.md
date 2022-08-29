# xbrl-parser

Parses XBRL files (DEI, GAAP, IFRS).

## Install
`git clone https://github.com/criskurtin/xbrl-parser.git`

`cd xbrl-parser`

`pip install -e .`

## Usage 
```py
from xbrl_parser import XBRL

raw_xbrl_string = (
  '<?xml version="1.0" encoding="iso-8859-1"?>'
  '<xbrli:xbrl xmlns:link="http://www.xbrl.org/2003/linkbase" xmlns:xlink="http://www.w3.org/1999/xlink"'
  ' xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xbrli="http://www.xbrl.org/2003/instance"'
  ' xmlns:ISO4217="http://www.xbrl.org/2003/iso4217" xmlns:xbrldi="http://xbrl.org/2006/xbrldi"'
  ' xmlns:ifrs-full="http://xbrl.ifrs.org/taxonomy/2017-03-09/ifrs-full"'
  ' xmlns:ifrs-mc="http://xbrl.ifrs.org/taxonomy/2017-03-09/ifrs-mc">'
  '</xbrli:xbrl>'
)

xbrl = XBRL(raw_xbrl_string, "ifrs")
xbrl.parse()

financials = xbrl.financials
```
