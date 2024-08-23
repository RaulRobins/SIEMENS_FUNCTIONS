V17 Update 07 Patch OPC UA behavior: 
---------------

This patch intended to solve unexpected TIA Portal crash when compiling the PLC
if there is a connection with a configured OPC UA Server interface.
More details see FAQ: https://support.industry.siemens.com/cs/ww/en/view/109971630

---------------

Install notes:

Attention:
This patch is valid for TIA Portal V17.00.00.07 (V17 Update 7) only.
Please check the version of the TIA Portal on your computer before installing the patch.

-	Install the TIA Portal update before installing the patch.
-	Close all TIA Portal instances before installing the patch.	
-	Copy the ZIP-File to a local drive on the PC where the patch should be installed.
-	Extract the ZIP-File into a temporary folder on the local drive of the PC.
-	Back up the original DLL "Siemens.Simatic.OpcUa.Base.Bl" from the folder "C:\Program Files\Siemens\Automation\Portal V17\Bin" (in case of a standard installation).
-	Copy the DLL "Siemens.Simatic.OpcUa.Base.Bl" from the ZIP-File into the folder "C:\Program Files\Siemens\Automation\Portal V17\Bin" and replace the original files (in case of a standard installation).
-	If errors occur, restore the original files and contact Siemens Customer Support.

---------------

Please verify the affected file after inserting it in regard to correctness.

Please check the SHA256 hash of the zip-file:

- "Siemens.Simatic.OpcUa.Base.Bl.dll"	Value: ff4f414e7520fe25b8a6e3f2595046d3028c3160f8ada4c867100cde498bbcc3

We recommend to use the powershell to check the SHA256 file hash. To determine the file hash, please follow these steps:
- Open the Powershell
- Change the Powershell directory to the directory where the file is located via "cd <Full file path>"
- Type "Get-FileHash Siemens.Simatic.OpcUa.Base.Bl.dll -Algorithm SHA256"
- Wait until the File hash has been generated
- Compare the generated file hash with the one from this document
Alternatively, you can use the batch file described on the following page: https://support.industry.siemens.com/cs/ww/en/view/109483101

Please note that this only works with Windows 10/11 and Windows Server 2019/2022!

---------------
