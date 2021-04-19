---
description: Sie können dieselbe DLL sowohl in der Ladezeit als auch im Lauf Zeit-Dynamic Linking verwenden.
ms.assetid: 0ffce2b1-ce50-4550-aa68-6628fdcac01a
title: Verwenden Run-Time dynamischen Verknüpfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d6ca65c510433350b81a282d8bf7a3a3825ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353215"
---
# <a name="using-run-time-dynamic-linking"></a>Verwenden Run-Time dynamischen Verknüpfungen

Sie können dieselbe DLL sowohl in der Ladezeit als auch im Lauf Zeit-Dynamic Linking verwenden. Im folgenden Beispiel wird die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion verwendet, um ein Handle für die myputs-dll zu erhalten (Weitere Informationen finden Sie unter [Erstellen einer einfachen Dynamic-Link Bibliothek](creating-a-simple-dynamic-link-library.md)). Wenn **LoadLibrary** erfolgreich ist, verwendet das Programm das zurückgegebene Handle in der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion, um die Adresse der myputs-Funktion der dll zu erhalten. Nach dem Aufruf der DLL-Funktion Ruft das Programm die [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) -Funktion auf, um die dll zu entladen.

Da das Programmlauf Zeit dynamische Verknüpfungen verwendet, ist es nicht erforderlich, das Modul mit einer Import Bibliothek für die dll zu verknüpfen.

Dieses Beispiel veranschaulicht einen wichtigen Unterschied Zwischenlauf Zeit-und Lade Zeit-dynamischer Verknüpfung. Wenn die dll nicht verfügbar ist, muss die Anwendung, die die dynamische Verknüpfung zur Ladezeit verwendet, einfach beendet werden. Das Beispiel für die dynamische Verknüpfung zur Laufzeit kann jedoch auf den Fehler reagieren.


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

 

 
