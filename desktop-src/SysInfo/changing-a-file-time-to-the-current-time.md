---
description: Im folgenden Beispiel wird die Zeit für den letzten Schreibvorgang für eine Datei mithilfe der SetFileTime-Funktion auf die aktuelle Systemzeit festgelegt.
ms.assetid: b4a70c01-d5ce-47e8-9918-9c9176894240
title: Ändern der Uhrzeit der Datei in die aktuelle Zeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3d4b6189514196c5f8a332c259da9f8f8d7417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960995"
---
# <a name="changing-a-file-time-to-the-current-time"></a>Ändern der Uhrzeit der Datei in die aktuelle Zeit

Im folgenden Beispiel wird die Zeit für den letzten Schreibvorgang für eine Datei mithilfe der [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) -Funktion auf die aktuelle Systemzeit festgelegt.

Das NTFS-Dateisystem speichert Zeitwerte im UTC-Format, sodass Sie von Änderungen in der Zeitzone oder der Sommerzeit nicht betroffen sind. Das FAT-Dateisystem speichert Zeitwerte basierend auf der lokalen Zeit des Computers.

Die Datei muss mit der Funktion " [**fiatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " unter Verwendung des Zugriffs auf Datei \_ Schreib Attribute geöffnet werden \_ .


```C++
#include <windows.h>

// SetFileToCurrentTime - sets last write time to current system time
// Return value - TRUE if successful, FALSE otherwise
// hFile  - must be a valid file handle

BOOL SetFileToCurrentTime(HANDLE hFile)
{
    FILETIME ft;
    SYSTEMTIME st;
    BOOL f;

    GetSystemTime(&st);              // Gets the current system time
    SystemTimeToFileTime(&st, &ft);  // Converts the current system time to file time format
    f = SetFileTime(hFile,           // Sets last-write time of the file 
        (LPFILETIME) NULL,           // to the converted current system time 
        (LPFILETIME) NULL, 
        &ft);    

    return f;
}
```



 

 
