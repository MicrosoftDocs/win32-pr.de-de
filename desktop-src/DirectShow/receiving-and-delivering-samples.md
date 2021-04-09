---
description: Empfangen und Bereitstellung von Beispielen
ms.assetid: 92954b40-1424-4dee-997c-fc41089b7fa5
title: Empfangen und Bereitstellung von Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364743e0dfc201d419a61fa4c88bde686976d6b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860185"
---
# <a name="receiving-and-delivering-samples"></a><span data-ttu-id="e83b2-103">Empfangen und Bereitstellung von Beispielen</span><span class="sxs-lookup"><span data-stu-id="e83b2-103">Receiving and Delivering Samples</span></span>

<span data-ttu-id="e83b2-104">Der folgende Pseudo Code zeigt, wie die **imeminput:: Receive** -Methode implementiert wird:</span><span class="sxs-lookup"><span data-stu-id="e83b2-104">The following pseudocode shows how to implement the **IMemInput::Receive** method:</span></span>


```C++
HRESULT CMyInputPin::Receive(IMediaSample *pSample)
{
    CAutoLock cObjectLock(&m_csReceive);

    // Perhaps the filter needs to wait on something.
    WaitForSingleObject(m_hSomeEventThatReceiveNeedsToWaitOn, INFINITE);

    // Before using resources, make sure it is safe to proceed. Do not
    // continue if the base-class method returns anything besides S_OK.
    hr = CBaseInputPin::Receive(pSample);
    if (hr != S_OK) 
    {
        return hr;
    }

    /* It is safe to use resources allocated in Active and Pause. */

    // Deliver sample(s), via your output pin(s).
    for (each output pin)
        pOutputPin->Deliver(pSample);

    return hr;
}
```



<span data-ttu-id="e83b2-105">Die **Receive** -Methode enthält die streamingsperre, nicht die Filter Sperre.</span><span class="sxs-lookup"><span data-stu-id="e83b2-105">The **Receive** method holds the streaming lock, not the filter lock.</span></span> <span data-ttu-id="e83b2-106">Der Filter muss möglicherweise auf ein Ereignis warten, bevor die Daten verarbeitet werden können. Dies ist hier durch den Rückruf von **WaitForSingleObject** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e83b2-106">The filter might need to wait on some event before it can process the data, shown here by the call to **WaitForSingleObject**.</span></span> <span data-ttu-id="e83b2-107">Nicht jeder Filter muss dies tun.</span><span class="sxs-lookup"><span data-stu-id="e83b2-107">Not every filter will need to do this.</span></span> <span data-ttu-id="e83b2-108">Die [**cbasinput PIN:: Receive**](cbaseinputpin-receive.md) -Methode überprüft einige allgemeine streamingbedingungen.</span><span class="sxs-lookup"><span data-stu-id="e83b2-108">The [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method verifies some general streaming conditions.</span></span> <span data-ttu-id="e83b2-109">\_ \_ Wenn der Filter beendet wird, wird der falsche VFW E-Status zurückgegeben \_ , false, \_ Wenn der Filter geleert wird usw.</span><span class="sxs-lookup"><span data-stu-id="e83b2-109">It returns VFW\_E\_WRONG\_STATE if the filter is stopped, S\_FALSE if the filter is flushing, and so forth.</span></span> <span data-ttu-id="e83b2-110">Jeder andere Rückgabecode als S \_ OK gibt an, dass die **Receive** -Methode sofort zurückgeben und das Beispiel nicht verarbeiten sollte.</span><span class="sxs-lookup"><span data-stu-id="e83b2-110">Any return code other than S\_OK indicates that the **Receive** method should return immediately and not process the sample.</span></span>

<span data-ttu-id="e83b2-111">Nachdem das Beispiel verarbeitet wurde, übermitteln Sie es an den downstreamfilter, indem Sie [**cbaseoutputpin::D eliver**](cbaseoutputpin-deliver.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e83b2-111">After the sample is processed, deliver it to the downstream filter by calling [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md).</span></span> <span data-ttu-id="e83b2-112">Diese Hilfsmethode ruft **IMemInputPin:: Receive** für die downstreameingabepin auf.</span><span class="sxs-lookup"><span data-stu-id="e83b2-112">This helper method calls **IMemInputPin::Receive** on the downstream input pin.</span></span> <span data-ttu-id="e83b2-113">Ein Filter kann Beispiele für mehrere Pins bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e83b2-113">A filter might deliver samples to several pins.</span></span>

 

 



