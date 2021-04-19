---
title: Suchen von Text nach Fehler Code Nummern
description: Es ist manchmal notwendig, den Fehlertext anzuzeigen, der mit den Fehlercodes verknüpft ist, die von netzwerkbezogenen Funktionen zurückgegeben werden. Möglicherweise müssen Sie diese Aufgabe mit den Netzwerk Verwaltungsfunktionen ausführen, die vom System bereitgestellt werden.
ms.assetid: 90ed87ca-7a08-4a66-b06a-e1bf668fb81a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0811c2b2da283a9cd5eb776cdb33a175c63491
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342135"
---
# <a name="looking-up-text-for-error-code-numbers"></a>Suchen von Text nach Fehler Code Nummern

Es ist manchmal notwendig, den Fehlertext anzuzeigen, der mit den Fehlercodes verknüpft ist, die von netzwerkbezogenen Funktionen zurückgegeben werden. Möglicherweise müssen Sie diese Aufgabe mit den Netzwerk Verwaltungsfunktionen ausführen, die vom System bereitgestellt werden.

Der Fehlertext für diese Meldungen finden Sie in der Nachrichten Tabellen Datei mit dem Namen Netmsg.dll, die Sie unter% systemroot% \\ system32 finden. Diese Datei enthält Fehlermeldungen im Bereich NERR- \_ Basis (2100) bis Max \_ . NERR (Nr- \_ Basis + 899). Diese Fehlercodes werden in der SDK-Header Datei lmerr. h definiert.

Die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) -Funktion können Netmsg.dll laden. Die [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) -Funktion ordnet dem Meldungs Text einen Fehlercode zu, wenn ein Modul Handle für die Netmsg.dll Datei vorliegt.

Im folgenden Beispiel wird veranschaulicht, wie der mit den Netzwerk Verwaltungsfunktionen verknüpfte Fehlertext angezeigt wird, und es werden Fehlermeldungen angezeigt, die mit systembezogenen Fehlercodes verknüpft sind. Wenn die angegebene Fehlernummer in einem bestimmten Bereich liegt, wird das netmsg.dll Message-Modul geladen und verwendet, um die angegebene Fehlernummer mit der [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) -Funktion zu suchen.


```C++
#include <windows.h>
#include <stdio.h>

#include <lmerr.h>

void
DisplayErrorText(
    DWORD dwLastError
    );

#define RTN_OK 0
#define RTN_USAGE 1
#define RTN_ERROR 13

int
__cdecl
main(
    int argc,
    char *argv[]
    )
{
    if(argc != 2) {
        fprintf(stderr,"Usage: %s <error number>\n", argv[0]);
        return RTN_USAGE;
    }

    DisplayErrorText( atoi(argv[1]) );

    return RTN_OK;
}

void
DisplayErrorText(
    DWORD dwLastError
    )
{
    HMODULE hModule = NULL; // default to system source
    LPSTR MessageBuffer;
    DWORD dwBufferLength;

    DWORD dwFormatFlags = FORMAT_MESSAGE_ALLOCATE_BUFFER |
        FORMAT_MESSAGE_IGNORE_INSERTS |
        FORMAT_MESSAGE_FROM_SYSTEM ;

    //
    // If dwLastError is in the network range, 
    //  load the message source.
    //

    if(dwLastError >= NERR_BASE && dwLastError <= MAX_NERR) {
        hModule = LoadLibraryEx(
            TEXT("netmsg.dll"),
            NULL,
            LOAD_LIBRARY_AS_DATAFILE
            );

        if(hModule != NULL)
            dwFormatFlags |= FORMAT_MESSAGE_FROM_HMODULE;
    }

    //
    // Call FormatMessage() to allow for message 
    //  text to be acquired from the system 
    //  or from the supplied module handle.
    //

    if(dwBufferLength = FormatMessageA(
        dwFormatFlags,
        hModule, // module to get message from (NULL == system)
        dwLastError,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), // default language
        (LPSTR) &MessageBuffer,
        0,
        NULL
        ))
    {
        DWORD dwBytesWritten;

        //
        // Output message string on stderr.
        //
        WriteFile(
            GetStdHandle(STD_ERROR_HANDLE),
            MessageBuffer,
            dwBufferLength,
            &dwBytesWritten,
            NULL
            );

        //
        // Free the buffer allocated by the system.
        //
        LocalFree(MessageBuffer);
    }

    //
    // If we loaded a message source, unload it.
    //
    if(hModule != NULL)
        FreeLibrary(hModule);
}
```



Nachdem Sie dieses Programm kompiliert haben, können Sie die Fehlercode Nummer als Argument einfügen, und das Programm zeigt den Text an. Beispiel:

``` syntax
C:\> netmsg 2453
Could not find domain controller for this domain
```

 

 