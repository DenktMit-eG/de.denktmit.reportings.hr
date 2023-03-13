# de.denktmit.reportings.hr

This project

# Local setup on macOS

1. Download the newest version of Pentaho from https://sourceforge.net/projects/pentaho/files/latest/download
2. Move the unzipped folder called something like "data integration" to your Applications directory

## Run the application using the command line

1. Open a terminal and navigate to `/Applications/data-integration/Data\ Integration.app\Contents\MacOS`
2. In this folder you have to run the  `./JavaApplicationStub`
3. Now the application should open
4. Now the software starts, so you can add the 3 tickets from the [java folder](src/main/java) to the software (open
   file option in the software)

## Run the application from Finder

1. Open the data-integration folder right-click the Data Integration symbol
2. Click "Show Package Contents" (Packetinhalte anzeigen)
3. Navigate to `Contents/MacOS/JavaApplicationStub` execute the JavaApplicationStub exec
4. Now the software starts, so you can add the 3 tickets from the [java folder](src/main/java) to the software (open
   file option in the software)

## Ticket explanation

Ticket 1: Checks, that working hours are <= 20 per week in lecture period

Ticket 2: Checks, that the working time of 8 hours per day hat not been exceeded

Ticket 3: Checks, that working time is not over 5 hours without a break of at least 15 minutes

## Use the tickets

Ticket 1:

- Add your working times in correct csv format into the "Read Arbeitszeiten" text file input
- Add the [Vorlesungszeiten.csv](src/main/resources/Vorlesungszeiten.csv) to the "Read Vorlesungszeiträume" text file
  input (note that only semesters from 2019-2024 are included)
- Run the ticket
- Look into "Preview data" tab to see your results, if your times are correct or should be revised

Ticket 2:
- Add your working times in correct csv format into the "Read Arbeitszeiten" text file input
- Run the ticket
- Look into "Preview data" tab to see your results, if your times are correct or should be revised

Ticket 3:
- Add your working times in correct csv format into the "Read Arbeitszeiten" text file input
- Run the ticket
- Look into "Preview data" tab to see your results, if your times are correct or should be revised

## Issue handling

If you have issues trying to run the application, use following steps:

1. Be sure, that you are using java version 8 (`java -version`)
2. Increase the max memory limit with the command
   `export PENTAHO_DI_JAVA_OPTIONS="-Xmx2g -XX:MaxPermSize=256m"`
3. Call the commands with sudo
4. Execute the `spoon.sh` file in the data-integration folder to execute the application
5. View problem: Change your Mac appearance to light mode to avoid view problems and restart the application