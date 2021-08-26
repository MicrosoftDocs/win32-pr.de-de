---
title: IVMVirtualMachine-Schnittstelle (VPCCOMInterfaces.h)
description: Definiert die Schnittstelle für einen virtuellen Computer.
ms.assetid: c1c243f2-0fb7-4249-8dc9-f0b70059e78f
keywords:
- IVMVirtualMachine-Schnittstelle Virtueller PC
- IVMVirtualMachine-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f2f50c5279bafd12d8edd01a47e9cbcb1a3cc3bb2b89ea140e46cf06c0aa06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124680"
---
# <a name="ivmvirtualmachine-interface"></a>IVMVirtualMachine-Schnittstelle

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definiert die Schnittstelle für einen virtuellen Computer. **IVMVirtualMachine** kann Clients über die [**ausgehende SCHNITTSTELLE IVMVirtualMachineEvents**](ivmvirtualmachineevents.md) über Ereignisse benachrichtigen. **IVMVirtualMachine-Objekte** werden von [**IVMVirtualPC-Methoden**](ivmvirtualpc.md) wie [**CreateVirtualMachine,**](ivmvirtualpc-createvirtualmachine.md) [**RegisterVirtualMachine**](ivmvirtualpc-registervirtualmachine.md)und [**FindVirtualMachine**](ivmvirtualpc-findvirtualmachine.md)zurückgegeben. Sie können auch ein **IVMVirtualMachine-Objekt** aus dem [**IVMVirtualMachineCollection-Objekt**](ivmvirtualmachinecollection.md) abrufen, das von der [**IVMVirtualPC::VirtualMachines-Eigenschaft**](ivmvirtualpc-virtualmachines.md) zurückgegeben wird.

## <a name="members"></a>Member

Die **IVMVirtualMachine-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMVirtualMachine** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IVMVirtualMachine-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                           | Beschreibung                                                                                                |
|:---------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**AddDVDRIVEDrive**](ivmvirtualmachine-adddvdromdrive.md)                       | Fügt dem virtuellen Computer ein neues CD- oder DVD-Laufwerk hinzu.<br/>                                              |
| [**AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md)         | Fügt dem virtuellen Computer eine neue Festplattenverbindung hinzu.<br/>                                         |
| [**AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md)                 | Fügt dem virtuellen Computer eine Netzwerkschnittstelle hinzu.<br/>                                                |
| [**AttachUSBDevice**](ivmvirtualmachine-attachusbdevice.md)                     | Fügt ein USB-Gerät an einen virtuellen Computer an.<br/>                                                     |
| [**DetachUSBDevice**](ivmvirtualmachine-detachusbdevice.md)                     | Gibt ein USB-Gerät von einem virtuellen Computer frei.<br/>                                                   |
| [**DiscardSavedState**](ivmvirtualmachine-discardsavedstate.md)                 | Verwirft alle gespeicherten Statusinformationen für einen gespeicherten virtuellen Computer.<br/>                               |
| [**DiscardUndoDisks**](ivmvirtualmachine-discardundodisks.md)                   | Verwirft die virtuellen Rückgängigdatenträger.<br/>                                                                |
| [**GetActivationValue**](ivmvirtualmachine-getactivationvalue.md)               | Ruft den Wert der angegebenen Aktivierungseinstellung für diesen virtuellen Computer ab.<br/>               |
| [**GetConfigurationValue**](ivmvirtualmachine-getconfigurationvalue.md)         | Ruft den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer ab.<br/>            |
| [**MergeUndoDisks**](ivmvirtualmachine-mergeundodisks.md)                       | Führt die virtuellen Rückgängigdatenträger zusammen.<br/>                                                                  |
| [**Anhalten**](ivmvirtualmachine-pause.md)                                         | Hält den virtuellen Computer an.<br/>                                                                     |
| [**RemoveActivationValue**](ivmvirtualmachine-removeactivationvalue.md)         | Entfernt den Wert der angegebenen Aktivierungseinstellung für diesen virtuellen Computer.<br/>                 |
| [**RemoveConfigurationValue**](ivmvirtualmachine-removeconfigurationvalue.md)   | Entfernt den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer.<br/>              |
| [**RemoveDVAFFINDrive**](ivmvirtualmachine-removedvdromdrive.md)                 | Entfernt das angegebene CD- oder DVD-Laufwerk vom virtuellen Computer.<br/>                                 |
| [**RemoveHardDiskConnection**](ivmvirtualmachine-removeharddiskconnection.md)   | Entfernt die angegebene Festplattenverbindung vom virtuellen Computer.<br/>                            |
| [**RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md)           | Entfernt eine Netzwerkschnittstelle vom virtuellen Computer.<br/>                                           |
| [**Zurücksetzen**](ivmvirtualmachine-reset.md)                                         | Setzt den virtuellen Computer zurück.<br/>                                                                     |
| [**Fortsetzen**](ivmvirtualmachine-resume.md)                                       | Setzt den virtuellen Computer fort.<br/>                                                                    |
| [**Speichern**](ivmvirtualmachine-save.md)                                           | Speichert den Status des virtuellen Computers.<br/>                                                                |
| [**SetActivationValue**](ivmvirtualmachine-setactivationvalue.md)               | Legt den Wert der angegebenen Aktivierungseinstellung für diesen virtuellen Computer fest.<br/>                    |
| [**SetConfigurationValue**](ivmvirtualmachine-setconfigurationvalue.md)         | Legt den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer fest.<br/>                 |
| [**StartCommunicationChannel**](ivmvirtualmachine-startcommunicationchannel.md) | Richtet einen Kommunikationskanal zwischen Host und Gast ein.<br/>                                         |
| [**Start**](ivmvirtualmachine-startup.md)                                     | Startet den virtuellen Computer aus dem nicht initialisierten oder gespeicherten Zustand.<br/>                        |
| [**Startup2**](ivmvirtualmachine-startup2.md)                                   | Startet den virtuellen Computer entweder aus dem nicht initialisierten oder gespeicherten Zustand mit erweiterten Optionen.<br/> |
| [**TurnOff**](ivmvirtualmachine-turnoff.md)                                     | Der virtuelle Computer wird heruntergefahren.<br/>                                                                  |



 

