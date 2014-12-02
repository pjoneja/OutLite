  var sheet = SpreadsheetApp.getActiveSheet();

// Triggers have been set up. There should be two 1) on Submit 2) on Change. Check resources ---> current project triggers.

function getCommand() {
  var spreadsheet = sheet.getDataRange();
  var entries = spreadsheet.getValues(); //returns row-by-row array of all entries
  var LastRow = entries[spreadsheet.getLastRow() - 1]; //returns array of last row
  var LastCommand = LastRow[1];
 
  Logger.log(LastCommand);
  
  //MailApp.sendEmail("teamoutlite@gmail.com", "Response", LastCommand); 

  
  var payload = 
   {
     "params" : LastCommand
   };

   var options =
   {
     "method" : "post",
     "payload" : payload
   };

  
  
 var response = UrlFetchApp.fetch("https://api.spark.io/v1/devices/53ff70066667574828502367/led?access_token=8a1e8465290bc1370450715e1535fba27d3022f5", options);
  Logger.log(response);

  

}

