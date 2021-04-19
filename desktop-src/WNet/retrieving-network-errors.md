---
title: Abrufen von Netzwerkfehlern
description: Die WNET-Funktionen geben Fehlercodes für die Kompatibilität mit Windows für Arbeitsgruppen zurück. Jede WNET-Funktion legt auch den von GetLastError zurückgegebenen Fehler Codewert fest.
ms.assetid: 8188304a-8ab3-4c43-a6d6-2806043cc195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436d63b51d0f57698403d206774710450eee1c8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339505"
---
# <a name="retrieving-network-errors"></a>Abrufen von Netzwerkfehlern

Die WNET-Funktionen geben Fehlercodes für die Kompatibilität mit Windows für Arbeitsgruppen zurück. Jede WNET-Funktion legt auch den von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)zurückgegebenen Fehler Codewert fest.

Wenn eine der WNET-Funktionen einen erweiterten Fehler Fehler zurückgibt \_ \_ , kann eine Anwendung die [**wnetgetlasterror**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora) -Funktion aufrufen, um zusätzliche Informationen zum Fehler abzurufen. Diese Informationen sind in der Regel spezifisch für den Netzwerkanbieter.

Im folgenden Beispiel wird eine Anwendungs definierte Fehler Behandlungs Funktion ("netterrorhandler") veranschaulicht. Die Funktion nimmt drei Argumente an: ein Fenster Handle, den von einer der WNET-Funktionen zurückgegebenen Fehlercode und den Namen der Funktion, die den Fehler erzeugt hat. Wenn der Fehlercode "Fehler bei erweiterter Fehler" lautet \_ \_ , ruft "netterrorhandler" **wnetgetlasterror** auf, um erweiterte Fehlerinformationen zu erhalten und die Informationen zu drucken. Das Beispiel ruft die [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) -Funktion auf, um Nachrichten zu verarbeiten.


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



 

 