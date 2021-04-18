---
description: 'Die Speicher Objekte sind in drei Typen unterteilt: Controller, Laufwerke und Medien.'
ms.assetid: CF38F6E8-A43D-4A97-8055-6B17E323524C
title: Speicherklassen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0c17ad2530a86e7f404fe19eaeb3ef5a1cd7895
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352667"
---
# <a name="storage-classes"></a>Speicherklassen

Die Speicher Objekte sind in drei Typen unterteilt: Controller, Laufwerke und Medien.

Es gibt zwei Controller, einen emulierten IDE-Controller und einen synthetischen SCSI-Controller. Beide Controller unterstützen die Anlage von Laufwerken, die die Medien hosten.

Im folgenden finden Sie WMI-Klassen für die Virtualisierung in Bezug auf den Speicher. Es wird auch die Unterstützung synthetischer Disketten Medien unterstützt. Das Anfügen an ein physisches Diskettenlaufwerk wird nicht unterstützt.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                      | BESCHREIBUNG                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSVM \_ affectedstoragejobelements**](msvm-affectedstoragejobelement.md)<br/>       | Stellt die Zuordnung zwischen einem Auftrag und den verwalteten Elementen dar, die von seiner Ausführung betroffen sein können.<br/>                                                                                               |
| [**MSVM- \_ BasedOn**](msvm-basedon.md)<br/>                                           | Eine Zuordnung, die beschreibt, wie Speicherblöcke aus Blöcken auf niedrigerer Ebene zusammengestellt werden können.<br/>                                                                                                           |
| [**MSVM \_ controlledby**](msvm-controlledby.md)<br/>                                 | Ordnet dem Speichercontroller, der das Gerät besitzt, ein Speichergerät zu.<br/>                                                                                                                          |
| [**MSVM \_ diskdrive**](msvm-diskdrive.md)<br/>                                       | Stellt ein Festplattenlaufwerk innerhalb eines virtuellen Computers dar.<br/>                                                                                                                                              |
| [**MSVM \_ diskettecontroller**](msvm-diskettecontroller.md)<br/>                     | Stellt den Disketten Controller auf dem virtuellen Computer dar.<br/>                                                                                                                                               |
| [**MSVM \_ diskettedrive**](msvm-diskettedrive.md)<br/>                               | Stellt ein Diskettenlaufwerk innerhalb des virtuellen Computers dar.<br/>                                                                                                                                                  |
| [**MSVM \_ dvddrive**](msvm-dvddrive.md)<br/>                                         | Stellt ein DVD-Laufwerk innerhalb eines virtuellen Computers dar.<br/>                                                                                                                                                    |
| [**MSVM- \_ idecontroller**](msvm-idecontroller.md)<br/>                               | Stellt einen IDE-Controller dar.<br/>                                                                                                                                                                          |
| [**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md)<br/>             | Verwaltet die virtuellen Medien (VHD-, vhdx-, ISO-oder VFD-Dateien) für eine virtuelle Maschine.<br/>                                                                                                                    |
| [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md)<br/>                                   | Stellt Speicher Laufwerk Medien dar und wird verwendet, um die Speicher Laufwerke aufzufüllen.<br/>                                                                                                                             |
| [**MSVM \_ mediapresent**](msvm-mediapresent.md)<br/>                                 | Ordnet ein Speicher Laufwerk den Medien zu, die in das Laufwerk eingefügt werden.<br/>                                                                                                                                     |
| [**MSVM \_ mountedstorageimage**](msvm-mountedstorageimage.md)<br/>                   | Stellt ausführliche Informationen über ein manuell eingebundenes Speicher Abbild bereit.<br/>                                                                                                                                  |
| [**MSVM \_ protocolcontrollerforunit**](msvm-protocolcontrollerforunit.md)<br/>       | Diese Zuordnung gibt an, dass eine Unterklasse des logischen Geräts (z. b. ein Speicher Volume) über einen bestimmten Protokoll Controller verbunden ist.<br/>                                                       |
| [**MSVM \_ scsiprotocolcontroller**](msvm-scsiprotocolcontroller.md)<br/>             | Stellt einen synthetischen SCSI-Controller dar.<br/>                                                                                                                                                                |
| [**MSVM \_ storagealert**](msvm-storagealert.md)<br/>                                 | Stellt ein Ereignis dar, das jedes Mal ausgelöst wird, wenn sich die **OperationalStatus** -Eigenschaft der [**MSVM \_ resourcepool**](msvm-resourcepool.md) -Klasse oder der [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md) -Klasse ändert.<br/> |
| [**MSVM \_ storagezugecationsettingdata**](msvm-storageallocationsettingdata.md)<br/> | Stellt Einstellungen dar, die sich speziell auf die Zuordnung des virtuellen Speichers beziehen.<br/>                                                                                                                         |
| [**MSVM \_ storagejob**](msvm-storagejob.md)<br/>                                     | Stellt einen Speicher Vorgangs Auftrag dar, der vom Microsoft Hyper-V Abbild Verwaltungsdienst erstellt wurde.<br/>                                                                                                          |
| [**MSVM \_ virtualharddisksettingdata**](msvm-virtualharddisksettingdata.md)<br/>     | Stellt Einstellungsdaten für eine virtuelle Festplatte bereit.<br/>                                                                                                                                                         |
| [**MSVM \_ virtualharddiskstate**](msvm-virtualharddiskstate.md)<br/>                 | Stellt Zustandsinformationen für ein vorhandenes virtuelles Festplatten Abbild bereit.<br/>                                                                                                                                    |



 

 

 




