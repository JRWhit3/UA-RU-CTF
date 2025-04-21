UA RS CTF - By Jared Whitney
2022 Industroyer2 Attack
=====================

Files:
- scada_config.xml: Fake SCADA configuration file.
- scada_config.xml.xmp: Metadata file for scada_config.xml.
- firewall.log: Fake firewall log with a malicious C2 connection.

Analysis Instructions:
1. Install ExifTool: `sudo apt install exiftool` (Linux), `brew install exiftool` (macOS), or download from https://exiftool.org/ (Windows).
2. Extract the ZIP archive.
3. Run `exiftool scada_config.xml.xmp` to view metadata.
4. Run `cat scada_config.xml` and `cat firewall.log` (Linux/macOS) or `type scada_config.xml` and `type firewall.log` (Windows), or open in a text editor (e.g., nano, Notepad).
5. To find the malicious log entry, run `cat firewall.log | grep 185.220.101.123` (Linux/macOS) or `type firewall.log | findstr 185.220.101.123` (Windows).

