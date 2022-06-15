# Stop-Windows-10-updates
At CoastFM we don't auto updates, this stops it from happeing and gives us time to do it when we want

1. Use the Windows key + R to open the Run command, type regedit, and click OK to open the Windows registry.
2. Browse the following path:
3. HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\NetworkList\DefaultMediaCost
4. Right-click the DefaultMediaCost key and select Permissions.
5. On the Security tab, click the Advanced button.
6. Next to TrustedInstaller, click the Change link.
7. Type Administrators, and click the Check Names button to make sure you're typing the correct object.
8. Click OK.
9. On the Advanced Security Settings for DefaultMediaCost, check the "Replace owner on subcontainers and objects" check box (Under the change link you just clicked)
10. Click Apply.
11. Click OK.
12. On "Permissions for DefaultMediaCost" window select the Administrators group, and then make sure to check the allow Full Control box.
13. Click Apply.
14. Click OK.
15. On the DefaultMediaCost key, you'll find different entries, including for 3G, 4G, Default, Ethernet, and WiFi with their default data values: 1 or 2. The data value 1 means that the connection type is non-metered, and the data value of 2 means that the connection type is metered. Double-click the Ethernet DWORD (32-bit) Value key, and change the value to 2.
16. Click OK.
17. Close the registry and restart your computer to complete the process.
