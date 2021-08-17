---
description: Jedes Mal, wenn ein Prozess ein Verzeichnisobjekt erstellt oder öffnet, empfängt er ein Handle für das -Objekt.
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: Verzeichnishandles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc8f983748154a781e5dd2923e0c3e3351a26acb47c2230d3142d6ad6444513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015219"
---
# <a name="directory-handles"></a>Verzeichnishandles

Jedes Mal, wenn ein Prozess ein Verzeichnisobjekt erstellt oder öffnet, empfängt er ein Handle für das -Objekt.

Um ein Handle für ein vorhandenes Verzeichnis abzurufen, rufen Sie die [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) mit dem **FLAG FILE FLAG BACKUP \_ \_ \_ SEMANTICS auf.**

Sie können ein Verzeichnishandle an die folgenden Funktionen übergeben.



| Funktion                                                         | Beschreibung                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread)                              | Sichern Sie eine Datei oder ein Verzeichnis, einschließlich der Sicherheitsinformationen.<br/>                                                                                      |
| [**BackupSeek**](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | Sucht in einem Datenstrom, auf den ursprünglich zugegriffen wird, mithilfe der [**BackupRead-**](/windows/desktop/api/winbase/nf-winbase-backupread) oder [**BackupWrite-Funktion.**](/windows/desktop/api/winbase/nf-winbase-backupwrite)<br/> |
| [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | Stellen Sie eine Datei oder ein Verzeichnis wieder her, die bzw. das mit [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread)gesichert wurde.<br/>                                                             |
| [**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | Ruft Dateiinformationen für die angegebene Datei ab.<br/>                                                                                                    |
| [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | Ruft die Größe der angegebenen Datei in Bytes ab.<br/>                                                                                                   |
| [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Ruft das Datum und die Uhrzeit der Erstellung, des letzten Zugriffs und der letzten Änderung einer Datei oder eines Verzeichnisses ab.<br/>                                                   |
| [**GetFileType**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | Ruft den Dateityp der angegebenen Datei ab.<br/>                                                                                                        |
| [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | Ruft Informationen ab, die die Änderungen im angegebenen Verzeichnis beschreiben.<br/>                                                                      |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Legt das Datum und die Uhrzeit der Erstellung, des letzten Zugriffs oder der letzten Änderung der angegebenen Datei oder des angegebenen Verzeichnisses fest.<br/>                                             |



 

 

