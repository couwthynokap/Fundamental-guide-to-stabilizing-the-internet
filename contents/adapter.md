# Internet Optimization: Network Adapter Settings

# It's important
> [!CAUTION]
> Information about network adapter settings is available in the documentation for your network adapter.
> Some system optimization software allows you to change the network adapter settings more conveniently.

- There are two important settings in the network adapter settings that can greatly affect the speed and stability of your Internet connection: Offload and Powersaving.

## Offload:

- Offload is a feature that shifts some packet processing tasks from the CPU to the network adapter. This can increase the speed and stability of your Internet connection, especially under heavy load.

## Powersaving:

- Powersaving is a feature that allows the network adapter to go into a low power consumption mode when not in use. 

## How to configure the network adapter:

- Open powershell and paste these commands

## Offloads Enabled:
 ```
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*EEE" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*FlowControl" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*IPChecksumOffloadIPv4" -RegistryValue "3" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*InterruptModeration" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*LsoV2IPv4" -RegistryValue "1" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*LsoV2IPv6" -RegistryValue "1" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*NumRssQueues" -RegistryValue "2" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*PMARPOffload" -RegistryValue "1" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*PMNSOffload" -RegistryValue "1" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*PriorityVLANTag" -RegistryValue "1" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*RSS" -RegistryValue "1" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*WakeOnMagicPacket" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*WakeOnPattern" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*ReceiveBuffers" -RegistryValue "2048" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*TransmitBuffers" -RegistryValue "2048" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*TCPChecksumOffloadIPv4" -RegistryValue "3" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*TCPChecksumOffloadIPv6" -RegistryValue "3" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*UDPChecksumOffloadIPv4" -RegistryValue "3" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*UDPChecksumOffloadIPv6" -RegistryValue "3" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "DMACoalescing" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "EEELinkAdvertisement" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "ITR" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "ReduceSpeedOnPowerDown" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "WaitAutoNegComplete" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "WakeOnLink" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "AdvancedEEE" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "EnableGreenEthernet" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "GigaLite" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "PowerSavingMode" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "S5WakeOnLan" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "WolShutdownLinkSpeed" -RegistryValue "2" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "LogLinkStateEvent" -RegistryValue "16" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "WakeOnMagicPacketFromS5" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -DisplayName "Ultra Low Power Mode" -DisplayValue "Disabled" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -DisplayName "System Idle Power Saver" -DisplayValue "Disabled" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -DisplayName "Selective Suspend" -DisplayValue "Disabled" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -DisplayName "Selective Suspend Idle Timeout" -DisplayValue "60" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -DisplayName "Link Speed Battery Saver" -DisplayValue "Disabled" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "*SelectiveSuspend" -RegistryValue "0" >nul 2>&1 
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "EnablePME" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "TxIntDelay" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "TxDelay" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "EnableModernStandby" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "*ModernStandbyWoLMagicPacket" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "EnableLLI" -RegistryValue "1" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "*SSIdleTimeout" -RegistryValue "60" >nul 2>&1
 ```

## Offloads Disabled:
 ```
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*EEE" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*FlowControl" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*IPChecksumOffloadIPv4" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*InterruptModeration" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*LsoV2IPv4" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*LsoV2IPv6" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*NumRssQueues" -RegistryValue "2" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*PMARPOffload" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*PMNSOffload" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*PriorityVLANTag" -RegistryValue "1" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*RSS" -RegistryValue "1" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*WakeOnMagicPacket" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*WakeOnPattern" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*ReceiveBuffers" -RegistryValue "2048" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*TransmitBuffers" -RegistryValue "2048" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*TCPChecksumOffloadIPv4" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*TCPChecksumOffloadIPv6" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*UDPChecksumOffloadIPv4" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "*UDPChecksumOffloadIPv6" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "DMACoalescing" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "EEELinkAdvertisement" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "ITR" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "ReduceSpeedOnPowerDown" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "WaitAutoNegComplete" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "WakeOnLink" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "AdvancedEEE" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "EnableGreenEthernet" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "GigaLite" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "PowerSavingMode" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "S5WakeOnLan" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "WolShutdownLinkSpeed" -RegistryValue "2" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "LogLinkStateEvent" -RegistryValue "16" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -RegistryKeyword "WakeOnMagicPacketFromS5" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -DisplayName "Ultra Low Power Mode" -DisplayValue "Disabled" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -DisplayName "System Idle Power Saver" -DisplayValue "Disabled" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -DisplayName "Selective Suspend" -DisplayValue "Disabled" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -DisplayName "Selective Suspend Idle Timeout" -DisplayValue "60" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -Name "*" -DisplayName "Link Speed Battery Saver" -DisplayValue "Disabled" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "*SelectiveSuspend" -RegistryValue "0" >nul 2>&1 
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "EnablePME" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "TxIntDelay" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "TxDelay" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "EnableModernStandby" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "*ModernStandbyWoLMagicPacket" -RegistryValue "0" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "EnableLLI" -RegistryValue "1" >nul 2>&1
powershell Set-NetAdapterAdvancedProperty -AllProperties -Name "*" -RegistryKeyword "*SSIdleTimeout" -RegistryValue "60" >nul 2>&1
 ```

