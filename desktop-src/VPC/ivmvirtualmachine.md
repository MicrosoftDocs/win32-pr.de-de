---
title: Ivmvirtualmachine-Schnittstelle (vpccominterfaces. h)
description: Definiert die Schnittstelle für eine virtuelle Maschine.
ms.assetid: c1c243f2-0fb7-4249-8dc9-f0b70059e78f
keywords:
- Ivmvirtualmachine Interface Virtual PC
- Virtueller Computer für ivmvirtualmachine Interface, beschrieben
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
ms.openlocfilehash: 006fe414a662c3d6d556aba68712aa0b428d9b5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340966"
---
# <a name="ivmvirtualmachine-interface"></a>Ivmvirtualmachine-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert die Schnittstelle für eine virtuelle Maschine. **Ivmvirtualmachine** kann Clients über Ereignisse über die ausgehende Schnittstelle [**ivmvirtualmachineevents**](ivmvirtualmachineevents.md) benachrichtigen. **Ivmvirtualmachine** -Objekte werden von [**ivmvirtualpc**](ivmvirtualpc.md) -Methoden wie z. b. " [**kreatevirtualmachine**](ivmvirtualpc-createvirtualmachine.md)", " [**registervirtualmachine**](ivmvirtualpc-registervirtualmachine.md)" und " [**findvirtualmachine**](ivmvirtualpc-findvirtualmachine.md)" zurückgegeben. Sie können auch ein **ivmvirtualmachine** -Objekt aus dem [**ivmvirtualmachinecollection**](ivmvirtualmachinecollection.md) -Objekt abrufen, das von der [**ivmvirtualpc:: VirtualMachines**](ivmvirtualpc-virtualmachines.md) -Eigenschaft zurückgegeben wird.

## <a name="members"></a>Member

Die **ivmvirtualmachine** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmvirtualmachine** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ivmvirtualmachine** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                           | BESCHREIBUNG                                                                                                |
|:---------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md)                       | Fügt ein neues CD-oder DVD-Laufwerk zum virtuellen Computer hinzu.<br/>                                              |
| [**AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md)         | Fügt der virtuellen Maschine eine neue Festplatten Verbindung hinzu.<br/>                                         |
| [**Addnetworkadapter**](ivmvirtualmachine-addnetworkadapter.md)                 | Fügt der virtuellen Maschine eine Netzwerkschnittstelle hinzu.<br/>                                                |
| [**Attach-bdevice**](ivmvirtualmachine-attachusbdevice.md)                     | Fügt ein USB-Gerät an einen virtuellen Computer an.<br/>                                                     |
| [**Detachobdevice**](ivmvirtualmachine-detachusbdevice.md)                     | Gibt ein USB-Gerät von einem virtuellen Computer frei.<br/>                                                   |
| [**Verwerfen von dsavedstate**](ivmvirtualmachine-discardsavedstate.md)                 | Verwirft alle gespeicherten Zustandsinformationen für eine gespeicherte virtuelle Maschine.<br/>                               |
| [**Verwerfen von dodisks**](ivmvirtualmachine-discardundodisks.md)                   | Verwirft die virtuellen Rückgängig-Datenträger.<br/>                                                                |
| [**Getactivationvalue**](ivmvirtualmachine-getactivationvalue.md)               | Ruft den Wert der angegebenen Aktivierungs Einstellung für diesen virtuellen Computer ab.<br/>               |
| [**GetConfigurationValue**](ivmvirtualmachine-getconfigurationvalue.md)         | Ruft den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer ab.<br/>            |
| [**Mergeundodisks**](ivmvirtualmachine-mergeundodisks.md)                       | Führt die virtuellen Rückgängig-Datenträger zusammen.<br/>                                                                  |
| [**Anhalten**](ivmvirtualmachine-pause.md)                                         | Hält den virtuellen Computer an.<br/>                                                                     |
| [**Removeactivationvalue**](ivmvirtualmachine-removeactivationvalue.md)         | Entfernt den Wert der angegebenen Aktivierungs Einstellung für diesen virtuellen Computer.<br/>                 |
| [**Removeconfigurationvalue**](ivmvirtualmachine-removeconfigurationvalue.md)   | Entfernt den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer.<br/>              |
| [**Removedvdromdrive**](ivmvirtualmachine-removedvdromdrive.md)                 | Entfernt das angegebene CD-oder DVD-Laufwerk von der virtuellen Maschine.<br/>                                 |
| [**Removeharddiskconnection**](ivmvirtualmachine-removeharddiskconnection.md)   | Entfernt die angegebene Festplatten Verbindung von der virtuellen Maschine.<br/>                            |
| [**Removenetworkadapter**](ivmvirtualmachine-removenetworkadapter.md)           | Entfernt eine Netzwerkschnittstelle von der virtuellen Maschine.<br/>                                           |
| [**Zurücksetzen**](ivmvirtualmachine-reset.md)                                         | Setzt den virtuellen Computer zurück.<br/>                                                                     |
| [**Fortsetzen**](ivmvirtualmachine-resume.md)                                       | Setzt den virtuellen Computer fort.<br/>                                                                    |
| [**Speichern**](ivmvirtualmachine-save.md)                                           | Speichert den Zustand der virtuellen Maschine.<br/>                                                                |
| [**Der Wert von "".**](ivmvirtualmachine-setactivationvalue.md)               | Legt den Wert der angegebenen Aktivierungs Einstellung für diesen virtuellen Computer fest.<br/>                    |
| [**Setconfigurationvalue**](ivmvirtualmachine-setconfigurationvalue.md)         | Legt den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer fest.<br/>                 |
| [**Startcommunicationchannel**](ivmvirtualmachine-startcommunicationchannel.md) | Richtet einen Kommunikationskanal zwischen Host und Gast ein.<br/>                                         |
| [**Start**](ivmvirtualmachine-startup.md)                                     | Startet die virtuelle Maschine entweder aus dem nicht initialisierten oder gespeicherten Zustand.<br/>                        |
| [**Startup2**](ivmvirtualmachine-startup2.md)                                   | Startet die virtuelle Maschine entweder über den nicht initialisierten oder gespeicherten Zustand mit erweiterten Optionen.<br/> |
| [**TurnOff**](ivmvirtualmachine-turnoff.md)                                     | Der virtuelle Computer wird heruntergefahren.<br/>                                                                  |



 

