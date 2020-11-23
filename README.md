# RealFinal
Real Final is a project created to manage version control and cloud storage for music creators


planned featureset --
- connect to cloud providers
    - allow users to connect to their own Google Drive or Dropbox to start, add more over time 
    - eventually have your own cloud solution for those who dont have their own -- charge for this, likely will be backed by google or aws, may consider an on prem solution to start
- create a naming convention
    - "-project<x>" meaning new version for a project file, useful to those who arent familiar with the filetypes of a particular DAW, or if you tend to save your projects in a directory mixed with export files. Also helps version your DAW project file. `Example Title: MySong-project2.xyz`
    - "-v<x>" meaning new song version for an export file (mp3, wav, aiff, etc). `Example Title: MySong-v12.wav`
    - "-v<x>-mix<n>-[description]" meaning changes have been made to the mix for version #x. This is the n'th change to the mix for this song's x'th version. `Example Title: MySong-v34-mix3`. Optionally, a short description can be provided explaining the new changes. `Example Title: MySong-v34-mix3-hihatLeftPan`
    - "-project<x>-autosave<datetimestamp>" meaning this is an autosave created while editing version x of the project file. `Example Title: MySong-project3-autosave11102020_094532` This datetimestamp means this file was created after the most recent project version, 3, at 9:45:32 am on 11/10/2020.
- settings
    - choose a max number of versions of each filetype to be stored
    - choose a total max number of files to be stored
    - choose a max amount of space to be used.
        - if max reached, replace files? or dont allow new saves? Or show a warning?
    - match current highest main version number when creating a new file of any type. In other words, if you have a file `MySong-project4.xyz` and a file `MySong-v20.mp3`, next time a project or export file are created, it will have a suffix number of 21.
    - autosave every Y seconds/minutes/hours/days(at time xx:xx) while DAW is running
        - select DAW
        - where are your temporary files stored? Populate with default for the specified daw, but allow user to change this
            - NOTE that if they are not sure, they should leave it unchanged
    - save a local copy and a copy in the cloud
        - do this every time a new file is created? When a project file is created? When an export file is created? When a mix file is created?
- UI/UX/front end
    - 