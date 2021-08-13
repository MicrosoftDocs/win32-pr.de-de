---
title: Bestimmen des Speicherorts einer Freigabe
description: Im folgenden Beispiel wird veranschaulicht, wie die WNetGetUniversalName-Funktion aufgerufen wird, um den Speicherort einer Freigabe auf einem umgeleiteten Laufwerk zu bestimmen.
ms.assetid: ce57fecb-8b14-4514-a3fd-45d7ef6eee89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a881d452c6aa9eac5eea85d4ef0e9ddce83524f001294d2a6d6d6307f5ff1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566893"
---
# <a name="determining-the-location-of-a-share"></a>Bestimmen des Speicherorts einer Freigabe

Im folgenden Beispiel wird veranschaulicht, wie die [**WNetGetUniversalName-Funktion**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) aufgerufen wird, um den Speicherort einer Freigabe auf einem umgeleiteten Laufwerk zu bestimmen.

Zuerst ruft das Codebeispiel die **WNetGetUniversalName-Funktion** auf und gibt die [**Informationsebene UNIVERSAL \_ NAME \_ INFO**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) an, um einen Zeiger auf eine Universal Naming Convention (UNC)-Namenszeichenfolge für die Ressource abzurufen. Anschließend ruft das Beispiel **WNetGetUniversalName** ein zweites Mal auf und gibt die [**Informationsebene REMOTE \_ NAME \_ INFO**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) an, um zwei zusätzliche Netzwerkverbindungsinformationszeichenfolgen abzurufen. Wenn die Aufrufe erfolgreich sind, gibt das Beispiel den Speicherort der Freigabe aus.

Führen Sie die folgenden Schritte aus, um das folgende Codebeispiel zu testen:

1.  Nennen Sie das Codebeispiel GetUni.cpp.
2.  Fügen Sie das Beispiel einer Konsolenanwendung namens GetUni hinzu.
3.  Verknüpfen Sie die Bibliotheken Shell32.lib, Mpr.lib und NetApi32.lib mit der Compilerliste der Bibliotheken.
4.  Wechseln Sie an der Eingabeaufforderung in das Verzeichnis GetUni.
5.  Kompilieren Sie GetUni.cpp.
6.  Führen Sie die Datei GetUni.exe gefolgt von einem Laufwerkbuchstaben und Doppelpunkt wie folgt aus:

    **GetUni H:\\**


```C++
#define  STRICT
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#pragma comment(lib, "mpr.lib")

#define BUFFSIZE = 1000

void main( int argc, char *argv[] )
{
  DWORD cbBuff = 1000;    // Size of Buffer
  TCHAR szBuff[1000];    // Buffer to receive information
  REMOTE_NAME_INFO  * prni = (REMOTE_NAME_INFO *)   &szBuff;
  UNIVERSAL_NAME_INFO * puni = (UNIVERSAL_NAME_INFO *) &szBuff;
  DWORD res;

  if((argc < 2) | (lstrcmp(argv[1], "/?") == 0))
  {
    printf("Syntax:  GetUni DrivePathAndFilename\n"
         "Example: GetUni U:\\WINNT\\SYSTEM32\\WSOCK32.DLL\n");
    return;
  }
  
  // Call WNetGetUniversalName with the UNIVERSAL_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using UNIVERSAL_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1],
         UNIVERSAL_NAME_INFO_LEVEL, // The structure is written to this block of memory. 
         (LPVOID) &szBuff, 
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print the location of the share, 
    //  using the pointer to UNIVERSAL_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n\n", res); 
   
  else
    _tprintf(TEXT("Universal Name: \t%s\n\n"), puni->lpUniversalName); 
    
  //
  // Call WNetGetUniversalName with the REMOTE_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using REMOTE_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1], 
         REMOTE_NAME_INFO_LEVEL, 
         (LPVOID) &szBuff,    //Structure is written to this block of memory
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print
    //  the location of the share, using 
    //  the pointer to REMOTE_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n", res); 
  else
    _tprintf(TEXT("Universal Name: \t%s\nConnection Name:\t%s\nRemaining Path: \t%s\n"),
          prni->lpUniversalName, 
          prni->lpConnectionName, 
          prni->lpRemainingPath);
  return;
}
```



 

 