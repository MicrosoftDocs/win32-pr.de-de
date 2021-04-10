---
description: Wenn viele Systemfunktionen ausfallen, legen Sie den letzten Fehlercode fest.
ms.assetid: 4cc626ac-7574-44ce-8377-e0bdd8e74b7e
title: Abrufen des Last-Error Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28ba096fae2bd38bb8dc9c291a677aa6fa161d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041391"
---
# <a name="retrieving-the-last-error-code"></a>Abrufen des Last-Error Codes

Wenn viele Systemfunktionen ausfallen, legen Sie den letzten Fehlercode fest. Wenn Ihre Anwendung weitere Details zu einem Fehler benötigt, kann Sie den letzten Fehlercode mithilfe der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion abrufen und eine Beschreibung des Fehlers mithilfe der [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion anzeigen.

Das folgende Beispiel enthält eine Fehler Behandlungs Funktion, die die Fehlermeldung ausgibt und den Prozess beendet. Der *lpszfunction* -Parameter ist der Name der Funktion, die den letzten Fehlercode festgelegt hat.


```C++
#include <windows.h>
#include <strsafe.h>

void ErrorExit(LPTSTR lpszFunction) 
{ 
    // Retrieve the system error message for the last-error code

    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, NULL );

    // Display the error message and exit the process

    lpDisplayBuf = (LPVOID)LocalAlloc(LMEM_ZEROINIT, 
        (lstrlen((LPCTSTR)lpMsgBuf) + lstrlen((LPCTSTR)lpszFunction) + 40) * sizeof(TCHAR)); 
    StringCchPrintf((LPTSTR)lpDisplayBuf, 
        LocalSize(lpDisplayBuf) / sizeof(TCHAR),
        TEXT("%s failed with error %d: %s"), 
        lpszFunction, dw, lpMsgBuf); 
    MessageBox(NULL, (LPCTSTR)lpDisplayBuf, TEXT("Error"), MB_OK); 

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
    ExitProcess(dw); 
}

void main()
{
    // Generate an error

    if(!GetProcessId(NULL))
        ErrorExit(TEXT("GetProcessId"));
}
```



 

 
