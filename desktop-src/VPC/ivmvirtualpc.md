---
title: Ivmvirtualpc-Schnittstelle (vpccominterfaces. h)
description: Definiert das Windows Virtual PC-Anwendungs Objekt der obersten Ebene. Alle anderen Windows Virtual PC-Schnittstellen Objekte werden über dieses Objekt abgerufen.
ms.assetid: 519d3f1b-0a72-4c67-a2d9-124fda6c8b7a
keywords:
- Ivmvirtualpc Interface Virtual PC
- Virtueller Computer für ivmvirtualpc-Schnittstelle, beschrieben
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
ms.openlocfilehash: 9d674fd1cbbe6c51881d15f91f0ebfb20f4f6749
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040733"
---
# <a name="ivmvirtualpc-interface"></a>Ivmvirtualpc-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert das Windows Virtual PC-Anwendungs Objekt der obersten Ebene. Alle anderen Windows Virtual PC-Schnittstellen Objekte werden über dieses Objekt abgerufen.

**Ivmvirtualpc** kann Clients über Ereignisse über die ausgehende Schnittstelle [**ivmvirtualpcevents**](ivmvirtualpcevents.md) benachrichtigen.

## <a name="members"></a>Member

Die **ivmvirtualpc** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmvirtualpc** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ivmvirtualpc** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                      | BESCHREIBUNG                                                                                              |
|:--------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**"Kreatedifferencingvirtualharddisk"**](ivmvirtualpc-createdifferencingvirtualharddisk.md) | Erstellt eine differenzierende virtuelle Festplatte.<br/>                                                     |
| [**"Kreatedynamicvirtualharddisk"**](ivmvirtualpc-createdynamicvirtualharddisk.md)           | Erstellt eine dynamische Größe der virtuellen Festplatte.<br/>                                             |
| [**"Kreatefixedvirtualharddisk"**](ivmvirtualpc-createfixedvirtualharddisk.md)               | Erstellt eine virtuelle Festplatte mit fester Größe.<br/>                                                       |
| [**"Kreatefloppydiskimage"**](ivmvirtualpc-createfloppydiskimage.md)                         | Erstellt eine Disketten Image Datei.<br/>                                                             |
| [**"Kreatevirtualmachine"**](ivmvirtualpc-createvirtualmachine.md)                           | Erstellt eine neue Konfiguration für virtuelle Maschinen und ruft das Objekt der virtuellen Maschine ab.<br/>         |
| [**Deletevirtualmachine**](ivmvirtualpc-deletevirtualmachine.md)                           | Löscht die Konfiguration einer virtuellen Maschine.<br/>                                                      |
| [**Findvirtualmachine**](ivmvirtualpc-findvirtualmachine.md)                               | Ruft ein Objekt für virtuelle Maschinen ab, das mit der angeforderten Konfiguration übereinstimmt.<br/>                  |
| [**Findvirtualnetwork**](ivmvirtualpc-findvirtualnetwork.md)                               | Ruft ein virtuelles Netzwerk Objekt ab, das mit dem angeforderten Namen übereinstimmt.<br/>                           |
| [**GetConfigurationValue**](ivmvirtualpc-getconfigurationvalue.md)                         | Ruft den Wert der angegebenen Konfigurationseinstellung ab<br/>                                   |
| [**Getdvdfiles**](ivmvirtualpc-getdvdfiles.md)                                             | Ruft ein Array bekannter DVD-Dateien ab.<br/>                                                        |
| [**Getfloppydiskfiles**](ivmvirtualpc-getfloppydiskfiles.md)                               | Ruft ein Array bekannter virtueller Disketten Dateien ab.<br/>                                        |
| [**Getfloppydiskimagetype**](ivmvirtualpc-getfloppydiskimagetype.md)                       | Ruft den Typ einer vorhandenen Disketten Image Datei ab.<br/>                                     |
| [**Getharddisk**](ivmvirtualpc-getharddisk.md)                                             | Ruft ein Objekt ab, das einer vorhandenen Datenträger Image Datei entspricht.<br/>                             |
| [**Getharddiskfiles**](ivmvirtualpc-getharddiskfiles.md)                                   | Ruft ein Array bekannter virtueller Festplatten Dateien ab.<br/>                                          |
| [**Getvirtualmachinefiles**](ivmvirtualpc-getvirtualmachinefiles.md)                       | Ruft ein Array bekannter Konfigurationsdateien für virtuelle Maschinen ab.<br/>                              |
| [**Registervirtualmachine**](ivmvirtualpc-registervirtualmachine.md)                       | Registriert eine vorhandene VM-Konfiguration und ruft das Objekt der virtuellen Maschine ab.<br/> |
| [**Removeconfigurationvalue**](ivmvirtualpc-removeconfigurationvalue.md)                   | Entfernt den Wert der angegebenen Konfigurationseinstellung.<br/>                                     |
| [**Setconfigurationvalue**](ivmvirtualpc-setconfigurationvalue.md)                         | Legt den Wert der angegebenen Konfigurationseinstellung fest.<br/>                                        |
| [**Unregistervirtualmachine**](ivmvirtualpc-unregistervirtualmachine.md)                   | Hebt die Registrierung der Konfiguration einer virtuellen Maschine auf, ohne die Konfigurationsdatei zu löschen.<br/>          |



 

