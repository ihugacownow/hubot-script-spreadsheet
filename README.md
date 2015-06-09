hubot-script-spreadsheet
========================

hubot (query) interface to google spreadsheet (*with* authentication)


### Example

Simple:

    hubot> hubot spreadsheet myspreadsheet
    Product Id  Description            Price, USD
    ----------  ---------------------  ----------
    123123      Something awesome         1000.00
    245452      Very interesting book       11.45
    232323      Yet another product        555.55
    
    source: https://docs.google.com/spreadsheet/ccc?key=sdfsdfsdfsdf..

regex searchquery:
    
    hubot> hubot spreadsheet myspreadsheet awesome|book
    Product Id  Description            Price, USD
    ----------  ---------------------  ----------
    123123      Something awesome         1000.00
    245452      Very interesting book       11.45
    
    source: https://docs.google.com/spreadsheet/ccc?key=sdfsdfsdfsdf..

### Why

A spreadsheet is an awesome userinterface+database in one view.
Its easy for everybody to use, so referencing/querying spreadsheets can be very handy during text teamcommunication.

###  Configuration:

    client_id: 
    client_secret:
    refresh_token:

### Commands:

add a spreadsheet first: 

    hubot phones save myspreadsheet spreadsheetname|sheet1|2|http://....

then:

     hubot phones                                 # shows usage + available sheets

     hubot phones myspreadsheet                   # displays sheet

     hubot phones myspreadsheet <regex>           # displays sheet  entries which match "foo"
     
     hubot phones del myspreadsheet               # delete
