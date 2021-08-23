---
description: Eine Anwendung kann das aktuelle Verzeichnis ändern, indem sie die SetCurrentDirectory-Funktion aufruft.
ms.assetid: b08e7739-55d4-4690-9ce5-2a8cb29214e9
title: Ändern des aktuellen Verzeichnisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf742c872bab7d37e115afa815fff961d2f975bfbd3db75ff61a5e992d64a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632110"
---
# <a name="changing-the-current-directory"></a>Ändern des aktuellen Verzeichnisses

Das Verzeichnis am Ende des aktiven Pfads wird als aktuelles Verzeichnis bezeichnet. Es handelt sich um das Verzeichnis, in dem die aktive Anwendung gestartet wurde, es sei denn, sie wurde explizit geändert. Eine Anwendung kann ermitteln, welches Verzeichnis aktuell ist, indem sie die [**GetCurrentDirectory-Funktion**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) aufruft. Manchmal ist es erforderlich, die [**GetFullPathName-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) zu verwenden, um sicherzustellen, dass der Laufwerkbuchstabe enthalten ist, wenn die Anwendung dies erfordert.

> [!Note]  
> Obwohl jeder Prozess nur über ein aktuelles Verzeichnis verfügen kann, speichert das System den letzten aktuellen Pfad für jedes Volume (Laufwerkbuchstabe), wenn die Anwendung volumes mithilfe der [**SetCurrentDirectory-Funktion**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) wechselt. Dieses Verhalten tritt nur auf, wenn ein Laufwerkbuchstabe ohne vollqualifizierten Pfad angegeben wird, wenn der aktuelle Verzeichnisverweispunkt auf ein anderes Volume geändert wird. Dies gilt für Get- oder Set-Vorgänge.

 

Eine Anwendung kann das aktuelle Verzeichnis ändern, indem sie die [**SetCurrentDirectory-Funktion**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) aufruft.

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



 

 



