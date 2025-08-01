# Wopw
Wopw - is a python3 library, making coding faster and easier. Supports all popular OS's: macOS, Windows, Linux. Supports VSCode comments

# Classes and it modules (& variables):

- AppleScript:  VSCode comment:
  # For macOS only! Class for funcs with integration with macOS
  - MakeNotification: module;  VSCode comment: 
    # Will make an notification. Requires agreeing a notification access from "Script Editor" on newer macOS

    # Variables:
    
    - **Description: str; Text (main) of notification**
    - **Title: str | None = None; Title of notification**
    - **Subtitle: str | None = None; Subtitle of notification**
    - **Sound: str | None = 'Ping'; Sound which will be used when notification is showed**
    - **CareAboutTextExceptions: bool | None = True; Used to disable calling -1 return, except just removing prohibited symbols from text**
    
    # Returns (out):
    
    - **-2: If Description, Title, Subtitle is bigger that 240 characters**
    - **-1: Wrong value for: Description, Title, Subtitle; Make sure none of them don't contains symbols like: ", $**
    - **-3: Non-macOS system running**
    
    **Any other - AppleScript out**

cls: module;  VSCode comment: # Clears terminal screen\n# Supports: Windows, Linux, macOS (Darwin)

- color;  VSCode comment:
  # Supports: macOS (Darwin)
  # Colors for print

  Example usage:

  print(f"{print.foreground_st.blue}Proccessing{print.end}") - will display "Proccessing" in blue color

  - foreground_st;  VSCode comment:
    # Start foreground of colors\nUsed to start color of text

    black: str
    red: str
    green: str
    yellow: str
    blue: str
    magenta: str
    cyan: str
    white: str
  - background_st;  VSCode comment:
    # Start background of colors\nUsed to start color of background text
    black: str
    red: str
    green: str
    yellow: str
    blue: str
    magenta: str
    cyan: str
    white: str
  end: str

- wopw
  - Version: int; version in int for checking version
  - VersionType: str; version type, like: Beta or Release
  - BuildCount: int; count of build (used for small releases)
  - Build: str; build of wopw
  - CheckVersion: module;  VSCode comment: 
      # Requires module "requests" and internet connection
      # Checks for lastest version of Wopw
      
      # Returns:
      
      - **1: Version is newest**
      - **2: Version is spoofed (current version is bigger that newest)**
      - **-1: Version outdated**
      - **-2: No module "requests"**
      - **-3: Unknown error while requestsing version**
