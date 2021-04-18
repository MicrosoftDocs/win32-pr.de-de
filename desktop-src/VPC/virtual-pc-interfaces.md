---
title: Windows Virtual PC-Schnittstellen
description: Die folgenden Schnittstellen werden von Windows Virtual PC unterstützt.
ms.assetid: de003075-8609-4303-838e-da449b91dc8d
keywords:
- Virtueller Windows Virtual PC-PC, Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a505fab360214d92b844c282fe12722281770f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340714"
---
# <a name="windows-virtual-pc-interfaces"></a>Windows Virtual PC-Schnittstellen

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Die folgenden Schnittstellen werden von Windows Virtual PC unterstützt.



| Schnittstelle                                                                             | BESCHREIBUNG                                                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**Ivmaccountant**](ivmaccountant.md)<br/>                                     | Ermöglicht den Zugriff auf Buchhaltungs bezogene Informationen für einen virtuellen Computer (VM).<br/>                          |
| [**Ivmdisplay**](ivmdisplay.md)<br/>                                           | Steuert die Anzeigeeinstellungen eines virtuellen Computers.<br/>                                                                 |
| [**Ivmdvddrive**](ivmdvddrive.md)<br/>                                         | Steuert ein CD-ROM-oder DVD-ROM-Laufwerk innerhalb eines virtuellen Computers.<br/>                                                        |
| [**Ivmdvddrivecollection**](ivmdvddrivecollection.md)<br/>                     | Definiert die Sammlung von CD-und DVD-Laufwerken innerhalb des virtuellen Computers.<br/>                                             |
| [**Ivmdvddriveevents**](ivmdvddriveevents.md)<br/>                             | Definiert die ausgehende Ereignis Schnittstelle für die [**ivmdvddrive**](ivmdvddrive.md) -Schnittstelle.<br/>             |
| [**Ivmfloppydrive**](ivmfloppydrive.md)<br/>                                   | Steuert ein Diskettenlaufwerk innerhalb eines virtuellen Computers.<br/>                                                                   |
| [**Ivmfloppydrivecollection**](ivmfloppydrivecollection.md)<br/>               | Definiert eine Sammlung von Diskettenlaufwerken innerhalb der VM.<br/>                                                   |
| [**Ivmfloppydriveevents**](ivmfloppydriveevents.md)<br/>                       | Definiert die ausgehende Ereignis Schnittstelle für die [**ivmfloppydrive**](ivmfloppydrive.md) -Schnittstelle.<br/>       |
| [**Ivmguestos**](ivmguestos.md)<br/>                                           | Definiert das Gast Betriebssystem, das auf einem virtuellen Computer ausgeführt wird.<br/>                                                |
| [**Ivmharddisk**](ivmharddisk.md)<br/>                                         | Ermöglicht den Zugriff auf ein Festplatten Abbild.<br/>                                                                  |
| [**Ivmharddiskconnection**](ivmharddiskconnection.md)<br/>                     | Definiert die Verbindung für eine Festplatte innerhalb der VM.<br/>                                                  |
| [**Ivmharddiskconnectioncollection**](ivmharddiskconnectioncollection.md)<br/> | Definiert die Sammlung von Festplatten Verbindungen innerhalb des virtuellen Computers.<br/>                                         |
| [**Ivmhostinfo**](ivmhostinfo.md)<br/>                                         | Ruft Informationen über den Host Computer ab.<br/>                                                          |
| [**Ivmkeyboard**](ivmkeyboard.md)<br/>                                         | Steuert das Tastatur Gerät innerhalb eines virtuellen Computers.<br/>                                                              |
| [**Ivmmouse**](ivmmouse.md)<br/>                                               | Steuert das Mausgerät innerhalb einer VM.<br/>                                                                 |
| [**Ivmnetworkadapter**](ivmnetworkadapter.md)<br/>                             | Dient als Schnittstelle für eine virtuelle Netzwerkschnittstellenkarte (NIC) innerhalb einer VM.<br/>                         |
| [**Ivmnetworkadaptercollection**](ivmnetworkadaptercollection.md)<br/>         | Definiert eine Sammlung virtueller NICs innerhalb einer VM.<br/>                                                      |
| [**Ivmparallelport**](ivmparallelport.md)<br/>                                 | Definiert einen parallelen Port innerhalb einer VM.<br/>                                                                   |
| [**Ivmparallelportcollection**](ivmparallelportcollection.md)<br/>             | Definiert die Sammlung paralleler Ports innerhalb der VM.<br/>                                                |
| [**Ivmserialport**](ivmserialport.md)<br/>                                     | Definiert einen seriellen Anschluss innerhalb eines virtuellen Computers.<br/>                                                                     |
| [**Ivmserialportcollection**](ivmserialportcollection.md)<br/>                 | Definiert die Sammlung von seriellen Anschlüssen innerhalb der VM.<br/>                                                  |
| [**Ivmtask**](ivmtask.md)<br/>                                                 | Wird verwendet, um asynchrone Aufgaben für verschiedene Methoden zu überwachen und zu steuern.<br/>                                    |
| [**Ivmtaskcollection**](ivmtaskcollection.md)<br/>                             | Definiert die Sammlung von Task Objekten innerhalb eines virtuellen Computers.<br/>                                                    |
| [**Ivmusbdevice**](ivmusbdevice.md)<br/>                                       | Definiert die Schnittstelle für ein USB-Gerät, das mit dem Host System verbunden ist.<br/>                                    |
| [**Ivmusbde vicecollection**](ivmusbdevicecollection.md)<br/>                   | Definiert die Sammlung von USB-Geräten, die mit dem Host System verbunden sind.<br/>                                     |
| [**Ivmvirtualmachine**](ivmvirtualmachine.md)<br/>                             | Definiert die Schnittstelle für eine VM.<br/>                                                                        |
| [**Ivmvirtualmachinecollection**](ivmvirtualmachinecollection.md)<br/>         | Definiert die Sammlung von VMS innerhalb von Windows Virtual PC.<br/>                                               |
| [**Ivmvirtualmachineevents**](ivmvirtualmachineevents.md)<br/>                 | Definiert die ausgehende Ereignis Schnittstelle für die [**ivmvirtualmachine**](ivmvirtualmachine.md) -Schnittstelle.<br/> |
| [**Ivmvirtualnetwork**](ivmvirtualnetwork.md)<br/>                             | Definiert ein virtuelles Netzwerk.<br/>                                                                             |
| [**Ivmvirtualnetworkcollection**](ivmvirtualnetworkcollection.md)<br/>         | Definiert eine Auflistung von [**ivmvirtualnetwork**](ivmvirtualnetwork.md) -Objekten.<br/>                        |
| [**Ivmvirtualpc**](ivmvirtualpc.md)<br/>                                       | Definiert das Windows Virtual PC-Anwendungs Objekt der obersten Ebene.<br/>                                           |
| [**Ivmvirtualpcevents**](ivmvirtualpcevents.md)<br/>                           | Definiert die ausgehende Ereignis Schnittstelle für die [**ivmvirtualpc**](ivmvirtualpc.md) -Schnittstelle.<br/>           |



 

