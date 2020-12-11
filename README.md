<h4 align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/PowerShell_Core_6.0_icon.png/80px-PowerShell_Core_6.0_icon.png"></img>PowerShell script for exporting IIS statistics by user to the DB
</h4>

- ## ***Introduction***
  With that powershell script you can export statistics from your IIS server any site logs to the SQL databases.
  But, first you need to install ***Microsoft LogParser*** on the server.

- ## ***Getting started***
  1. **Microsoft LogParser**, [`download`](https://www.microsoft.com/en-us/download/details.aspx?id=24659) and install
  2. **Download** script
  3. **Open** script for editing and set variables values for your configuration
      ```powershell
      $dbserver = "..." # DB server,port
      $database = "..." # DB name
      $environment = "PROD" # Environment name
      $start = [DateTime]::Now
      $startFormatted = $start.ToString("yyyyMMddHHmmss")
      $source = "e:\IISLogsToDB" # IIS logs path
      $logpath = "$source\$name\$name-log-$startFormatted.txt" # Script log file path
      $logParser = "${env:ProgramFiles(x86)}\Log Parser 2.2\LogParser.exe" # LogParser install dir & exec file
      ```
  4. **Create** the database and take access rights
  5. **Run** and **enjoy**

- ## ***License***
  GPLv3
