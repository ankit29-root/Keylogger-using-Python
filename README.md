## Keylogger Capturing using Python

### Uses
Some uses of a keylogger are:
- Security Testing: improving the protection against hidden key loggers;
- Business Administration: Monitor what employees are doing (with their consent);
- School/Institutions: Track keystrokes and log banned words in a file;
- Personal Control and File Backup: Make sure no one is using your computer when you are away;
- Parental Control: Track what your children are doing;
- Self-analysis and assessment.

### Features
- Global event hook on all (incl. On-Screen) keyboards using cross-platform library [Keyboard](https://github.com/boppreh/keyboard). The program makes no attempt to hide itself.
- Pure Python, no C modules to be compiled.
- 2 logging modes:
  - Storing logs locally and once a day sending logs to your onion hidden service (via Tor, of course, stealthily installing it);
  - Debug mode (printing to console).
- Persistence:
  - Adding to Windows Startup.
- Human-readable logs:
  - Logging keys as they actually are in your layout; cyrillic keyboard layout is fully implemented;
  - Logging window titles and current time where appropriate;
  - Backspace support (until the active window is changed);
  - Full upper-/ lowercase detection (capslock + shift keys).
- Privacy protection:
  - RSA public-key encryption of logs on the fly using [PyCryptoDome](https://pycryptodome.readthedocs.io/en/latest/).

#### System requirements
- MS Windows (tested on 10). TODO: test Linux (requires sudo) and macOS support;
- [Python 3](https://www.python.org/downloads/) (tested on v. 3.7.4).

##### System arguments
`Start.py mode [encrypt]`
- **modes**:
  - **local:** store the logs in a local txt file. Filename is a MD5 hash of the current date (YYYY-Mon-DD).
  - **debug:** write to the console.
- **[optional]**
  - **encrypt:** enable the encryption of logs with a public key provided in Start.py.

### Video tutorials (similar but simpler projects)
https://www.youtube.com/watch?v=uODkiVbuR-g
https://www.youtube.com/watch?v=8BiOPBsXh0g
