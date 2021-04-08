---
description: Wenn ein Methoden Aufrufwert einen Fehler erzeugt, geben viele Funktionen einen Fehlercode zurück.
ms.assetid: 9d60277a-5ee8-471e-bfcd-d104064030a8
title: Abrufen von Fehlermeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cefeab75e4419bc1e36785236962069a6913e84d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865012"
---
# <a name="retrieving-error-messages"></a><span data-ttu-id="c3012-103">Abrufen von Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="c3012-103">Retrieving Error Messages</span></span>

<span data-ttu-id="c3012-104">Wenn ein Methoden Aufrufwert einen Fehler erzeugt, geben viele Funktionen einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="c3012-104">When a method call produces an error, many functions return an error code.</span></span> <span data-ttu-id="c3012-105">Für die meisten Zertifikat Dienst Schnittstellen und API-Elemente, die einen Fehlercode zurückgeben, kann der Fehlermeldungs Text abgerufen werden, indem [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) mit einem **null** -Modul Handle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c3012-105">For most Certificate Services interfaces and API elements that return an error code, the error message text can be retrieved by calling [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) with a **NULL** module handle.</span></span> <span data-ttu-id="c3012-106">Wenn **FormatMessage** nicht erfolgreich ist, führte der Fehlercode höchstwahrscheinlich aus einem Backup-API-Element oder einem Daten Bank bezogenen Fehler. Wenn Sie **FormatMessage** mit einem Modul handle aufrufen, das der Ntdsbmsg.dll Bibliothek entspricht, sollte der Fehlermeldungs Text abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c3012-106">If **FormatMessage** does not succeed, the error code most likely resulted from a backup API element or database related error; calling **FormatMessage** with a module handle corresponding to the Ntdsbmsg.dll library should retrieve the error message text.</span></span> <span data-ttu-id="c3012-107">Im folgenden Beispiel wird gezeigt, wie Fehlermeldungs Text in einer Zertifikat Dienst Anwendung abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c3012-107">The following example shows how to retrieve error message text in a Certificate Services application.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
// Display error message text, given an error code.
// Typically, the parameter passed to this function is retrieved
// from GetLastError().
void PrintCSBackupAPIErrorMessage(DWORD dwErr)
{

    WCHAR   wszMsgBuff[512];  // Buffer for text.

    DWORD   dwChars;  // Number of chars returned.

    // Try to get the message from the system errors.
    dwChars = FormatMessage( FORMAT_MESSAGE_FROM_SYSTEM |
                             FORMAT_MESSAGE_IGNORE_INSERTS,
                             NULL,
                             dwErr,
                             0,
                             wszMsgBuff,
                             512,
                             NULL );

    if (0 == dwChars)
    {
        // The error code did not exist in the system errors.
        // Try Ntdsbmsg.dll for the error code.

        HINSTANCE hInst;

        // Load the library.
        hInst = LoadLibrary(L"Ntdsbmsg.dll");
        if ( NULL == hInst )
        {
            printf("cannot load Ntdsbmsg.dll\n");
            exit(1);  // Could 'return' instead of 'exit'.
        }

        // Try getting message text from ntdsbmsg.
        dwChars = FormatMessage( FORMAT_MESSAGE_FROM_HMODULE |
                                 FORMAT_MESSAGE_IGNORE_INSERTS,
                                 hInst,
                                 dwErr,
                                 0,
                                 wszMsgBuff,
                                 512,
                                 NULL );

        // Free the library.
        FreeLibrary( hInst );

    }

    // Display the error message, or generic text if not found.
    printf("Error value: %d Message: %ws\n",
            dwErr,
            dwChars ? wszMsgBuff : L"Error message not found." );

}
```



 

 
