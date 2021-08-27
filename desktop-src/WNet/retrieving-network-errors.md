---
title: Abrufen von Netzwerkfehlern
description: Die WNET-Funktionen geben Fehlercodes für die Kompatibilität mit Windows für Arbeitsgruppen zurück. Jede WNet-Funktion legt auch den von GetLastError zurückgegebenen Fehlercodewert fest.
ms.assetid: 8188304a-8ab3-4c43-a6d6-2806043cc195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92f02a05ab93d50b9c448ae280e5de7ddbed1260cf1df8b8b3e56aa33aaeff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072020"
---
# <a name="retrieving-network-errors"></a>Abrufen von Netzwerkfehlern

Die WNET-Funktionen geben Fehlercodes für die Kompatibilität mit Windows für Arbeitsgruppen zurück. Jede WNET-Funktion legt auch den von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)zurückgegebenen Fehlercodewert fest.

Wenn eine der WNet-Funktionen ERROR \_ EXTENDED ERROR zurückgibt, kann eine Anwendung die \_ [**WNetGetLastError-Funktion**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora) aufrufen, um zusätzliche Informationen zum Fehler abzurufen. Diese Informationen sind in der Regel spezifisch für den Netzwerkanbieter.

Das folgende Beispiel veranschaulicht eine anwendungsdefinierte Fehlerbehandlungsfunktion (NetErrorHandler). Die Funktion verwendet drei Argumente: ein Fensterhandle, den von einer der WNet-Funktionen zurückgegebenen Fehlercode und den Namen der Funktion, die den Fehler erzeugt hat. Wenn der Fehlercode ERROR \_ EXTENDED \_ ERROR lautet, ruft NetErrorHandler **WNetGetLastError** auf, um erweiterte Fehlerinformationen abzurufen, und gibt die Informationen aus. Das Beispiel ruft die [**MessageBox-Funktion**](/windows/win32/api/winuser/nf-winuser-messagebox) auf, um Nachrichten zu verarbeiten.


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "mpr.lib")
#pragma comment(lib, "user32.lib")

BOOL WINAPI NetErrorHandler(HWND hwnd, 
                            DWORD dwErrorCode, 
                            LPSTR lpszFunction) 
{ 
    DWORD dwWNetResult, dwLastError; 
    CHAR szError[256]; 
    CHAR szCaption[256]; 
    CHAR szDescription[256]; 
    CHAR szProvider[256]; 
 
    // The following code performs standard error-handling. 
 
    if (dwErrorCode != ERROR_EXTENDED_ERROR) 
    { 
        sprintf_s((LPSTR) szError, sizeof(szError), "%s failed; \nResult is %ld", 
            lpszFunction, dwErrorCode); 
        sprintf_s((LPSTR) szCaption, sizeof(szCaption), "%s error", lpszFunction); 
        MessageBox(hwnd, (LPSTR) szError, (LPSTR) szCaption, MB_OK); 
        return TRUE; 
    } 
 
    // The following code performs error-handling when the 
    //  ERROR_EXTENDED_ERROR return value indicates that the 
    //  WNetGetLastError function can retrieve additional information.
 
    else 
    { 
        dwWNetResult = WNetGetLastError(&dwLastError, // error code
            (LPSTR) szDescription,  // buffer for error description 
            sizeof(szDescription),  // size of error buffer
            (LPSTR) szProvider,     // buffer for provider name 
            sizeof(szProvider));    // size of name buffer
 
        //
        // Process errors.
        //
        if(dwWNetResult != NO_ERROR) { 
            sprintf_s((LPSTR) szError, sizeof(szError), 
                "WNetGetLastError failed; error %ld", dwWNetResult); 
            MessageBox(hwnd, (LPSTR) szError, "WNetGetLastError", MB_OK); 
            return FALSE; 
        } 
 
        //
        // Otherwise, print the additional error information.
        //
        sprintf_s((LPSTR) szError, sizeof(szError), 
            "%s failed with code %ld;\n%s", 
            (LPSTR) szProvider, dwLastError, (LPSTR) szDescription); 
        sprintf_s((LPSTR) szCaption, sizeof(szCaption), "%s error", lpszFunction); 
        MessageBox(hwnd, (LPSTR) szError, (LPSTR) szCaption, MB_OK); 
        return TRUE; 
    } 
}
```



 

 