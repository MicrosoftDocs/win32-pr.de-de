---
title: Sicherungsfunktionen
description: Die folgenden Funktionen werden bei der Bandsicherung verwendet.
ms.assetid: 8c5f92f7-4918-475c-bc86-2b02291488d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2164958d7261c4c22caf1ac5124f524eca2f7ed355b082bede59d66a2e6fe697
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529610"
---
# <a name="backup-functions"></a>Sicherungsfunktionen

Die folgenden Funktionen werden bei der [Bandsicherung verwendet.](tape-backup.md)



| Funktion                                           | Beschreibung                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread)                   | Liest Daten, die einer angegebenen Datei oder einem angegebenen Verzeichnis zugeordnet sind, in einen Puffer ein.                                |
| [**BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek)                   | Sucht vorwärts in einem Datenstrom.                                                                        |
| [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)                 | Schreibt einen Datenstrom aus einem Puffer in eine angegebene Datei oder ein angegebenes Verzeichnis.                                |
| [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) | Ein Band wird neu gebändert.                                                                                      |
| [**EraseTape**](/windows/desktop/api/Winbase/nf-winbase-erasetape)                     | Löscht ein Band ganz oder teilweise.                                                                          |
| [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters)     | Ruft Informationen ab, die das Band oder bandlaufwerk beschreiben.                                       |
| [**GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition)         | Ruft die aktuelle Adresse des Bandes ab.                                                             |
| [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus)             | Bestimmt, ob das Bandgerät für die Verarbeitung von Bandbefehlen bereit ist.                                  |
| [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape)                 | Bereitet das Band für den Zugriff oder das Entfernen vor.                                                           |
| [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)     | Gibt die Blockgröße eines Bandes an oder konfiguriert das Bandgerät.                                      |
| [**SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition)         | Legt die Bandposition auf dem angegebenen Gerät fest.                                                        |
| [**WriteTapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark)             | Schreibt eine angegebene Anzahl von Dateimarks, Setmarks, kurzen Dateimarks oder langen Dateimarks auf ein Bandgerät. |



 

Die folgenden Funktionen werden für die Arbeit mit dem Einzelinstanzspeicher und [der SIS-Sicherung bereitgestellt.](single-instance-store-and-sis-backup.md)



| Funktion                                                          | Beschreibung                                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**SisCreateBackupStructure**](siscreatebackupstructure.md)      | Erstellt die angegebene SIS-Sicherungsstruktur basierend auf den angegebenen Informationen.                      |
| [**SisCreateRestoreStructure**](siscreaterestorestructure.md)    | Erstellt die angegebene SIS-Wiederherstellungsstruktur basierend auf den angegebenen Informationen.                     |
| [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)    | Gibt Informationen zurück, die die Common Store-Dateien beschreiben, auf die der angegebene SIS-Link verweist.            |
| [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)          | Gibt von SIS-API-Funktionen zugeordneten Arbeitsspeicher frei.                                                       |
| [**SisFreeBackupStructure**](sisfreebackupstructure.md)          | Gibt die angegebene SIS-Sicherungsstruktur frei.                                                          |
| [**SisFreeRestoreStructure**](sisfreerestorestructure.md)        | Gibt die angegebene SIS-Wiederherstellungsstruktur frei.                                                         |
| [**SisRestoredCommon StoreFile**](sisrestoredcommonstorefile.md) | Meldet der SIS-Architektur, dass eine Common Store-Datei geschrieben wurde.                         |
| [**SisRestoredLink**](sisrestoredlink.md)                        | Gibt die Namen der Common Store-Datei oder der Dateien zurück, auf die der angegebene wiederhergestellte SIS-Link verweist. |



 

Die folgenden Funktionen werden für die Arbeit mit der Sicherung [und Wiederherstellung verschlüsselter Dateien bereitgestellt.](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files)



| Funktion                                                | Beschreibung                                                                                |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CloseEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw) | Schließen Sie eine verschlüsselte Datei, die mit [**OpenEncryptedFileRaw geöffnet wurde.**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa) |
| [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa)   | Öffnen Sie eine verschlüsselte Datei mit Zugriff auf Daten im verschlüsselten Format.                            |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw)   | Liest eine verschlüsselte Datei, die ihre Daten im verschlüsselten Format belässt.                               |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw) | Schreiben einer verschlüsselten Datei, die ihre Daten im verschlüsselten Format belässt.                              |



 

 

 