## <a name="note-for-developers-on-64-bit-windows"></a>Hinweis für Entwickler unter 64-Bit-Windows

Bei 64-Bit-Editionen von Windows befindet sich die Typbibliothek für Windows Virtual PC in einer 64-Bit-Binärdatei (VPC.exe) im Verzeichnis% windir% \\ system32. Dieses Verzeichnis ist standardmäßig nicht für 32-Bit-Prozesse sichtbar. WOW64 ordnet den gesamten Zugriff auf das Verzeichnis% windir% \\ system32 dem Verzeichnis% windir% \\ syswow64 standardmäßig zu. Visual Studio ist eine 32-Bit-Binärdatei und kann daher die Datei an diesem Speicherort nicht öffnen. Zum Generieren einer Interoperabilitäts-Assembly für Windows Virtual PC verwenden Sie TlbImp.exe, das in Visual Studio und in der Windows SDK verfügbar ist. Verwenden Sie die folgende Befehlszeile, um *Microsoft.VirtualPC.Interop.dll* zu generieren:

**TlbImp.exe/out: * * * Microsoft.VirtualPC.Interop.dll* **/Namespace: Microsoft. VirtualPC. Interop% windir% \\ system32 \\ #d2**

Zu anderen Lösungen gehören das Kopieren von VPC.exe in ein anderes Verzeichnis, in dem der Compiler Sie finden kann, oder das Verwenden des OleView.exe Tools aus dem Windows SDK, um eine IDL-Datei aus der Typbibliothek in VPC.exe zu extrahieren.

 

