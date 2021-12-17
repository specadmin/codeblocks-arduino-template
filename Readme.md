# Arduino project template for Code::Blocks IDE #

Arduino projects could be built with any IDE. This template allows you to create and configure an empty Arduino project in Code::Blocks IDE.


## Usage ##

1. Start Code:Blocks IDE and create a new project (File -> New -> Project).
2. Select "Arduino project" template and follow the wizard's instructions.
3. Select the target for your Arduino board.
4. Build your project by the "Build" command.
5. Upload your sketch into the board by the "Run" command.


## Dependencies ##

* Code::Blocks IDE
* gcc-avr
* avr-libc
* avrdude
* miniterm


## Integration into Code::Blocks ##

1. Find Code::Blocks templates directory 
```
cd /usr/share/codeblocks/templates/wizard
```

2. Backup an existing Arduino template (if present)
```
sudo mv arduino arduino.bak
```

3. Clone this repository
```
sudo git clone https://github.com/specadmin/codeblocks-arduino-template.git arduino
```

4. Ensure the following line is present in config.script file in RegisterWizards() function:
```
RegisterWizard(wizProject,     _T("arduino"),      _T("Arduino Project"),       _T("Embedded Systems"));
```

5. Restart Code::Blocks IDE