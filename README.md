
# Fixing "PS1 Cannot Be Loaded" Error in PowerShell

If you encounter the "PS1 cannot be loaded because running scripts is disabled on this system" error in PowerShell, you can follow these steps to resolve it.

1. **Open PowerShell as Administrator:**
   - Right-click on the PowerShell icon or press `Win + X` and select "Windows PowerShell (Admin)".

2. **Check Current Execution Policy:**
   - Run the following command to check the current execution policy:
     ```powershell
     Get-ExecutionPolicy
     ```

3. **Set Execution Policy for Current User:**
   - If the execution policy is set to "Restricted," change it to "RemoteSigned" for the current user by running:
     ```powershell
     Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
     ```
     You might be prompted to confirm the change; type `Y` for yes.

4. **Reload the PowerShell Session:**
   - Close and reopen the PowerShell session for the changes to take effect.

5. **Check Execution Policy Again:**
   - Confirm that the execution policy is now set to "RemoteSigned" by running:
     ```powershell
     Get-ExecutionPolicy
     ```

6. **Run Your Script:**
   - Try running your PowerShell script again and check if the issue is resolved.

