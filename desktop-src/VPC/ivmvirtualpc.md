---
title: IVMVirtualPC-Schnittstelle (VPCCOMInterfaces.h)
description: Definiert das Anwendungsobjekt Windows virtuellen PCs auf oberster Ebene. Alle anderen Windows Virtuelle PC-Schnittstellenobjekte werden über dieses Objekt abgerufen.
ms.assetid: 519d3f1b-0a72-4c67-a2d9-124fda6c8b7a
keywords:
- IVMVirtualPC-Schnittstelle Virtueller PC
- IVMVirtualPC-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMVirtualPC
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69dd5eec832e95b2b93ff0fb0bee026428a937fa277f86ff14ef672bc66e0dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124650"
---
# <a name="ivmvirtualpc-interface"></a>IVMVirtualPC-Schnittstelle

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definiert das Anwendungsobjekt Windows virtuellen PCs auf oberster Ebene. Alle anderen Windows Virtuelle PC-Schnittstellenobjekte werden über dieses Objekt abgerufen.

**IVMVirtualPC kann** Clients über Ereignisse benachrichtigen, indem die ausgehende [**IVMVirtualPCEvents-Schnittstelle**](ivmvirtualpcevents.md) verwendet wird.

## <a name="members"></a>Member

Die **IVMVirtualPC-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMVirtualPC** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IVMVirtualPC-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                      | Beschreibung                                                                                              |
|:--------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**CreateDifferencingVirtualHardDisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md) | Erstellt eine sich unterscheidende virtuelle Festplatte.<br/>                                                     |
| [**CreateDynamicVirtualHardDisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)           | Erstellt eine virtuelle Festplatte, deren Größe dynamisch geändert wird.<br/>                                             |
| [**CreateFixedVirtualHardDisk**](ivmvirtualpc-createfixedvirtualharddisk.md)               | Erstellt eine virtuelle Festplatte mit fester Größe.<br/>                                                       |
| [**CreateFloppyDiskImage**](ivmvirtualpc-createfloppydiskimage.md)                         | Erstellt eine Diskettenimagedatei.<br/>                                                             |
| [**CreateVirtualMachine**](ivmvirtualpc-createvirtualmachine.md)                           | Erstellt eine neue Konfiguration des virtuellen Computers und ruft das Objekt des virtuellen Computers ab.<br/>         |
| [**DeleteVirtualMachine**](ivmvirtualpc-deletevirtualmachine.md)                           | Löscht die Konfiguration eines virtuellen Computers.<br/>                                                      |
| [**FindVirtualMachine**](ivmvirtualpc-findvirtualmachine.md)                               | Ruft ein Virtuelles Computerobjekt ab, das der angeforderten Konfiguration entspricht.<br/>                  |
| [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md)                               | Ruft ein virtuelles Netzwerkobjekt ab, das dem angeforderten Namen entspricht.<br/>                           |
| [**GetConfigurationValue**](ivmvirtualpc-getconfigurationvalue.md)                         | Ruft den Wert der angegebenen Konfigurationseinstellung ab<br/>                                   |
| [**GetDVDFiles**](ivmvirtualpc-getdvdfiles.md)                                             | Ruft ein Array bekannter DVD-Dateien ab.<br/>                                                        |
| [**GetFloppyDiskFiles**](ivmvirtualpc-getfloppydiskfiles.md)                               | Ruft ein Array bekannter virtueller Diskettendateien ab.<br/>                                        |
| [**GetFloppyDiskImageType**](ivmvirtualpc-getfloppydiskimagetype.md)                       | Ruft den Typ einer vorhandenen Diskettenimagedatei ab.<br/>                                     |
| [**GetHardDisk**](ivmvirtualpc-getharddisk.md)                                             | Ruft ein Objekt ab, das einer vorhandenen Datenträgerimagedatei entspricht.<br/>                             |
| [**GetHardDiskFiles**](ivmvirtualpc-getharddiskfiles.md)                                   | Ruft ein Array bekannter virtueller Festplattendateien ab.<br/>                                          |
| [**GetVirtualMachineFiles**](ivmvirtualpc-getvirtualmachinefiles.md)                       | Ruft ein Array bekannter Konfigurationsdateien für virtuelle Computer ab.<br/>                              |
| [**RegisterVirtualMachine**](ivmvirtualpc-registervirtualmachine.md)                       | Registriert eine vorhandene Konfiguration eines virtuellen Computers und ruft das Objekt des virtuellen Computers ab.<br/> |
| [**RemoveConfigurationValue**](ivmvirtualpc-removeconfigurationvalue.md)                   | Entfernt den Wert der angegebenen Konfigurationseinstellung.<br/>                                     |
| [**SetConfigurationValue**](ivmvirtualpc-setconfigurationvalue.md)                         | Legt den Wert der angegebenen Konfigurationseinstellung fest.<br/>                                        |
| [**UnregisterVirtualMachine**](ivmvirtualpc-unregistervirtualmachine.md)                   | Aufheben der Registrierung einer Konfiguration eines virtuellen Computers, ohne die Konfigurationsdatei zu löschen.<br/>          |



 