## Additional information:

- Open a command prompt as administrator. Paste the copied commands one by one and press Enter.

## Registry Settings

 ```
Reg.exe add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile" /v "NetworkThrottlingIndex" /t REG_DWORD /d "10" /f
Reg.exe add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile" /v "SystemResponsiveness" /t REG_DWORD /d "10" /f
Reg.exe add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile" /v "NoLazyMode" /t REG_DWORD /d "1" /f
Reg.exe add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "EnableICMPRedirect" /t REG_DWORD /d "1" /f
Reg.exe add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "AllowUnqualifiedQuery" /t REG_DWORD /d "1" /f
Reg.exe add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "DisableMediaSenseEventLog" /t REG_DWORD /d "1" /f
Reg.exe add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "EnableBcastArpReply" /t REG_DWORD /d "0" /f
Reg.exe add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "EnableConnectionRateLimiting" /t REG_DWORD /d "0" /f
Reg.exe add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "EnableIPAutoConfigurationLimits" /t REG_DWORD /d "0" /f
Reg.exe add "HKLM\SOFTWARE\Policies\Microsoft\Windows\Psched" /v "NonBestEffortLimit" /t REG_DWORD /d "1" /f
Reg.exe add "HKLM\SYSTEM\CurrentControlSet\services\NDIS\Parameters" /v "RssBaseCpu" /t REG_DWORD /d "1" /f
Reg.exe add "HKLM\SOFTWARE\Microsoft\MSMQ\Parameters" /v "TCPNoDelay" /t REG_DWORD /d "1" /f
Reg.exe add "HKLM\SOFTWARE\Microsoft\MSMQ\Parameters\Security" /v "SecureDSCommunication" /t REG_DWORD /d "0" /f
Reg.exe add "HKLM\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters" /v "IRPStackSize" /t REG_DWORD /d "32" /f
Reg.exe add "HKLM\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters" /v "Size" /t REG_DWORD /d "3" /f
 ```

## Netsh Settings

 ```
netsh winsock set autotuning on
netsh int ip set global neighborcachelimit=4096
netsh int ip set global routecachelimit=4096
netsh int ip set global sourceroutingbehavior=drop
netsh int ip set global taskoffload=enabled
netsh int ip set global dhcpmediasense=disabled
netsh int ip set global mediasenseeventlog=disabled
netsh int ip set global icmpredirects= disabled
netsh int ip set global randomizeidentifiers=disabled
netsh int tcp set global chimney=enabled
netsh int tcp set global dca=enabled
netsh int tcp set global netdma=disabled
netsh int tcp set global rsc=disabled
netsh int tcp set global maxsynretransmissions=2
netsh int tcp set global timestamps=disabled
netsh int tcp set global ecncapability=disabled
netsh int tcp set global congestionprovider=ctcp
netsh interface teredo set state disabled
netsh int isatap set state disable
netsh int ipv6 isatap set state disabled
netsh int ipv6 6to4 set state disabled
netsh interface IPV6 set global randomizeidentifier=disabled
netsh interface IPV6 set privacy state=disabled
netsh int ipv6 set global dhcpmediasense=disabled
netsh int ipv6 set global icmpredirects= disabled
netsh int ipv6 set global sourceroutingbehavior=drop
netsh int 6to4 set state disabled
netsh int teredo set state disabled
netsh int tcp set global initialRto=2000
netsh int tcp set heuristics disabled
netsh int tcp set heuristics wsh=disabled
netsh int tcp set security mpp=disabled
netsh int tcp set security profiles=disabled
netsh int ipv4 set dynamicport tcp start=1025 num=64511
netsh int ipv4 set dynamicport udp start=1025 num=64511
 ```
