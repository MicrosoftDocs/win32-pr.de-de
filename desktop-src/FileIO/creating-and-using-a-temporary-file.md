---
description: Beispielcode, der zeigt, wie eine temporäre Datei zu Datenbearbeitungszwecken mithilfe der Funktionen GetTempFileName und GetTempPath erstellt wird.
ms.assetid: 6254c67d-5d34-499d-b1a4-8cac526dd294
title: Erstellen und Verwenden einer temporären Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f242b9b021744c42e7e1b8745c7eec2b6388249246872192ecfd6308bdab55af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650420"
---
# <a name="creating-and-using-a-temporary-file"></a>Erstellen und Verwenden einer temporären Datei

Anwendungen können eindeutige Datei- und Pfadnamen für temporäre Dateien mithilfe der [**Funktionen GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) und [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) abrufen. Die **GetTempFileName-Funktion** generiert einen eindeutigen Dateinamen, und die **GetTempPath-Funktion** ruft den Pfad zu einem Verzeichnis ab, in dem temporäre Dateien erstellt werden sollen.

Im folgenden Verfahren wird beschrieben, wie eine Anwendung eine temporäre Datei zu Datenbearbeitungszwecken erstellt.

**So erstellen und verwenden Sie eine temporäre Datei**

1.  Die Anwendung öffnet die vom Benutzer bereitgestellte Quelltextdatei mithilfe von [**CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
2.  Die Anwendung ruft einen temporären Dateipfad und Dateinamen mithilfe der [**Funktionen GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) und [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) ab und verwendet [**dann CreateFile,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) um die temporäre Datei zu erstellen.
3.  Die Anwendung liest Textdatenblöcke in einen Puffer, konvertiert den Pufferinhalt mithilfe der [CharUpperBuffA-Funktion](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in Großbuchstaben und schreibt den konvertierten Puffer in die temporäre Datei.
4.  Wenn alle Quelldateien in die temporäre Datei geschrieben werden, schließt die Anwendung beide Dateien und benennt die temporäre Datei mithilfe der [**MoveFileEx-Funktion**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) in "allcaps.txt" um.

Jeder der vorherigen Schritte wird auf Erfolg überprüft, bevor mit dem nächsten Schritt fortbeschrieben wird. Im Fall eines Fehlers wird eine Fehlerbeschreibung angezeigt. Die Anwendung wird sofort beendet, nachdem die Fehlermeldung angezeigt wurde.

Beachten Sie, dass die Bearbeitung von Textdateien nur aus Demonstrationszwecken ausgewählt wurde und durch alle gewünschten erforderlichen Datenbearbeitungsprozeduren ersetzt werden kann. Die Datendatei kann einen beliebigen Datentyp haben, nicht nur Text.

Die [**GetTempPath-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) ruft eine vollqualifizierte Pfadzeichenfolge aus einer Umgebungsvariablen ab, überprüft jedoch nicht im Voraus, ob der Pfad oder die entsprechenden Zugriffsrechte für diesen Pfad vorliegen. Dies liegt in der Verantwortung des Anwendungsentwicklers. Weitere Informationen finden Sie unter [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha). Im folgenden Beispiel wird ein Fehler als Terminalbedingung betrachtet, und die Anwendung wird beendet, nachdem eine beschreibende Meldung an die Standardausgabe gesendet wurde. Es gibt jedoch viele andere Optionen, z. B. die Aufforderung des Benutzers zur Eingabe eines temporären Verzeichnisses oder einfach den Versuch, das aktuelle Verzeichnis zu verwenden.

> [!Note]  
> Die [**GetTempFileName-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) erfordert nicht, dass die [**GetTempPath-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) verwendet wird.

 

Das folgende C++-Beispiel zeigt, wie Sie eine temporäre Datei zu Datenbearbeitungszwecken erstellen.


```C++
//
//  This application opens a file specified by the user and uses
//  a temporary file to convert the file to upper case letters.
//  Note that the given source file is assumed to be an ASCII text file
//  and the new file created is overwritten each time the application is
//  run.
//

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE 1024

void PrintError(LPCTSTR errDesc);

int _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile     = INVALID_HANDLE_VALUE;
    HANDLE hTempFile = INVALID_HANDLE_VALUE; 

    BOOL fSuccess  = FALSE;
    DWORD dwRetVal = 0;
    UINT uRetVal   = 0;

    DWORD dwBytesRead    = 0;
    DWORD dwBytesWritten = 0; 

    TCHAR szTempFileName[MAX_PATH];  
    TCHAR lpTempPathBuffer[MAX_PATH];
    char  chBuffer[BUFSIZE]; 

    LPCTSTR errMsg;

    if(argc != 2)
    {
        _tprintf(TEXT("Usage: %s <file>\n"), argv[0]);
        return -1;
    }

    //  Opens the existing file. 
    hFile = CreateFile(argv[1],               // file name 
                       GENERIC_READ,          // open for reading 
                       0,                     // do not share 
                       NULL,                  // default security 
                       OPEN_EXISTING,         // existing file only 
                       FILE_ATTRIBUTE_NORMAL, // normal file 
                       NULL);                 // no template 
    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        PrintError(TEXT("First CreateFile failed"));
        return (1);
    } 

     //  Gets the temp path env string (no guarantee it's a valid path).
    dwRetVal = GetTempPath(MAX_PATH,          // length of the buffer
                           lpTempPathBuffer); // buffer for path 
    if (dwRetVal > MAX_PATH || (dwRetVal == 0))
    {
        PrintError(TEXT("GetTempPath failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (2);
    }

    //  Generates a temporary file name. 
    uRetVal = GetTempFileName(lpTempPathBuffer, // directory for tmp files
                              TEXT("DEMO"),     // temp file name prefix 
                              0,                // create unique name 
                              szTempFileName);  // buffer for name 
    if (uRetVal == 0)
    {
        PrintError(TEXT("GetTempFileName failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (3);
    }

    //  Creates the new file to write to for the upper-case version.
    hTempFile = CreateFile((LPTSTR) szTempFileName, // file name 
                           GENERIC_WRITE,        // open for write 
                           0,                    // do not share 
                           NULL,                 // default security 
                           CREATE_ALWAYS,        // overwrite existing
                           FILE_ATTRIBUTE_NORMAL,// normal file 
                           NULL);                // no template 
    if (hTempFile == INVALID_HANDLE_VALUE) 
    { 
        PrintError(TEXT("Second CreateFile failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (4);
    } 

    //  Reads BUFSIZE blocks to the buffer and converts all characters in 
    //  the buffer to upper case, then writes the buffer to the temporary 
    //  file. 
    do 
    {
        if (ReadFile(hFile, chBuffer, BUFSIZE, &dwBytesRead, NULL)) 
        {
            //  Replaces lower case letters with upper case
            //  in place (using the same buffer). The return
            //  value is the number of replacements performed,
            //  which we aren't interested in for this demo.
            CharUpperBuffA(chBuffer, dwBytesRead); 

            fSuccess = WriteFile(hTempFile, 
                                 chBuffer, 
                                 dwBytesRead,
                                 &dwBytesWritten, 
                                 NULL); 
            if (!fSuccess) 
            {
                PrintError(TEXT("WriteFile failed"));
                return (5);
            }
        } 
        else
        {
            PrintError(TEXT("ReadFile failed"));
            return (6);
        }
    //  Continues until the whole file is processed.
    } while (dwBytesRead == BUFSIZE); 

    //  The handles to the files are no longer needed, so
    //  they are closed prior to moving the new file.
    if (!CloseHandle(hFile)) 
    {
       PrintError(TEXT("CloseHandle(hFile) failed"));
       return (7);
    }
    
    if (!CloseHandle(hTempFile)) 
    {
       PrintError(TEXT("CloseHandle(hTempFile) failed"));
       return (8);
    }

    //  Moves the temporary file to the new text file, allowing for differnt
    //  drive letters or volume names.
    fSuccess = MoveFileEx(szTempFileName, 
                          TEXT("AllCaps.txt"), 
                          MOVEFILE_REPLACE_EXISTING | MOVEFILE_COPY_ALLOWED);
    if (!fSuccess)
    { 
        PrintError(TEXT("MoveFileEx failed"));
        return (9);
    }
    else 
        _tprintf(TEXT("All-caps version of %s written to AllCaps.txt\n"), argv[1]);
    return (0);
}

//  ErrorMessage support function.
//  Retrieves the system error message for the GetLastError() code.
//  Note: caller must use LocalFree() on the returned LPCTSTR buffer.
LPCTSTR ErrorMessage(DWORD error) 
{ 
    LPVOID lpMsgBuf;

    FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER 
                   | FORMAT_MESSAGE_FROM_SYSTEM 
                   | FORMAT_MESSAGE_IGNORE_INSERTS,
                  NULL,
                  error,
                  MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
                  (LPTSTR) &lpMsgBuf,
                  0,
                  NULL);

    return((LPCTSTR)lpMsgBuf);
}

//  PrintError support function.
//  Simple wrapper function for error output.
void PrintError(LPCTSTR errDesc)
{
        LPCTSTR errMsg = ErrorMessage(GetLastError());
        _tprintf(TEXT("\n** ERROR ** %s: %s\n"), errDesc, errMsg);
        LocalFree((LPVOID)errMsg);
}
```



 

 
