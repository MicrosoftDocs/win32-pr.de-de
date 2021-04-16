---
description: Das folgende Codebeispiel zeigt die Verwendung eines Mutex-Objekts, um zu bestimmen, ob MSN Explorer angemeldet ist.
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: Ermitteln, ob MSN im Anmeldestatus ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d7af3511035c997493f0439a8635c1a928a75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523960"
---
# <a name="determining-if-msn-is-in-the-sign-in-state"></a><span data-ttu-id="e85de-103">Ermitteln, ob MSN im Anmeldestatus ist</span><span class="sxs-lookup"><span data-stu-id="e85de-103">Determining if MSN Is in the Sign-in State</span></span>

<span data-ttu-id="e85de-104">Das folgende Codebeispiel zeigt die Verwendung eines Mutex-Objekts, um zu bestimmen, ob MSN Explorer angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="e85de-104">The following code example shows the usage of a mutex object to determine if MSN Explorer is signed in.</span></span> <span data-ttu-id="e85de-105">Wenn Sie die Verwendung des Handles abgeschlossen haben, stellen Sie sicher, dass Sie die [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) -Funktion aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="e85de-105">When you have finished using the handle, be sure to call the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span>

> [!Note]  
> <span data-ttu-id="e85de-106">Dieses Mutex-Objekt ist für die Überprüfung von MSN Explorer 7 verfügbar. *x* -Anmeldestatus.</span><span class="sxs-lookup"><span data-stu-id="e85de-106">This mutex object is available for use in checking MSN Explorer 7.*x* sign-in status.</span></span> <span data-ttu-id="e85de-107">Er ist möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e85de-107">It may be unavailable in subsequent versions.</span></span>

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 
