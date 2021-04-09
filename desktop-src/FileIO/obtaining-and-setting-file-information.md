---
description: Funktionen, die verwendet werden, um Dateiinformationen zu erhalten und festzulegen.
ms.assetid: 3b5fb709-c699-4651-8072-97210c8cf763
title: Abrufen und Festlegen von Dateiinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c6eb6abf2554e1945e0782c667245ea0eaa99be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868912"
---
# <a name="obtaining-and-setting-file-information"></a>Abrufen und Festlegen von Dateiinformationen

In den folgenden Themen wird beschrieben, wie Sie Dateiinformationen erhalten und festlegen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Abrufen von Dateityp Informationen](retrieving-file-type-information.md)<br/>                               | Die [**getfiletype**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype) -Funktion Ruft den Dateityp ab: Datenträger, Zeichen (z. b. eine Konsole), Pipe oder unbekannt.<br/>                                                                                                                                               |
| [Bestimmen der Größe einer Datei](determining-the-size-of-a-file.md)<br/>                                   | Die [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) -Funktion Ruft die Größe einer Datei ab.<br/>                                                                                                                                                                                                      |
| [Suchen nach einer oder mehreren Dateien](searching-for-one-or-more-files.md)<br/>                                 | Eine Anwendung kann das aktuelle Verzeichnis nach allen Dateinamen durchsuchen, die einem bestimmten Muster entsprechen, indem die Funktionen [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**findfirstfileex**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)und [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) verwendet werden.<br/> |
| [Festlegen und erhalten des Zeitstempels einer Datei](setting-and-getting-the-timestamp-of-a-file.md)<br/>         | Anwendungen können das Datum und die Uhrzeit der Erstellung, letzten Änderung oder des letzten Zugriffs auf eine Datei mithilfe der Funktionen [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) und [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) abrufen und festlegen.<br/>                                                                         |
| [Festlegen der Codepage für den aktuellen Zeichensatz](determining-the-current-character-set-code-page.md)<br/> | Die [**arefileapisansi**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) -Funktion bestimmt, ob die Datei-e/a-Funktionen die ANSI-oder OEM-Zeichensatz-Codepage verwenden.<br/>                                                                                                                               |



 

 