### <a name="properties"></a>Eigenschaften

Die **IVMVirtualMachine-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                            | Zugriffstyp           | Beschreibung                                                                                                                                    |
|:------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Buchhalter**](ivmvirtualmachine-accountant.md)<br/>                       | Schreibgeschützt<br/>  | Ein Fiktiver für diesen virtuellen Computer.<br/>                                                                                             |
| [**AttachedDriveTypes**](ivmvirtualmachine-attacheddrivetypes.md)<br/>       | Schreibgeschützt<br/>  | Ein Array, das den Typ des Laufwerks angibt, das an jeden Speicherort auf dem virtuellen Computer angefügt ist.<br/>                                             |
| [**BaseBoardSerialNumber**](ivmvirtualmachine-baseboardserialnumber.md)<br/> | Lesen/Schreiben<br/> | Die Seriennummer des Basisboards.<br/>                                                                                                       |
| [**BIOSGUID**](ivmvirtualmachine-biosguid.md)<br/>                           | Lesen/Schreiben<br/> | Die BIOS-GUID.<br/>                                                                                                                      |
| [**BIOSSerialNumber**](ivmvirtualmachine-biosserialnumber.md)<br/>           | Lesen/Schreiben<br/> | Die BIOS-Seriennummer.<br/>                                                                                                             |
| [**ChassisAssetTag**](ivmvirtualmachine-chassisassettag.md)<br/>             | Lesen/Schreiben<br/> | Das Chassis-Ressourcentag.<br/>                                                                                                              |
| [**ChassisSerialNumber**](ivmvirtualmachine-chassisserialnumber.md)<br/>     | Lesen/Schreiben<br/> | Die Seriennummer des Gehäuses.<br/>                                                                                                          |
| [**ConfigID**](ivmvirtualmachine-configid.md)<br/>                           | Schreibgeschützt<br/>  | Der eindeutige Bezeichner für den virtuellen Computer.<br/>                                                                                      |
| [**Anzeige**](ivmvirtualmachine-display.md)<br/>                             | Schreibgeschützt<br/>  | Die Videoanzeige für den virtuellen Computer.<br/>                                                                                          |
| [**DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md)<br/>                   | Schreibgeschützt<br/>  | Eine aufzählbare Sammlung von CD- und DVD-Laufwerken, die an den virtuellen Computer angefügt sind.<br/>                                                      |
| [**Datei**](ivmvirtualmachine-file.md)<br/>                                   | Schreibgeschützt<br/>  | Der vollqualifizierte Pfad der VMC-Datei für die Konfiguration des virtuellen Computers.<br/>                                                    |
| [**FloppyDrives**](ivmvirtualmachine-floppydrives.md)<br/>                   | Schreibgeschützt<br/>  | Eine aufzählbare Sammlung von Diskettenlaufwerken, die an den virtuellen Computer angefügt sind.<br/>                                                          |
| [**GuestOS**](ivmvirtualmachine-guestos.md)<br/>                             | Schreibgeschützt<br/>  | Das Gastbetriebssystem für diesen virtuellen Computer.<br/>                                                                                |
| [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)<br/>     | Schreibgeschützt<br/>  | Eine aufzählbare Auflistung von Festplattenverbindungen.<br/>                                                                                  |
| [**Has3DNow**](ivmvirtualmachine-has3dnow.md)<br/>                           | Schreibgeschützt<br/>  | Gibt an, ob der Prozessor den 3DNow-Anweisungssatz unterstützt.<br/>                                                                 |
| [**HasMMX**](ivmvirtualmachine-hasmmx.md)<br/>                               | Schreibgeschützt<br/>  | Gibt an, ob der Prozessor den MMX-Anweisungssatz unterstützt.<br/>                                                                   |
| [**HasSSE**](ivmvirtualmachine-hassse.md)<br/>                               | Schreibgeschützt<br/>  | Gibt an, ob der Prozessor den SSE-Anweisungssatz unterstützt.<br/>                                                                   |
| [**HasSSE2**](ivmvirtualmachine-hassse2.md)<br/>                             | Schreibgeschützt<br/>  | Gibt an, ob der Prozessor den SSE2-Anweisungssatz unterstützt.<br/>                                                                  |
| [**Tastatur**](ivmvirtualmachine-keyboard.md)<br/>                           | Schreibgeschützt<br/>  | Das Tastaturgerät für den virtuellen Computer.<br/>                                                                                        |
| [**Speicher**](ivmvirtualmachine-memory.md)<br/>                               | Lesen/Schreiben<br/> | Die Menge des physischen Arbeitsspeichers auf dem virtuellen Computer in Megabyte.<br/>                                                                 |
| [**Maus**](ivmvirtualmachine-mouse.md)<br/>                                 | Schreibgeschützt<br/>  | Das Mausgerät für den virtuellen Computer.<br/>                                                                                           |
| [**Name**](ivmvirtualmachine-name.md)<br/>                                   | Lesen/Schreiben<br/> | Der Name der Konfiguration des virtuellen Computers.<br/>                                                                                      |
| [**NetworkAdapters**](ivmvirtualmachine-networkadapters.md)<br/>             | Schreibgeschützt<br/>  | Eine aufzählbare Auflistung von NICs, die an den virtuellen Computer angefügt sind.<br/>                                                                   |
| [**Hinweise**](ivmvirtualmachine-notes.md)<br/>                                 | Lesen/Schreiben<br/> | Die Hinweise für den virtuellen Computer.<br/>                                                                                                  |
| [**ParallelPorts**](ivmvirtualmachine-parallelports.md)<br/>                 | Schreibgeschützt<br/>  | Eine aufzählbare Auflistung paralleler Ports.<br/>                                                                                         |
| [**ProcessorSpeed**](ivmvirtualmachine-processorspeed.md)<br/>               | Schreibgeschützt<br/>  | Die Geschwindigkeit des Prozessors in Megahertz (MHz).<br/>                                                                                     |
| [**RdpPipeName**](ivmvirtualmachine-rdppipename.md)<br/>                     | Schreibgeschützt<br/>  | Name der RDP-Verbindungs-Named Pipe, die für Video und Eingabe verwendet wird.<br/>                                                                     |
| [**SavedStateFilePath**](ivmvirtualmachine-savedstatefilepath.md)<br/>       | Schreibgeschützt<br/>  | Der vollständige Pfad zur gespeicherten Zustandsdatei.<br/>                                                                                              |
| [**SerialPorts**](ivmvirtualmachine-serialports.md)<br/>                     | Schreibgeschützt<br/>  | Eine aufzählbare Auflistung von seriellen Anschlüssen.<br/>                                                                                           |
| [**ShutdownActionOnQuit**](ivmvirtualmachine-shutdownactiononquit.md)<br/>   | Lesen/Schreiben<br/> | Die Aktion, die auf diesem virtuellen Computer ausgeführt werden soll, wenn er ausgeführt wird, wenn Windows Virtueller PC beendet wird.<br/>                                |
| [**State**](ivmvirtualmachine-state.md)<br/>                                 | Schreibgeschützt<br/>  | Der aktuelle Status des virtuellen Computers.<br/>                                                                                           |
| [**Rückgängigbar**](ivmvirtualmachine-undoable.md)<br/>                           | Lesen/Schreiben<br/> | Gibt an, ob die Rückgängig-Laufwerke für Festplatten aktiviert sind, die mit dem virtuellen Computer verbunden sind.<br/>                                      |
| [**Undoaction**](ivmvirtualmachine-undoaction.md)<br/>                       | Lesen/Schreiben<br/> | Die Standardaktion, die auf allen rückgängig zu machenden Laufwerken ausgeführt werden soll, wenn der virtuelle Computer aus dem Gastbetriebssystem heruntergefahren wird.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



 

