# Optimizing the Internet: MSI/MSI-X support in the network adapter

- One of the key elements to maximizing the speed of your Internet connection is to use a network adapter that supports Message-Signaled Interrupts (MSI/MSI-X).  

## MSI and MSI-X:

> MSI (Message-Signaled Interrupt):  This is a mechanism that allows devices to signal events to the processor more efficiently than traditional interrupts.  
> MSI-X: This is an enhanced version of MSI that allows devices to generate multiple interrupts simultaneously, which increases system performance.

## Benefits of MSI/MSI-X:

- Improved performance: MSI/MSI-X allows the CPU to handle requests from the network adapter more efficiently, resulting in faster Internet speeds. Reduced CPU load: MSI/MSI-X reduce the number of interrupts that the CPU must handle, which reduces CPU load and improves overall system performance.

# How to verify MSI/MSI-X support:

## Use PowerShell commands:

```
Get-NetAdapterHardwareInfo | fl
Get-SmbClientNetworkInterface
```
        
## Check the results:

- In the output of the Get-NetAdapterHardwareInfo command, look for the LineBasedInterruptSupported, MsiInterruptSupported, and MsiXInterruptSupported properties.  If the values are True, your network adapter supports MSI/MSI-X. In the output of the Get-SmbClientNetworkInterface command, make sure that the RSS Capable column is True. This means that the network adapter supports RSS (Receive Side Scaling), which works in conjunction with MSI/MSI-X.

## Additional Guidelines:

If your network adapter supports MSI/MSI-X but these features are not enabled, refer to your network adapter documentation or the device manufacturer for instructions on how to enable MSI/MSI-X.

> Verify that the network adapter driver is compatible with MSI/MSI-X.  Update the driver if necessary.
> Check the BIOS settings and make sure MSI/MSI-X support is enabled.
