---
description: Volumes werden von einem Gerätetreiber implementiert, der als Volumemanager bezeichnet wird.
ms.assetid: 424ddbd9-5692-45ef-95fb-7b00b09e3205
title: Informationen zur Volumeverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0767d137eeecaa4ded060382b689b5ea3780dcbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351059"
---
# <a name="about-volume-management"></a>Informationen zur Volumeverwaltung

Volumes werden von einem Gerätetreiber implementiert, der als Volumemanager bezeichnet wird. Beispiele hierfür sind der Ftdisk-Manager, der Logical Disk Manager (LDM) und der Veritas Logical Volume Manager (LVM). Volumemanager bieten eine Schicht physischer Abstraktion, Datenschutz (mit einer Form von RAID) und Leistung.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Datei System Erkennung](file-system-recognition.md)<br/>           | Das Ziel der Dateisystem Erkennung besteht darin, dass das Windows-Betriebssystem über eine zusätzliche Option für ein gültiges, aber unbekanntes Dateisystem als "RAW" verfügt.<br/>                                                                                                         |
| [Benennen eines Volumes](naming-a-volume.md)<br/>                           | Eine Bezeichnung ist ein benutzerfreundlicher Name, der einem Volume zugewiesen wird, normalerweise von einem Endbenutzer, um die Erkennung zu vereinfachen. Ein Volume kann eine Bezeichnung, einen Laufwerk Buchstaben, beides oder keines von beiden aufweisen. Um die Bezeichnung für ein Volume festzulegen, verwenden Sie die Funktion [**setvolumelabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) .<br/> |
| [Auflisten von Volumes](enumerating-volumes.md)<br/>                   | Zum Erstellen einer kompletten Liste der Volumes auf einem Computer oder zum Bearbeiten der einzelnen Volumes können Sie Volumes auflisten.<br/>                                                                                                                                                       |
| [Abrufen von Volumeinformationen](obtaining-volume-information.md)<br/> | Vor dem Zugriff auf Dateien und Verzeichnisse auf einem bestimmten Volume sollten Sie die Funktionen des Dateisystems mithilfe der [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion ermitteln.<br/>                                                                              |
| [Ändern von Journalen](change-journals.md)<br/>                           | Wenn eine Änderung an einer Datei oder einem Verzeichnis in einem Volume vorgenommen wird, wird das Änderungs Journal für die Aktualisierung des Volumes mit einer Beschreibung der Änderung und des Datei-oder Verzeichnis namens aktualisiert.<br/>                                                                                        |
| [Eingebundene Ordner](volume-mount-points.md)<br/>                       | Mithilfe bereitgestellter Ordner können Sie unterschiedliche Dateisysteme wie das NTFS-Dateisystem, ein 16-Bit-FAT-Dateisystem und ein ISO-9660-Dateisystem auf einem CD-ROM-Laufwerk in einem logischen Dateisystem auf einem einzelnen NTFS-Volume vereinheitlichen.<br/>                                                      |
| [Master Dateitabelle](master-file-table.md)<br/>                       | Alle Informationen zu einer Datei, einschließlich Größe, Zeit-und Datumsstempel, Berechtigungen und Dateninhalt, werden entweder in MFT-Einträgen (Master File Table) oder außerhalb des in der MFT-Einträge beschriebenen Speicherplatzes gespeichert.<br/>                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Technische Referenz zu einfachen Datenträgern und Volumes](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Technische Referenz zu dynamischen Datenträgern und Volumes](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Referenz zur Volumeverwaltung](volume-management-reference.md)
</dt> </dl>

 

