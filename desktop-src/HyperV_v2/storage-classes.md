---
description: 'Die Speicherobjekte sind in drei Typen unterteilt: Controller, Laufwerke und Medien.'
ms.assetid: CF38F6E8-A43D-4A97-8055-6B17E323524C
title: Speicherklassen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c46efc17b3df5e1a509cec3565c6aaa7b65ff06d189951b100ac06d93a957e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829670"
---
# <a name="storage-classes"></a>Speicherklassen

Die Speicherobjekte sind in drei Typen unterteilt: Controller, Laufwerke und Medien.

Es gibt zwei Controller, einen emulierten IDE-Controller und einen synthetischen SCSI-Controller. Beide Controller unterstützen das Anhängen von Laufwerken, die die Medien hosten.

Im Folgenden finden Sie Virtualisierungs-WMI-Klassen im Zusammenhang mit Speicher. Es gibt auch Unterstützung für synthetische Diskettenmedien. Das Anfügen an ein physisches Diskettenlaufwerk wird nicht unterstützt.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                      | BESCHREIBUNG                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ AffectedStorageJobElement**](msvm-affectedstoragejobelement.md)<br/>       | Stellt die Zuordnung zwischen einem Auftrag und den verwalteten Elementen dar, die von seiner Ausführung betroffen sein können.<br/>                                                                                               |
| [**Msvm \_ BasedOn**](msvm-basedon.md)<br/>                                           | Eine Zuordnung, die beschreibt, wie Speichergefässungen aus niedrigeren Speicherebenen zusammengesetzt werden können.<br/>                                                                                                           |
| [**Msvm \_ ControlledBy**](msvm-controlledby.md)<br/>                                 | Ordnet dem Speichercontroller, der das Gerät besitzt, ein Speichergerät zu.<br/>                                                                                                                          |
| [**Msvm \_ DiskDrive**](msvm-diskdrive.md)<br/>                                       | Stellt ein Festplattenlaufwerk innerhalb eines virtuellen Computers dar.<br/>                                                                                                                                              |
| [**Msvm \_ DisketteController**](msvm-diskettecontroller.md)<br/>                     | Stellt den Diskettencontroller auf dem virtuellen Computer dar.<br/>                                                                                                                                               |
| [**Msvm \_ DisketteDrive**](msvm-diskettedrive.md)<br/>                               | Stellt ein Diskettenlaufwerk innerhalb des virtuellen Computers dar.<br/>                                                                                                                                                  |
| [**Msvm \_ DVDDrive**](msvm-dvddrive.md)<br/>                                         | Stellt ein DVD-Laufwerk innerhalb eines virtuellen Computers dar.<br/>                                                                                                                                                    |
| [**Msvm \_ IDEController**](msvm-idecontroller.md)<br/>                               | Stellt einen IDE-Controller dar.<br/>                                                                                                                                                                          |
| [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)<br/>             | Verwaltet die virtuellen Medien (VHD-, VHDX-, ISO- oder VFD-Dateien) für einen virtuellen Computer.<br/>                                                                                                                    |
| [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md)<br/>                                   | Stellt Speicherlaufwerkmedien dar und wird zum Auffüllen der Speicherlaufwerke verwendet.<br/>                                                                                                                             |
| [**Msvm \_ MediaPresent**](msvm-mediapresent.md)<br/>                                 | Ordnet dem in das Laufwerk eingefügten Medium ein Speicherlaufwerk zu.<br/>                                                                                                                                     |
| [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md)<br/>                   | Stellt ausführliche Informationen zu einem manuell bereitgestellten Speicherimage zur Verfügung.<br/>                                                                                                                                  |
| [**Msvm \_ ProtocolControllerForUnit**](msvm-protocolcontrollerforunit.md)<br/>       | Diese Zuordnung gibt an, dass eine Unterklasse eines logischen Geräts (z. B. ein Speichervolumen) über einen bestimmten Protokollcontroller verbunden ist.<br/>                                                       |
| [**Msvm \_ SCSIProtocolController**](msvm-scsiprotocolcontroller.md)<br/>             | Stellt einen synthetischen SCSI-Controller dar.<br/>                                                                                                                                                                |
| [**Msvm \_ StorageAlert**](msvm-storagealert.md)<br/>                                 | Stellt ein Ereignis dar, das jedes Mal ausgelöst wird, wenn sich die **OperationalStatus-Eigenschaft** der [**Msvm \_ ResourcePool-**](msvm-resourcepool.md) oder [**Msvm \_ LogicalDisk-Klasse**](msvm-logicaldisk.md) ändert.<br/> |
| [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)<br/> | Stellt Einstellungen dar, die sich speziell auf die Zuordnung des virtuellen Speichers bezieht.<br/>                                                                                                                         |
| [**Msvm \_ StorageJob**](msvm-storagejob.md)<br/>                                     | Stellt einen Speichervorgangauftrag dar, der vom Microsoft Hyper-V Image Management Service erstellt wurde.<br/>                                                                                                          |
| [**Msvm \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md)<br/>     | Stellt Einstellungsdaten für eine virtuelle Festplatte zur<br/>                                                                                                                                                         |
| [**Msvm \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md)<br/>                 | Stellt Statusinformationen für ein vorhandenes Image einer virtuellen Festplatte zur Verfügung.<br/>                                                                                                                                    |



 

 

 




