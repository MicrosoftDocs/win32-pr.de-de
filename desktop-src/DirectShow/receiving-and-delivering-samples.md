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
# <a name="receiving-and-delivering-samples"></a>Empfangen und Bereitstellung von Beispielen

Der folgende Pseudo Code zeigt, wie die **imeminput:: Receive** -Methode implementiert wird:


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



Die **Receive** -Methode enthält die streamingsperre, nicht die Filter Sperre. Der Filter muss möglicherweise auf ein Ereignis warten, bevor die Daten verarbeitet werden können. Dies ist hier durch den Rückruf von **WaitForSingleObject** dargestellt. Nicht jeder Filter muss dies tun. Die [**cbasinput PIN:: Receive**](cbaseinputpin-receive.md) -Methode überprüft einige allgemeine streamingbedingungen. \_ \_ Wenn der Filter beendet wird, wird der falsche VFW E-Status zurückgegeben \_ , false, \_ Wenn der Filter geleert wird usw. Jeder andere Rückgabecode als S \_ OK gibt an, dass die **Receive** -Methode sofort zurückgeben und das Beispiel nicht verarbeiten sollte.

Nachdem das Beispiel verarbeitet wurde, übermitteln Sie es an den downstreamfilter, indem Sie [**cbaseoutputpin::D eliver**](cbaseoutputpin-deliver.md)aufrufen. Diese Hilfsmethode ruft **IMemInputPin:: Receive** für die downstreameingabepin auf. Ein Filter kann Beispiele für mehrere Pins bereitzustellen.

 

 