### <a name="properties"></a>Eigenschaften

Die **IVMVirtualPC-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                   | Zugriffstyp           | Beschreibung                                                                                                                                           |
|:-------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md)<br/>   | Lesen/Schreiben<br/> | Das Standardverzeichnis, das nach verfügbaren Konfigurationsdateien für virtuelle Computer durchsucht werden soll.<br/>                                                    |
| [**HostInfo**](ivmvirtualpc-hostinfo.md)<br/>                                       | Schreibgeschützt<br/>  | Informationen zum physischen Computer.<br/>                                                                                                   |
| [**MaximumFloppyDrivesPerVM**](ivmvirtualpc-maximumfloppydrivespervm.md)<br/>       | Schreibgeschützt<br/>  | Die maximale Anzahl von Diskettenlaufwerken pro virtuellem Computer.<br/>                                                                                   |
| [**MaximumMemoryPerVM**](ivmvirtualpc-maximummemorypervm.md)<br/>                   | Schreibgeschützt<br/>  | Die maximal zulässige Menge an physischem Arbeitsspeicher pro virtuellem Computer in Megabyte.<br/>                                                       |
| [**MaximumNetworkAdaptersPerVM**](ivmvirtualpc-maximumnetworkadapterspervm.md)<br/> | Schreibgeschützt<br/>  | Die maximale Anzahl von Netzwerkschnittstellen pro virtuellem Computer.<br/>                                                                             |
| [**MaximumNumberOfIDEBuses**](ivmvirtualpc-maximumnumberofidebuses.md)<br/>         | Schreibgeschützt<br/>  | Die maximale Anzahl zulässiger Buslinien für die IDE.<br/>                                                                                               |
| [**MaximumParallelPortsPerVM**](ivmvirtualpc-maximumparallelportspervm.md)<br/>     | Schreibgeschützt<br/>  | Die maximale Anzahl paralleler Ports pro virtuellem Computer.<br/>                                                                                  |
| [**MaximumSerialPortsPerVM**](ivmvirtualpc-maximumserialportspervm.md)<br/>         | Schreibgeschützt<br/>  | Die maximale Anzahl von seriellen Anschlüssen pro virtuellem Computer.<br/>                                                                                    |
| [**MinimumMemoryPerVM**](ivmvirtualpc-minimummemorypervm.md)<br/>                   | Schreibgeschützt<br/>  | Die minimal zulässige Menge an physischem Arbeitsspeicher pro virtuellem Computer in Megabyte.<br/>                                                       |
| [**Name**](ivmvirtualpc-name.md)<br/>                                               | Schreibgeschützt<br/>  | Der Name der Windows Virtual PC-Anwendung.<br/>                                                                                            |
| [**SearchPaths**](ivmvirtualpc-searchpaths.md)<br/>                                 | Lesen/Schreiben<br/> | Die Dateisystempfade, die verwendet werden, um Dateien zu suchen, die dem virtuellen Windows zugeordnet sind.<br/>                                                      |
| [**SuggestedMaximumMemoryPerVM**](ivmvirtualpc-suggestedmaximummemorypervm.md)<br/> | Schreibgeschützt<br/>  | Die vorgeschlagene maximal zulässige Menge an physischem Arbeitsspeicher pro virtuellem Computer in Megabyte, um niedrige Arbeitsspeicherbedingungen auf dem Host zu vermeiden.<br/> |
| [**Aufgaben**](ivmvirtualpc-tasks.md)<br/>                                             | Schreibgeschützt<br/>  | Eine Auflistung von Aufgaben.<br/>                                                                                                                     |
| [**UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md)<br/>   | Schreibgeschützt<br/>  | Eine aufzählbare Auflistung von nicht verbundenen Netzwerkschnittstellen.<br/>                                                                                |
| [**Verfügbarkeit**](ivmvirtualpc-uptime.md)<br/>                                           | Schreibgeschützt<br/>  | Die Anzahl von Sekunden, die die Windows Virtual PC-Anwendung ausgeführt wurde.<br/>                                                                 |
| [**USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)<br/>                 | Schreibgeschützt<br/>  | Eine aufzählbare Sammlung aller USB-Geräte, die mit dem Host verbunden sind.<br/>                                                                         |
| [**Version**](ivmvirtualpc-version.md)<br/>                                         | Schreibgeschützt<br/>  | Die Version dieser Instanz von Windows Virtual PC.<br/>                                                                                        |
| [**VirtualMachines**](ivmvirtualpc-virtualmachines.md)<br/>                         | Schreibgeschützt<br/>  | Eine aufzählbare Sammlung von virtuellen Computern.<br/>                                                                                              |
| [**VirtualNetworks**](ivmvirtualpc-virtualnetworks.md)<br/>                         | Schreibgeschützt<br/>  | Eine aufzählbare Sammlung virtueller Netzwerke.<br/>                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



 

