hubot-script-spreadsheet
========================

hubot (query) interface to google spreadsheet (*with* authentication)

<img alt="" src="https://github.com/coderofsalvation/hubot-script-spreadsheet/blob/master/.res/cat.gif"/>

A cat gif, no project can live without it!

### Example

    hubot> hubot spreadsheet show myspreadsheet
    Product Id  Description            Price, USD
    ----------  ---------------------  ----------
    123123      Something awesome         1000.00
    245452      Very interesting book       11.45
    232323      Yet another product        555.55
    
    source: https://docs.google.com/spreadsheet/ccc?key=sdfsdfsdfsdf..

### Why

A spreadsheet is an awesome userinterface+database in one view.
Its easy for everybody to use, so referencing/querying spreadsheets can be very handy during text teamcommunication.

###  Configuration:

    GOOGLE_SPREADSHEET_LOGIN="you@gmail.com"
    GOOGLE_SPREADSHEET_PASSWD="somepassword"

### Commands:

add a spreadsheet first: 

    hubot spreadsheet save myspreadsheet spreadsheetname|sheet1|2|http://....

then:

     hubot spreadsheet                                 # shows usage + available sheets
     hubot spreadsheet show myspreadsheet              # displays sheet
     hubot spreadsheet show myspreadsheet foo          # displays sheet entries which match "foo"
     hubot spreadsheet del myspreadsheet               # delete
