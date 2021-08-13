---
description: Sie können dieselbe DLL sowohl bei dynamischen Verknüpfungen zur Ladezeit als auch zur Laufzeit verwenden.
ms.assetid: 0ffce2b1-ce50-4550-aa68-6628fdcac01a
title: Verwenden Run-Time dynamischen Verknüpfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c13cc66a34f0fd5938fcdada027b30223ebff0abe6e9ce459d60f93a6546f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119255980"
---
# <a name="using-run-time-dynamic-linking"></a>Verwenden Run-Time dynamischen Verknüpfung

Sie können dieselbe DLL sowohl bei dynamischen Verknüpfungen zur Ladezeit als auch zur Laufzeit verwenden. Im folgenden Beispiel wird die [**LoadLibrary-Funktion**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) verwendet, um ein Handle für die Myputs-DLL zu erhalten (siehe [Creating a Simple Dynamic-Link Library](creating-a-simple-dynamic-link-library.md)). Wenn **LoadLibrary** erfolgreich ist, verwendet das Programm das zurückgegebene Handle in der [**GetProcAddress-Funktion,**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) um die Adresse der myPuts-Funktion der DLL zu erhalten. Nach dem Aufruf der DLL-Funktion ruft das Programm die [**FreeLibrary-Funktion**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) auf, um die DLL zu entladen.

Da das Programm dynamisches Verknüpfen zur Laufzeit verwendet, ist es nicht erforderlich, das Modul mit einer Importbibliothek für die DLL zu verknüpfen.

In diesem Beispiel wird ein wichtiger Unterschied zwischen der dynamischen Verknüpfung zur Laufzeit und der dynamischen Verknüpfung zur Ladezeit veranschaulicht. Wenn die DLL nicht verfügbar ist, muss die Anwendung, die dynamische Verknüpfungen zur Ladezeit verwendet, einfach beendet werden. Das Beispiel für dynamisches Verknüpfen zur Laufzeit kann jedoch auf den Fehler reagieren.


```C++
// A simple program that uses LoadLibrary and 
// GetProcAddress to access myPuts from Myputs.dll. 
 
#include <windows.h> 
#include <stdio.h> 
 
typedef int (__cdecl *MYPROC)(LPWSTR); 
 
int main( void ) 
{ 
    HINSTANCE hinstLib; 
    MYPROC ProcAdd; 
    BOOL fFreeResult, fRunTimeLinkSuccess = FALSE; 
 
    // Get a handle to the DLL module.
 
    hinstLib = LoadLibrary(TEXT("MyPuts.dll")); 
 
    // If the handle is valid, try to get the function address.
 
    if (hinstLib != NULL) 
    { 
        ProcAdd = (MYPROC) GetProcAddress(hinstLib, "myPuts"); 
 
        // If the function address is valid, call the function.
 
        if (NULL != ProcAdd) 
        {
            fRunTimeLinkSuccess = TRUE;
            (ProcAdd) (L"Message sent to the DLL function\n"); 
        }
        // Free the DLL module.
 
        fFreeResult = FreeLibrary(hinstLib); 
    } 

    // If unable to call the DLL function, use an alternative.
    if (! fRunTimeLinkSuccess) 
        printf("Message printed from executable\n"); 

    return 0;

}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dynamische Verknüpfung zur Laufzeit](run-time-dynamic-linking.md)
</dt> </dl>

 

 
