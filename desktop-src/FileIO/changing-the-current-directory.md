---
description: Eine Anwendung kann das aktuelle Verzeichnis ändern, indem Sie die Funktion SetCurrentDirectory aufruft.
ms.assetid: b08e7739-55d4-4690-9ce5-2a8cb29214e9
title: Ändern des aktuellen Verzeichnisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e507d206bcd988a7c00f557bde2b8a0ad39c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354010"
---
# <a name="changing-the-current-directory"></a>Ändern des aktuellen Verzeichnisses

Das Verzeichnis am Ende des aktiven Pfads wird als Aktuelles Verzeichnis bezeichnet. Dabei handelt es sich um das Verzeichnis, in dem die aktive Anwendung gestartet wurde, sofern Sie nicht explizit geändert wurde. Eine Anwendung kann ermitteln, welches Verzeichnis aktuell ist, indem Sie die [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) -Funktion aufrufen. Es ist manchmal notwendig, die [**getfullpathname**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) -Funktion zu verwenden, um sicherzustellen, dass der Laufwerk Buchstabe enthalten ist, wenn Sie von der Anwendung benötigt wird.

> [!Note]  
> Obwohl jeder Prozess nur über ein aktuelles Verzeichnis verfügen kann, speichert das System den letzten aktuellen Pfad für jedes Volume (Laufwerk Buchstabe), wenn die Anwendung Volumes mithilfe der [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) -Funktion schaltet. Dieses Verhalten wird nur dann selbst bei der Angabe eines Laufwerk Buchstabens ohne einen voll qualifizierten Pfad angezeigt, wenn der aktuelle Verzeichnis Verweis auf ein anderes Volume geändert wird. Dies gilt für Get-oder Set-Vorgänge.

 

Eine Anwendung kann das aktuelle Verzeichnis ändern, indem Sie die Funktion [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) aufruft.

Im folgenden Beispiel wird die Verwendung von [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) und [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)veranschaulicht.


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>

#define BUFSIZE MAX_PATH
 
void _tmain(int argc, TCHAR **argv) 
{ 
   TCHAR Buffer[BUFSIZE];
   DWORD dwRet;

   if(argc != 2)
   {
      _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
      return;
   }

   dwRet = GetCurrentDirectory(BUFSIZE, Buffer);

   if( dwRet == 0 )
   {
      printf("GetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   if(dwRet > BUFSIZE)
   {
      printf("Buffer too small; need %d characters\n", dwRet);
      return;
   }

   if( !SetCurrentDirectory(argv[1]))
   {
      printf("SetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   _tprintf(TEXT("Set current directory to %s\n"), argv[1]);

   if( !SetCurrentDirectory(Buffer) )
   {
      printf("SetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   _tprintf(TEXT("Restored previous directory (%s)\n"), Buffer);
}
```



 

 