### <a name="properties"></a>Eigenschaften

Die **ivmvirtualpc** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                   | Zugriffstyp           | BESCHREIBUNG                                                                                                                                           |
|:-------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Defaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md)<br/>   | Lesen/Schreiben<br/> | Das Standardverzeichnis, das nach verfügbaren Konfigurationsdateien für virtuelle Maschinen durchsucht werden soll.<br/>                                                    |
| [**Hostinfo**](ivmvirtualpc-hostinfo.md)<br/>                                       | Schreibgeschützt<br/>  | Informationen zum physischen Computer.<br/>                                                                                                   |
| [**Maximumfloppydrivespervm**](ivmvirtualpc-maximumfloppydrivespervm.md)<br/>       | Schreibgeschützt<br/>  | Die maximale Anzahl von Diskettenlaufwerken pro virtuellem Computer.<br/>                                                                                   |
| [**Maximummemorypervm**](ivmvirtualpc-maximummemorypervm.md)<br/>                   | Schreibgeschützt<br/>  | Die maximal zulässige Menge an physischem Arbeitsspeicher pro virtuellem Computer in Megabyte.<br/>                                                       |
| [**Maximumnetworkadapterspervm**](ivmvirtualpc-maximumnetworkadapterspervm.md)<br/> | Schreibgeschützt<br/>  | Die maximale Anzahl von Netzwerkschnittstellen pro virtuellem Computer.<br/>                                                                             |
| [**Maximumanzahlofi**](ivmvirtualpc-maximumnumberofidebuses.md)<br/>         | Schreibgeschützt<br/>  | Die maximal zulässige Anzahl von Bussen für IDE.<br/>                                                                                               |
| [**Maximumparallelportspervm**](ivmvirtualpc-maximumparallelportspervm.md)<br/>     | Schreibgeschützt<br/>  | Die maximale Anzahl paralleler Ports pro virtuellem Computer.<br/>                                                                                  |
| [**Maximumserialportspervm**](ivmvirtualpc-maximumserialportspervm.md)<br/>         | Schreibgeschützt<br/>  | Die maximale Anzahl von seriellen Anschlüssen pro virtuellem Computer.<br/>                                                                                    |
| [**Minimummemorypervm**](ivmvirtualpc-minimummemorypervm.md)<br/>                   | Schreibgeschützt<br/>  | Die minimale zulässige Menge an physischem Arbeitsspeicher pro virtuellem Computer in Megabyte.<br/>                                                       |
| [**Name**](ivmvirtualpc-name.md)<br/>                                               | Schreibgeschützt<br/>  | Der Name der Windows Virtual PC-Anwendung.<br/>                                                                                            |
| [**SearchPath**](ivmvirtualpc-searchpaths.md)<br/>                                 | Lesen/Schreiben<br/> | Die Dateisystem Pfade, die verwendet werden, um Dateien zu suchen, die mit Windows Virtual PC verknüpft sind.<br/>                                                      |
| [**Vorschlag von "Vorschlag-maximummemorypervm"**](ivmvirtualpc-suggestedmaximummemorypervm.md)<br/> | Schreibgeschützt<br/>  | Die vorgeschlagene maximal zulässige Menge an physischem Arbeitsspeicher pro virtuellem Computer in Megabyte, um wenig Speicherplatz auf dem Host zu vermeiden.<br/> |
| [**Aufgaben**](ivmvirtualpc-tasks.md)<br/>                                             | Schreibgeschützt<br/>  | Eine Auflistung von Tasks.<br/>                                                                                                                     |
| [**Unconnectednetworkadapters**](ivmvirtualpc-unconnectednetworkadapters.md)<br/>   | Schreibgeschützt<br/>  | Eine Aufzähl Bare Auflistung von nicht verbundenen Netzwerkschnittstellen.<br/>                                                                                |
| [**Betriebszeit**](ivmvirtualpc-uptime.md)<br/>                                           | Schreibgeschützt<br/>  | Die Anzahl der Sekunden, die die Windows Virtual PC-Anwendung ausgeführt wurde.<br/>                                                                 |
| [**"Start"**](ivmvirtualpc-usbdevicecollection.md)<br/>                 | Schreibgeschützt<br/>  | Eine Aufzähl Bare Auflistung aller USB-Geräte, die mit dem Host verbunden sind.<br/>                                                                         |
| [**Version**](ivmvirtualpc-version.md)<br/>                                         | Schreibgeschützt<br/>  | Die Version dieser Instanz von Windows Virtual PC.<br/>                                                                                        |
| [**VirtualMachines**](ivmvirtualpc-virtualmachines.md)<br/>                         | Schreibgeschützt<br/>  | Eine Aufzähl Bare Auflistung von virtuellen Computern.<br/>                                                                                              |
| [**VirtualNetworks**](ivmvirtualpc-virtualnetworks.md)<br/>                         | Schreibgeschützt<br/>  | Eine Aufzähl Bare Auflistung von virtuellen Netzwerken.<br/>                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.<br/>               |



 

