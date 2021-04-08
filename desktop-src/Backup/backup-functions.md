---
title: Sicherungsfunktionen
description: Die folgenden Funktionen werden bei der Bandsicherung verwendet.
ms.assetid: 8c5f92f7-4918-475c-bc86-2b02291488d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312c7477c28f83b7c1c64073234799219346f89a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728920"
---
# <a name="backup-functions"></a>Sicherungsfunktionen

Die folgenden Funktionen werden bei der [Bandsicherung](tape-backup.md)verwendet.



| Funktion                                           | BESCHREIBUNG                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread)                   | Liest Daten, die einer angegebenen Datei oder einem angegebenen Verzeichnis zugeordnet sind, in einem Puffer.                                |
| [**BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek)                   | Sucht in einem Datenstrom nach vorne.                                                                        |
| [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)                 | Schreibt einen Datenstrom aus einem Puffer in eine angegebene Datei oder ein angegebenes Verzeichnis.                                |
| [**"Kreatetapeer Partition"**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) | Formatiert ein Band neu.                                                                                      |
| [**Erasetape**](/windows/desktop/api/Winbase/nf-winbase-erasetape)                     | Löscht den gesamten oder einen Teil eines Bands.                                                                          |
| [**Gettapeparameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters)     | Ruft Informationen ab, die das Band oder das Bandlaufwerk beschreiben.                                       |
| [**Gettapeposition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition)         | Ruft die aktuelle Adresse des Bands ab.                                                             |
| [**Gettapestatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus)             | Bestimmt, ob das Bandgerät für die Verarbeitung von Band Befehlen bereit ist.                                  |
| [**Preparetape**](/windows/desktop/api/Winbase/nf-winbase-preparetape)                 | Bereitet das Band vor, auf das zugegriffen werden soll.                                                           |
| [**Settapeparameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)     | Gibt die Blockgröße eines Bands an oder konfiguriert das Bandgerät.                                      |
| [**Settapeposition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition)         | Legt die Band Position auf dem angegebenen Gerät fest.                                                        |
| [**Schreibtapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark)             | Schreibt eine angegebene Anzahl von Datei Markierungen, setmarkierungen, kurzen Datei Markierungen oder langen Datei Markierungen in ein Bandgerät. |



 

Die folgenden Funktionen werden für die Arbeit mit [Einzelinstanzspeicher und SIS-Sicherung](single-instance-store-and-sis-backup.md)bereitgestellt.



| Funktion                                                          | BESCHREIBUNG                                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**Siscreatebackupstructure**](siscreatebackupstructure.md)      | Erstellt die angegebene SIS-Sicherungs Struktur basierend auf den bereitgestellten Informationen.                      |
| [**Siscreaterestorestruktur**](siscreaterestorestructure.md)    | Erstellt die angegebene SIS-Wiederherstellungs Struktur basierend auf den angegebenen Informationen.                     |
| [**Siscsfilestobackupforlink**](siscsfilestobackupforlink.md)    | Gibt Informationen zurück, die die gemeinsamen Speicherdateien beschreiben, auf die der angegebene SIS-Link verweist.            |
| [**Sisfrezuden Speicher**](sisfreeallocatedmemory.md)          | Gibt durch SIS-API-Funktionen zugeordnete Speicher frei.                                                       |
| [**Sisfrebackupstructure**](sisfreebackupstructure.md)          | Gibt die angegebene SIS-Sicherungs Struktur frei.                                                          |
| [**Sisfreerestorestruktur**](sisfreerestorestructure.md)        | Gibt die angegebene SIS-Wiederherstellungs Struktur frei.                                                         |
| [**Sisrestoredcommon StoreFile**](sisrestoredcommonstorefile.md) | Meldet an die SIS-Architektur, dass eine Common Store-Datei geschrieben wurde.                         |
| [**Sisrestoredlink**](sisrestoredlink.md)                        | Gibt die Namen der Datei des Common Stores oder der Dateien zurück, auf die der angegebene wiederhergestellte SIS-Link verweist. |



 

Die folgenden Funktionen werden für die Arbeit mit [der Sicherung und Wiederherstellung verschlüsselter Dateien](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files)bereitgestellt.



| Funktion                                                | BESCHREIBUNG                                                                                |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Closeverschlüsseltedfileraw**](/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw) | Schließen Sie eine verschlüsselte Datei, die mit [**openverschlüsseltedfileraw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa)geöffnet wurde. |
| [**Openverschlüsseltedfileraw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa)   | Öffnen Sie eine verschlüsselte Datei mit Zugriff auf Daten in verschlüsselter Form.                            |
| [**"Read verschlüsseltedfileraw"**](/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw)   | Lesen Sie eine verschlüsselte Datei, die Ihre Daten in verschlüsseltem Format verlässt.                               |
| [**"Write teencryptedfileraw"**](/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw) | Schreiben Sie eine verschlüsselte Datei, indem Sie Ihre Daten in verschlüsseltem Format belassen.                              |



 

 

 