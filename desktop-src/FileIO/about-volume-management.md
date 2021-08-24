---
description: Volumes werden von einem Gerätetreiber implementiert, der als Volume-Manager bezeichnet wird.
ms.assetid: 424ddbd9-5692-45ef-95fb-7b00b09e3205
title: Informationen zur Volumeverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5446726b7caf448eef74884e8b6afc9d27dc4d4fdc6ffadd4572e667aaeb2cf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766310"
---
# <a name="about-volume-management"></a>Informationen zur Volumeverwaltung

Volumes werden von einem Gerätetreiber implementiert, der als Volume-Manager bezeichnet wird. Beispiele hierfür sind FtDisk Manager, Logical Disk Manager (LDM) und VERITAS Logical Volume Manager (LVM). Volume-Manager bieten eine Ebene der physischen Abstraktion, des Datenschutzes (mithilfe einer Form von RAID) und der Leistung.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                       | Beschreibung                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Dateisystemerkennung](file-system-recognition.md)<br/>           | Ziel der Dateisystemerkennung ist es, dem Windows-Betriebssystem eine zusätzliche Option für ein gültiges, aber nicht unbekanntes Dateisystem als "RAW" zu ermöglichen.<br/>                                                                                                         |
| [Benennen eines Volumes](naming-a-volume.md)<br/>                           | Eine Bezeichnung ist ein benutzerfreundlicher Name, der einem Volume zugewiesen wird, in der Regel von einem Endbenutzer, damit es leichter zu erkennen ist. Ein Volume kann eine Bezeichnung, einen Laufwerkbuchstaben, beides oder keines von beiden haben. Verwenden Sie zum Festlegen der Bezeichnung für ein Volume die [**Funktion SetVolumeLabel.**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela)<br/> |
| [Aufzählen von Volumes](enumerating-volumes.md)<br/>                   | Um eine vollständige Liste der Volumes auf einem Computer zu erstellen oder jedes Volume nacheinander zu bearbeiten, können Sie Volumes auflisten.<br/>                                                                                                                                                       |
| [Abrufen von Volumeinformationen](obtaining-volume-information.md)<br/> | Bevor Sie auf Dateien und Verzeichnisse auf einem bestimmten Volume zugreifen, sollten Sie die Funktionen des Dateisystems mithilfe der [**GetVolumeInformation-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) bestimmen.<br/>                                                                              |
| [Change-Journal](change-journals.md)<br/>                           | Wenn eine Änderung an einer Datei oder einem Verzeichnis auf einem Volume vorgenommen wird, wird das USN-Änderungsjournal für dieses Volume mit einer Beschreibung der Änderung und dem Namen der Datei oder des Verzeichnisses aktualisiert.<br/>                                                                                        |
| [Bereitgestellte Ordner](volume-mount-points.md)<br/>                       | Mithilfe von bereitgestellten Ordnern können Sie unterschiedliche Dateisysteme wie das NTFS-Dateisystem, ein 16-Bit-FAT-Dateisystem und ein ISO-9660-Dateisystem auf einem CD-ROM-Laufwerk in einem logischen Dateisystem auf einem einzelnen NTFS-Volume vereinheitlichen.<br/>                                                      |
| [Masterdateitabelle](master-file-table.md)<br/>                       | Alle Informationen zu einer Datei, einschließlich Größe, Zeit- und Datumsstempel, Berechtigungen und Dateninhalt, werden entweder in MFT-Einträgen (Master File Table) oder außerhalb des MFT-Platzes gespeichert, der von MFT-Einträgen beschrieben wird.<br/>                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Basic Disks and Volumes Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Dynamic Disks and Volumes Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Referenz zur Volumeverwaltung](volume-management-reference.md)
</dt> </dl>

 

