---
title: Windows Virtuelle PC-Schnittstellen
description: Die folgenden Schnittstellen werden von einem virtuellen Windows unterstützt.
ms.assetid: de003075-8609-4303-838e-da449b91dc8d
keywords:
- Windows Virtual PC Virtual PC , Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963574a5293a7c48b29096e3dbc563c0f2073c7a697f84a86fa0b5750feeabe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511760"
---
# <a name="windows-virtual-pc-interfaces"></a>Windows Virtuelle PC-Schnittstellen

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Die folgenden Schnittstellen werden von einem virtuellen Windows unterstützt.



| Schnittstelle                                                                             | BESCHREIBUNG                                                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**IVMAccountant**](ivmaccountant.md)<br/>                                     | Bietet Zugriff auf buchhaltungsbezogene Informationen für einen virtuellen Computer (VM).<br/>                          |
| [**IVMDisplay**](ivmdisplay.md)<br/>                                           | Steuert die Anzeigeeinstellungen eines virtuellen Computers.<br/>                                                                 |
| [**IVMDVDDrive**](ivmdvddrive.md)<br/>                                         | Steuert ein CD-ROM- oder DVD-ROM-Laufwerk innerhalb eines virtuellen Computers.<br/>                                                        |
| [**IVMDVDDriveCollection**](ivmdvddrivecollection.md)<br/>                     | Definiert die Sammlung von CD- und DVD-Laufwerken innerhalb des virtuellen Computers.<br/>                                             |
| [**IVMDVDDriveEvents**](ivmdvddriveevents.md)<br/>                             | Definiert die ausgehende Ereignisschnittstelle für die [**IVMDVDDrive-Schnittstelle.**](ivmdvddrive.md)<br/>             |
| [**IVMFloppyDrive**](ivmfloppydrive.md)<br/>                                   | Steuert eine Diskette innerhalb eines virtuellen Computers.<br/>                                                                   |
| [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md)<br/>               | Definiert eine Sammlung von Diskettenlaufwerken innerhalb des virtuellen Computers.<br/>                                                   |
| [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)<br/>                       | Definiert die ausgehende Ereignisschnittstelle für die [**IVMFloppyDrive-Schnittstelle.**](ivmfloppydrive.md)<br/>       |
| [**IVMGuestOS**](ivmguestos.md)<br/>                                           | Definiert das Gastbetriebssystem, das auf einem virtuellen Computer ausgeführt wird.<br/>                                                |
| [**IVMHardDisk**](ivmharddisk.md)<br/>                                         | Ermöglicht den Zugriff auf ein Festplattenimage.<br/>                                                                  |
| [**IVMHardDiskConnection**](ivmharddiskconnection.md)<br/>                     | Definiert die Verbindung für eine Festplatte innerhalb des virtuellen Computers.<br/>                                                  |
| [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)<br/> | Definiert die Sammlung von Festplattenverbindungen innerhalb des virtuellen Computers.<br/>                                         |
| [**IVMHostInfo**](ivmhostinfo.md)<br/>                                         | Ruft Informationen zum Hostcomputer ab.<br/>                                                          |
| [**IVMKeyboard**](ivmkeyboard.md)<br/>                                         | Steuert das Tastaturgerät innerhalb eines virtuellen Computers.<br/>                                                              |
| [**IVMMouse**](ivmmouse.md)<br/>                                               | Steuert das Mausgerät innerhalb eines virtuellen Computers.<br/>                                                                 |
| [**IVMNetworkAdapter**](ivmnetworkadapter.md)<br/>                             | Dient als Schnittstelle zu einer virtuellen Netzwerkschnittstellenkarte (NIC) innerhalb eines virtuellen Computers.<br/>                         |
| [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)<br/>         | Definiert eine Sammlung virtueller NICs innerhalb eines virtuellen Computers.<br/>                                                      |
| [**IVMParallelPort**](ivmparallelport.md)<br/>                                 | Definiert einen parallelen Port innerhalb eines virtuellen Computers.<br/>                                                                   |
| [**IVMParallelPortCollection**](ivmparallelportcollection.md)<br/>             | Definiert die Sammlung paralleler Ports innerhalb des virtuellen Computers.<br/>                                                |
| [**IVMSerialPort**](ivmserialport.md)<br/>                                     | Definiert einen seriellen Anschluss innerhalb eines virtuellen Computers.<br/>                                                                     |
| [**IVMSerialPortCollection**](ivmserialportcollection.md)<br/>                 | Definiert die Sammlung von seriellen Anschlüssen innerhalb des virtuellen Computers.<br/>                                                  |
| [**IVMTask**](ivmtask.md)<br/>                                                 | Wird verwendet, um asynchrone Aufgaben für verschiedene Methoden zu überwachen und zu steuern.<br/>                                    |
| [**IVMTaskCollection**](ivmtaskcollection.md)<br/>                             | Definiert die Sammlung von Aufgabenobjekten innerhalb eines virtuellen Computers.<br/>                                                    |
| [**IVMUSBDevice**](ivmusbdevice.md)<br/>                                       | Definiert die Schnittstelle für ein USB-Gerät, das an das Hostsystem angeschlossen ist.<br/>                                    |
| [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md)<br/>                   | Definiert die Sammlung von USB-Geräten, die an das Hostsystem angeschlossen sind.<br/>                                     |
| [**IVMVirtualMachine**](ivmvirtualmachine.md)<br/>                             | Definiert die Schnittstelle für einen virtuellen Computer.<br/>                                                                        |
| [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)<br/>         | Definiert die Sammlung von VMs innerhalb Windows virtuellen PCs.<br/>                                               |
| [**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)<br/>                 | Definiert die ausgehende Ereignisschnittstelle für die [**IVMVirtualMachine-Schnittstelle.**](ivmvirtualmachine.md)<br/> |
| [**IVMVirtualNetwork**](ivmvirtualnetwork.md)<br/>                             | Definiert ein virtuelles Netzwerk.<br/>                                                                             |
| [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)<br/>         | Definiert eine Auflistung von [**IVMVirtualNetwork-Objekten.**](ivmvirtualnetwork.md)<br/>                        |
| [**IVMVirtualPC**](ivmvirtualpc.md)<br/>                                       | Definiert das Anwendungsobjekt Windows virtuellen PCs auf oberster Ebene.<br/>                                           |
| [**IVMVirtualPCEvents**](ivmvirtualpcevents.md)<br/>                           | Definiert die ausgehende Ereignisschnittstelle für die [**IVMVirtualPC-Schnittstelle.**](ivmvirtualpc.md)<br/>           |



 