### <a name="properties"></a>Eigenschaften

Die **ivmvirtualmachine** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                                    |
|:------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**FERIN**](ivmvirtualmachine-accountant.md)<br/>                       | Schreibgeschützt<br/>  | Ein Buchhalter für diesen virtuellen Computer.<br/>                                                                                             |
| [**"Attacheddrivetypes"**](ivmvirtualmachine-attacheddrivetypes.md)<br/>       | Schreibgeschützt<br/>  | Ein Array, das den Typ des Laufwerks angibt, das an die einzelnen Speicherorte der virtuellen Maschine angehängt ist.<br/>                                             |
| [**Baseboardserialnumber**](ivmvirtualmachine-baseboardserialnumber.md)<br/> | Lesen/Schreiben<br/> | Die Seriennummer des Basis Boards.<br/>                                                                                                       |
| [**Biosguid**](ivmvirtualmachine-biosguid.md)<br/>                           | Lesen/Schreiben<br/> | Die BIOS-GUID.<br/>                                                                                                                      |
| [**BIOSSerialNumber**](ivmvirtualmachine-biosserialnumber.md)<br/>           | Lesen/Schreiben<br/> | Die BIOS-Seriennummer.<br/>                                                                                                             |
| [**Chassisassettag**](ivmvirtualmachine-chassisassettag.md)<br/>             | Lesen/Schreiben<br/> | Das Chassis-Bestands Kennzeichen.<br/>                                                                                                              |
| [**Chassisserialnumber**](ivmvirtualmachine-chassisserialnumber.md)<br/>     | Lesen/Schreiben<br/> | Die Seriennummer des Chassis.<br/>                                                                                                          |
| [**ConfigID**](ivmvirtualmachine-configid.md)<br/>                           | Schreibgeschützt<br/>  | Der eindeutige Bezeichner für den virtuellen Computer.<br/>                                                                                      |
| [**Ausgestellten**](ivmvirtualmachine-display.md)<br/>                             | Schreibgeschützt<br/>  | Die Videoanzeige für den virtuellen Computer.<br/>                                                                                          |
| [**Dvdromdrives**](ivmvirtualmachine-dvdromdrives.md)<br/>                   | Schreibgeschützt<br/>  | Eine Aufzähl Bare Sammlung von CD-und DVD-Laufwerken, die an den virtuellen Computer angefügt sind.<br/>                                                      |
| [**Datei**](ivmvirtualmachine-file.md)<br/>                                   | Schreibgeschützt<br/>  | Der voll qualifizierte Pfad der VMC-Datei für die Konfiguration der virtuellen Maschine.<br/>                                                    |
| [**Floppydrives**](ivmvirtualmachine-floppydrives.md)<br/>                   | Schreibgeschützt<br/>  | Eine Aufzähl Bare Auflistung von Diskettenlaufwerken, die an den virtuellen Computer angefügt sind.<br/>                                                          |
| [**Guestos**](ivmvirtualmachine-guestos.md)<br/>                             | Schreibgeschützt<br/>  | Das Gast Betriebssystem für diesen virtuellen Computer.<br/>                                                                                |
| [**Harddiskconnections**](ivmvirtualmachine-harddiskconnections.md)<br/>     | Schreibgeschützt<br/>  | Eine Aufzähl Bare Auflistung von Festplatten Verbindungen.<br/>                                                                                  |
| [**Has3DNow**](ivmvirtualmachine-has3dnow.md)<br/>                           | Schreibgeschützt<br/>  | Gibt an, ob der Prozessor den 3DNow-Anweisungs Satz unterstützt.<br/>                                                                 |
| [**Hasmmx**](ivmvirtualmachine-hasmmx.md)<br/>                               | Schreibgeschützt<br/>  | Gibt an, ob der Prozessor den MMX-Anweisungs Satz unterstützt.<br/>                                                                   |
| [**Schwierigkeiten**](ivmvirtualmachine-hassse.md)<br/>                               | Schreibgeschützt<br/>  | Gibt an, ob der Prozessor den SSE-Anweisungs Satz unterstützt.<br/>                                                                   |
| [**HasSSE2**](ivmvirtualmachine-hassse2.md)<br/>                             | Schreibgeschützt<br/>  | Gibt an, ob der Prozessor den SSE2-Anweisungs Satz unterstützt.<br/>                                                                  |
| [**Tastatur**](ivmvirtualmachine-keyboard.md)<br/>                           | Schreibgeschützt<br/>  | Das Tastatur Gerät für den virtuellen Computer.<br/>                                                                                        |
| [**Arbeitsspeicher**](ivmvirtualmachine-memory.md)<br/>                               | Lesen/Schreiben<br/> | Die Menge an physischem Arbeitsspeicher auf dem virtuellen Computer in Megabyte.<br/>                                                                 |
| [**Maus**](ivmvirtualmachine-mouse.md)<br/>                                 | Schreibgeschützt<br/>  | Das Mausgerät für den virtuellen Computer.<br/>                                                                                           |
| [**Name**](ivmvirtualmachine-name.md)<br/>                                   | Lesen/Schreiben<br/> | Der Name der Konfiguration der virtuellen Maschine.<br/>                                                                                      |
| [**Netzwerkadapter**](ivmvirtualmachine-networkadapters.md)<br/>             | Schreibgeschützt<br/>  | Eine Aufzähl Bare Auflistung von NICs, die an den virtuellen Computer angefügt sind.<br/>                                                                   |
| [**Notizen**](ivmvirtualmachine-notes.md)<br/>                                 | Lesen/Schreiben<br/> | Die Anmerkungen für den virtuellen Computer.<br/>                                                                                                  |
| [**Parallelports**](ivmvirtualmachine-parallelports.md)<br/>                 | Schreibgeschützt<br/>  | Eine Aufzähl Bare Auflistung paralleler Ports.<br/>                                                                                         |
| [**ProcessorSpeed**](ivmvirtualmachine-processorspeed.md)<br/>               | Schreibgeschützt<br/>  | Die Geschwindigkeit des Prozessors in Megahertz (MHz).<br/>                                                                                     |
| [**Rdppipename**](ivmvirtualmachine-rdppipename.md)<br/>                     | Schreibgeschützt<br/>  | Der Name der RDP-Verbindungs Named Pipe, die für Videos und Eingaben verwendet werden.<br/>                                                                     |
| [**Savedstatefilepath**](ivmvirtualmachine-savedstatefilepath.md)<br/>       | Schreibgeschützt<br/>  | Der vollständige Pfad zur gespeicherten Zustands Datei.<br/>                                                                                              |
| [**SerialPorts**](ivmvirtualmachine-serialports.md)<br/>                     | Schreibgeschützt<br/>  | Eine Aufzähl Bare Auflistung von seriellen Anschlüssen.<br/>                                                                                           |
| [**Shutdownaktiononquit**](ivmvirtualmachine-shutdownactiononquit.md)<br/>   | Lesen/Schreiben<br/> | Die Aktion, die auf dieser virtuellen Maschine ausgeführt werden soll, wenn Sie ausgeführt wird, wenn Windows Virtual PC beendet wird.<br/>                                |
| [**State**](ivmvirtualmachine-state.md)<br/>                                 | Schreibgeschützt<br/>  | Der aktuelle Zustand der virtuellen Maschine.<br/>                                                                                           |
| [**Rückgängig gemacht**](ivmvirtualmachine-undoable.md)<br/>                           | Lesen/Schreiben<br/> | Gibt an, ob die rückgängig-Laufwerke für Festplatten aktiviert sind, die mit dem virtuellen Computer verbunden sind.<br/>                                      |
| [**Nicht doaction**](ivmvirtualmachine-undoaction.md)<br/>                       | Lesen/Schreiben<br/> | Die Standardaktion, die auf allen rückgängig-Laufwerken ausgeführt werden soll, wenn der virtuelle Computer innerhalb des Gast Betriebssystems heruntergefahren wird.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



 

