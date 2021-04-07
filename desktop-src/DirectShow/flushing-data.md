---
description: Leeren von Daten
ms.assetid: 528763a2-c0f2-4981-91dc-dd17987f5bd5
title: Leeren von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ddd052c18928d53511d9e955122d2d66ee59d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745633"
---
# <a name="flushing-data"></a>Leeren von Daten

Der folgende Pseudo Code zeigt, wie die [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode implementiert wird:


```C++
HRESULT CMyInputPin::BeginFlush()
{
    CAutoLock lock_it(m_pLock);
   
    // First, make sure the Receive method will fail from now on.
    HRESULT hr = CBaseInputPin::BeginFlush();
    
    // Force downstream filters to release samples. If our Receive method
    // is blocked in GetBuffer or Deliver, this will unblock it.
    for (each output pin)
    {
        hr = pOutputPin->DeliverBeginFlush();
    }

    // Unblock our Receive method if it is waiting on an event.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // At this point, the Receive method can't be blocked. Make sure 
    // it finishes, by taking the streaming lock. (Not necessary if this 
    // is the last step.)
    { 
        CAutoLock lock_2(&m_csReceive);

        /* Now it's safe to do anything that would crash or hang 
           if Receive were executing. */
    }
    return hr;
}
```



Wenn das leeren gestartet wird, übernimmt die **beginflush** -Methode die Filter Sperre, die die Zustandsänderung serialisiert. Es ist noch nicht sicher, die streamingsperre zu übernehmen, da das leeren im Anwendungs Thread erfolgt und sich der streamingingthread in der Mitte eines **Empfangs** Aufrufens befinden kann. Die PIN muss gewährleisten, dass der **Empfangs** Vorgang nicht blockiert wird und dass alle nachfolgenden **Empfangs** Aufrufe fehlschlagen. Die [**cbaseinputpin:: beginflush**](cbaseinputpin-beginflush.md) -Methode legt das interne Flag [**cbaseinputpin:: m \_ bflush**](cbaseinputpin-m-bflushing.md)fest. Wenn das-Flag den Wert **true** hat, schlägt die **Receive** -Methode fehl.

Durch die Bereitstellung des **beginflush** -Aufrufs nach unten stellt die PIN sicher, dass alle downstreamfilter Ihre Beispiele freigeben und von **Empfangs** Aufrufen zurückgegeben werden. Dadurch wird sichergestellt, dass die Eingabe-PIN nicht blockiert wird, um auf **GetBuffer** oder **Receive** zu warten. Wenn die **Receive** -Methode der PIN jemals auf ein Ereignis wartet (z. b. zum Abrufen von Ressourcen), sollte die **beginflush** -Methode die Wartezeit erzwingen, indem das-Ereignis festgelegt wird. An diesem Punkt wird die **Receive** -Methode garantiert zurückgegeben, und das **m \_ bgeleert** -Flag verhindert, dass neue **Empfangs** Aufrufe durchgeführt werden.

Für einige Filter ist dies alles, was **beginflush** tun muss. Die **endflush** -Methode signalisiert dem Filter, dass Sie die Beispiele erneut empfangen kann. Andere Filter müssen möglicherweise Variablen oder Ressourcen in **beginflush** verwenden, die auch beim **Empfang** verwendet werden. In diesem Fall sollte der Filter zuerst die streamingsperre enthalten. Stellen Sie sicher, dass Sie dies vor den vorherigen Schritten nicht durchführen, da Sie möglicherweise einen Deadlock verursachen.

Die **endflush** -Methode enthält die Filter Sperre und gibt den nachfolgenden Rückruf aus:


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



Die [**cbaseinputpin:: endflush**](cbaseinputpin-endflush.md) -Methode setzt das **m \_ bflush** -Flag auf " **false**" zurück. Dadurch kann die **Receive** -Methode erneut Beispiele empfangen. Dies sollte der letzte Schritt in **endflush** sein, da die PIN keine Stichproben erhalten darf, bis der Löschvorgang vollständig ist und alle downstreamfilter benachrichtigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Threads und kritische Abschnitte](threads-and-critical-sections.md)
</dt> </dl>

 

 



