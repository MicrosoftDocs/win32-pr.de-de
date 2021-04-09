---
title: Erstellen einer Status Rückruffunktion
description: Erstellen einer Status Rückruffunktion
ms.assetid: 9aa98340-a5a0-4084-9670-b3c27a1351ed
keywords:
- capsetcallbackonstatus-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592a5582bca37f644810f3496a39321d22da43be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036685"
---
# <a name="creating-a-status-callback-function"></a><span data-ttu-id="8d0f8-104">Erstellen einer Status Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="8d0f8-104">Creating a Status Callback Function</span></span>

<span data-ttu-id="8d0f8-105">Das folgende Beispiel ist eine einfache Status Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="8d0f8-105">The following example is a simple status callback function.</span></span> <span data-ttu-id="8d0f8-106">Registrieren Sie diesen Rückruf mithilfe des [**capsetcallbackonstatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) -Makros.</span><span class="sxs-lookup"><span data-stu-id="8d0f8-106">Register this callback by using the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro.</span></span>


```C++
TCHAR gachAppName[] = TEXT("Application Name");  // Application name.
TCHAR gachBuffer[100];  // Global buffer.

// StatusCallbackProc: status callback function. 
// hWnd:               capture window handle. 
// nID:                status code for the current status. 
// lpStatusText:       status text string for the current status. 
// 
LRESULT PASCAL StatusCallbackProc(HWND hWnd, int nID, 
    LPTSTR lpStatusText) 
{ 
    if (!hWnd) 
        return FALSE; 
 
    if (nID == 0) {
        // Clear old status messages.
        SetWindowText(hWnd, gachAppName); 
        return (LRESULT) TRUE; 
    } 
    // Show the status ID and status text. 
    _stprintf_s(gachBuffer, TEXT("Status# %d: %s"), nID, lpStatusText); 
 
    SetWindowText(hWnd, gachBuffer); 
    return (LRESULT) TRUE; 
} 
 
```



## <a name="related-topics"></a><span data-ttu-id="8d0f8-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8d0f8-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d0f8-108">Verwenden der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="8d0f8-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




