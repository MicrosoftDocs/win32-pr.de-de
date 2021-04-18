---
description: Wenn ein Prozess ein Verzeichnis Objekt erstellt oder öffnet, empfängt es ein Handle für das Objekt.
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: Verzeichnis Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4215a75622a7fa35ee36d45e769736bf1224a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366301"
---
# <a name="directory-handles"></a>Verzeichnis Handles

Wenn ein Prozess ein Verzeichnis Objekt erstellt oder öffnet, empfängt es ein Handle für das Objekt.

Um ein Handle für ein vorhandenes Verzeichnis zu erhalten, rufen Sie [**die Funktion "**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Funktion" mit dem **Dateiflag für die \_ \_ Sicherungs \_ Semantik** auf.

Sie können ein Verzeichnis Handle an die folgenden Funktionen übergeben.



| Funktion                                                         | BESCHREIBUNG                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread)                              | Sichern Sie eine Datei oder ein Verzeichnis, einschließlich der Sicherheitsinformationen.<br/>                                                                                      |
| [**BackupSeek**](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | Forward-Forward in einem Datenstrom, auf den zunächst mithilfe der [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) -Funktion oder der [**Backup Write**](/windows/desktop/api/winbase/nf-winbase-backupwrite) -Funktion zugegriffen wurde.<br/> |
| [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | Stellen Sie eine mit [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread)gesicherte Datei oder ein Verzeichnis wieder her.<br/>                                                             |
| [**Getfileingeformationbyhandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | Ruft Dateiinformationen für die angegebene Datei ab.<br/>                                                                                                    |
| [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | Ruft die Größe der angegebenen Datei in Bytes ab.<br/>                                                                                                   |
| [**' GetFileTime '**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Ruft das Datum und die Uhrzeit der Erstellung einer Datei oder eines Verzeichnisses, des letzten Zugriffs und der letzten Änderung ab.<br/>                                                   |
| [**Getfiletype**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | Ruft den Dateityp der angegebenen Datei ab.<br/>                                                                                                        |
| [**"Read directoriychangesw"**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | Ruft Informationen ab, die die Änderungen im angegebenen Verzeichnis beschreiben.<br/>                                                                      |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Legt das Datum und die Uhrzeit fest, zu der die angegebene Datei bzw. das angegebene Verzeichnis erstellt, auf den zuletzt zugegriffen wurde, oder zuletzt geändert<br/>                                             |



 

 

