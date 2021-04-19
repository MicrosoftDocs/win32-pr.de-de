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
# <a name="using-run-time-dynamic-linking"></a><span data-ttu-id="4736b-103">Verwenden Run-Time dynamischen Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="4736b-103">Using Run-Time Dynamic Linking</span></span>

<span data-ttu-id="4736b-104">Sie können dieselbe DLL sowohl in der Ladezeit als auch im Lauf Zeit-Dynamic Linking verwenden.</span><span class="sxs-lookup"><span data-stu-id="4736b-104">You can use the same DLL in both load-time and run-time dynamic linking.</span></span> <span data-ttu-id="4736b-105">Im folgenden Beispiel wird die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion verwendet, um ein Handle für die myputs-dll zu erhalten (Weitere Informationen finden Sie unter [Erstellen einer einfachen Dynamic-Link Bibliothek](creating-a-simple-dynamic-link-library.md)).</span><span class="sxs-lookup"><span data-stu-id="4736b-105">The following example uses the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to get a handle to the Myputs DLL (see [Creating a Simple Dynamic-Link Library](creating-a-simple-dynamic-link-library.md)).</span></span> <span data-ttu-id="4736b-106">Wenn **LoadLibrary** erfolgreich ist, verwendet das Programm das zurückgegebene Handle in der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion, um die Adresse der myputs-Funktion der dll zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4736b-106">If **LoadLibrary** succeeds, the program uses the returned handle in the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to get the address of the DLL's myPuts function.</span></span> <span data-ttu-id="4736b-107">Nach dem Aufruf der DLL-Funktion Ruft das Programm die [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) -Funktion auf, um die dll zu entladen.</span><span class="sxs-lookup"><span data-stu-id="4736b-107">After calling the DLL function, the program calls the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function to unload the DLL.</span></span>

<span data-ttu-id="4736b-108">Da das Programmlauf Zeit dynamische Verknüpfungen verwendet, ist es nicht erforderlich, das Modul mit einer Import Bibliothek für die dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="4736b-108">Because the program uses run-time dynamic linking, it is not necessary to link the module with an import library for the DLL.</span></span>

<span data-ttu-id="4736b-109">Dieses Beispiel veranschaulicht einen wichtigen Unterschied Zwischenlauf Zeit-und Lade Zeit-dynamischer Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="4736b-109">This example illustrates an important difference between run-time and load-time dynamic linking.</span></span> <span data-ttu-id="4736b-110">Wenn die dll nicht verfügbar ist, muss die Anwendung, die die dynamische Verknüpfung zur Ladezeit verwendet, einfach beendet werden.</span><span class="sxs-lookup"><span data-stu-id="4736b-110">If the DLL is not available, the application using load-time dynamic linking must simply terminate.</span></span> <span data-ttu-id="4736b-111">Das Beispiel für die dynamische Verknüpfung zur Laufzeit kann jedoch auf den Fehler reagieren.</span><span class="sxs-lookup"><span data-stu-id="4736b-111">The run-time dynamic linking example, however, can respond to the error.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4736b-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4736b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4736b-113">Dynamische Verknüpfung zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="4736b-113">Run-Time Dynamic Linking</span></span>](run-time-dynamic-linking.md)
</dt> </dl>

 

 
