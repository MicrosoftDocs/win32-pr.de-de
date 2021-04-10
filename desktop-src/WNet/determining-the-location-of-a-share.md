---
title: Bestimmen des Speicher Orts einer Freigabe
description: Im folgenden Beispiel wird veranschaulicht, wie die wnetgetuniversalname-Funktion aufgerufen wird, um den Speicherort einer Freigabe auf einem umgeleiteten Laufwerk zu ermitteln.
ms.assetid: ce57fecb-8b14-4514-a3fd-45d7ef6eee89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50c0d46e9ac2e520f7be15812b2f541fd3e588f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948947"
---
# <a name="determining-the-location-of-a-share"></a>Bestimmen des Speicher Orts einer Freigabe

Im folgenden Beispiel wird veranschaulicht, wie die [**wnetgetuniversalname**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) -Funktion aufgerufen wird, um den Speicherort einer Freigabe auf einem umgeleiteten Laufwerk zu ermitteln.

Zuerst Ruft das Codebeispiel die **wnetgetuniversalname** -Funktion auf und gibt die [**Universal \_ Name \_ Info**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) -Informationsebene an, um einen Zeiger auf eine Universal Naming Convention (UNC)-namens Zeichenfolge für die Ressource abzurufen. Im Beispiel wird **wnetgetuniversalname** ein zweites Mal aufgerufen. dabei wird die Informationsebene " [**Remote \_ Name \_ Info**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) " angegeben, um zwei zusätzliche Verbindungs Informations Zeichenfolgen für die Netzwerkverbindung abzurufen. Wenn die Aufrufe erfolgreich sind, gibt das Beispiel den Speicherort der Freigabe aus.

Um das folgende Codebeispiel zu testen, führen Sie die folgenden Schritte aus:

1.  Nennen Sie das Codebeispiel getuni. cpp.
2.  Fügen Sie das Beispiel einer Konsolenanwendung mit dem Namen getuni hinzu.
3.  Verknüpfen Sie die Bibliotheken shell32. lib, MPR. lib und Netapi32. lib mit der compilerliste der Bibliotheken.
4.  Wechseln Sie an der Eingabeaufforderung in das Verzeichnis getuni.
5.  Kompilieren Sie getuni. cpp.
6.  Führen Sie die Datei GetUni.exe gefolgt von einem Laufwerk Buchstaben und einem Doppelpunkt aus, wie hier:

    **Getuni H:\\**


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



 

 