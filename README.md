# hello-world
Encrypt Azure VM script
This works on Advocare
Login FIRST using the below command

Connect-AzAccount




$KVRGname = 'Production';
 $VMRGName = 'Production';
 $vmName = 'AZFILE002';
 $KeyVaultName = 'Advocare-Disk-Encrypt2';
 $KeyVault = Get-AzKeyVault -VaultName $KeyVaultName -ResourceGroupName $KVRGname;
 $diskEncryptionKeyVaultUrl = $KeyVault.VaultUri;
 $KeyVaultResourceId = $KeyVault.ResourceId;

 Set-AzVMDiskEncryptionExtension -ResourceGroupName $VMRGname -VMName $vmName -DiskEncryptionKeyVaultUrl $diskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId;
 
 
 
 
 
 
 changes account
 Set-AzContext -Subscription "e2c5a7c7-0912-4ba3-8b65-3f8812e6b43c"
 
 
 
List Azure account
 Set-AzContext -Subscription "adfdd4ac-312a-495d-b09c-a5726de07f96"
 

 Set-AzContext -Subscription " adfdd4ac-312a-495d-b09c-a5726de07f96"