## <a name="note-for-developers-on-64-bit-windows"></a>Hinweis für Entwickler auf 64-Bit-Windows

In 64-Bit-Editionen von Windows befindet sich die Typbibliothek für Windows Virtual PC in einer 64-Bit-Binärdatei (VPC.exe) im Verzeichnis %WinDir% \\ System32. Dieses Verzeichnis ist standardmäßig nicht für 32-Bit-Prozesse sichtbar. WOW64 ordnet den gesamten Zugriff auf das Verzeichnis %WinDir% System32 standardmäßig dem \\ Verzeichnis %WinDir% \\ SysWOW64 zu. Visual Studio ist eine 32-Bit-Binärdatei und kann die Datei daher nicht an diesem Speicherort öffnen. Um eine Interoperabilitäts-Assembly für Windows Virtuellen PC zu generieren, verwenden Sie TlbImp.exe, das im Visual Studio sdk Windows ist. Verwenden Sie *dieMicrosoft.VirtualPC.Interop.dll* Befehlszeile, um ein -Microsoft.VirtualPC.Interop.dllzu generieren:

**TlbImp.exe /out:** _Microsoft.VirtualPC.Interop.dll_ **/namespace:Microsoft.VirtualPC.Interop %WinDir% \\ System32 \\VPC.exe**

Andere Lösungen umfassen das Kopieren von VPC.exe in ein anderes Verzeichnis, in dem der Compiler sie finden kann, oder die Verwendung des OleView.exe-Tools aus dem Windows SDK zum Extrahieren einer IDL-Datei aus der Typbibliothek in VPC.exe.

 

