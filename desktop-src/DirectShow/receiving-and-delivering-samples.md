---
description: Empfangen und Bereitstellen von Beispielen
ms.assetid: 92954b40-1424-4dee-997c-fc41089b7fa5
title: Empfangen und Bereitstellen von Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e507cb3e20a8fd08c891cca5143f8bbf8c9d4f9a90bad27dc201dd43c43283e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952149"
---
# <a name="receiving-and-delivering-samples"></a>Empfangen und Bereitstellen von Beispielen

Der folgende Pseudocode zeigt, wie die **IMemInput::Receive-Methode implementiert** wird:


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



Die **Receive-Methode** enthält die Streamingsperre, nicht die Filtersperre. Der Filter muss möglicherweise auf ein Ereignis warten, bevor er die Daten verarbeiten kann. Dies wird hier durch den Aufruf von **WaitForSingleObject gezeigt.** Nicht jeder Filter muss dies tun. Die [**CBaseInputPin::Receive-Methode**](cbaseinputpin-receive.md) überprüft einige allgemeine Streamingbedingungen. Sie gibt VFW E WRONG STATE zurück, wenn der Filter beendet wurde, S FALSE, wenn der Filter geleert \_ \_ wird \_ \_ usw. Jeder Rückgabecode, der nicht S OK ist, gibt an, dass die Receive-Methode sofort zurückgeben \_ und das Beispiel nicht verarbeiten soll. 

Nachdem das Beispiel verarbeitet wurde, stellen Sie es durch Aufrufen von [**CBaseOutputPin::D eliver an den Downstreamfilter.**](cbaseoutputpin-deliver.md) Diese Hilfsmethode ruft **IMemInputPin::Receive für** den Downstreameingabepin auf. Ein Filter kann Stichproben an mehrere Stecknadeln liefern.

 

 



