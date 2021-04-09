---
description: Wird beendet
ms.assetid: e2796b69-05e5-4ced-b238-257952d81211
title: Wird beendet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a93bde3b504400eed59190bf1651828f2f4509a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867499"
---
# <a name="stopping"></a><span data-ttu-id="30bee-103">Wird beendet</span><span class="sxs-lookup"><span data-stu-id="30bee-103">Stopping</span></span>

<span data-ttu-id="30bee-104">Die Methode " **Ende** " muss die Blockierung der **Receive** -Methode aufheben und die Zuweisung der Filter Zuweisungen aufheben.</span><span class="sxs-lookup"><span data-stu-id="30bee-104">The **Stop** method must unblock the **Receive** method and decommit the filter's allocators.</span></span> <span data-ttu-id="30bee-105">Das Decommit einer Zuweisung zwingt, dass alle ausstehenden **GetBuffer** -Aufrufe zurückgegeben werden, wodurch die Blockierung von upstreamfiltern aufgehoben wird, die auf Beispiele warten</span><span class="sxs-lookup"><span data-stu-id="30bee-105">Decommitting an allocator forces any pending **GetBuffer** calls to return, which unblocks upstream filters that are waiting for samples.</span></span> <span data-ttu-id="30bee-106">Die Methode " **Ende** " enthält die Filter Sperre und ruft dann die [**cbasefilter:: stopmethode**](cbasefilter-stop.md) auf, die [**cbasepin:: inaktiv**](cbasepin-inactive.md) auf allen Pins des Filters aufruft:</span><span class="sxs-lookup"><span data-stu-id="30bee-106">The **Stop** method holds the filter lock and then calls the [**CBaseFilter::Stop**](cbasefilter-stop.md) method, which calls [**CBasePin::Inactive**](cbasepin-inactive.md) on all of the filter's pins:</span></span>


```C++
HRESULT CMyFilter::Stop()
{
    CAutoLock lock_it(m_pLock);
    // Inactivate all the pins, to protect the filter resources.
    hr = CBaseFilter::Stop();

    /* Safe to destroy filter resources used by the streaming thread. */

    return hr;
}
```



<span data-ttu-id="30bee-107">Überschreiben Sie die **inaktive** Methode der Eingabe-PIN wie folgt:</span><span class="sxs-lookup"><span data-stu-id="30bee-107">Override the input pin's **Inactive** method as follows:</span></span>


```C++
HRESULT CMyInputPin::Inactive()
{
    // You do not need to hold the filter lock here. 
    // It is already locked in Stop.

    // Unblock Receive.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // Make sure Receive will fail. 
    // This also decommits the allocator.
    HRESULT hr = CBaseInputPin::Inactive();

    // Make sure Receive has completed, and is not using resources.
    {
        CAutoLock c(&m_csReceive);

        /* It is now safe to destroy filter resources used by the
           streaming thread. */
    }
    return hr;
}
```



 

 



