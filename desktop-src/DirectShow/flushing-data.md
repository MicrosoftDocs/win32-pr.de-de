---
description: Leeren von Daten
ms.assetid: 528763a2-c0f2-4981-91dc-dd17987f5bd5
title: Leeren von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a435bf40ae9f71b35707935812c3a935a95df1904db00a652634b171f20a10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965460"
---
# <a name="flushing-data"></a>Leeren von Daten

Der folgende Pseudocode zeigt, wie die [**IPin::BeginFlush-Methode implementiert**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) wird:


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



Wenn das Leeren beginnt, verwendet die **BeginFlush-Methode** die Filtersperre, die die Zustandsänderung serialisiert. Es ist noch nicht sicher, die Streamingsperre zu verwenden, da das Leeren im Anwendungsthread erfolgt und sich der Streamingthread möglicherweise in der Mitte eines **Receive-Aufrufs** befindet. Die Pin muss garantieren, dass **Receive** nicht blockiert wird und dass alle nachfolgenden Aufrufe von **Receive** fehlschlagen. Die [**CBaseInputPin::BeginFlush-Methode**](cbaseinputpin-beginflush.md) legt das interne Flag [**CBaseInputPin::m \_ bFlushing fest.**](cbaseinputpin-m-bflushing.md) Wenn das Flag **TRUE ist,** schlägt die **Receive-Methode** fehl.

Durch die Bereitstellung des **BeginFlush-Aufrufs** nachgeschaltet stellt der Pin sicher, dass alle Downstreamfilter ihre Stichproben frei geben und von **Receive-Aufrufen zurückgeben.** Dadurch wird wiederum sichergestellt, dass der Eingabepin nicht blockiert wird und auf **GetBuffer oder** **Receive wartet.** Wenn die **Receive-Methode** Ihres Pins jemals auf ein Ereignis wartet (z. B. um Ressourcen zu erhalten), sollte die **BeginFlush-Methode** erzwingen, dass der Warte-Prozess beendet wird, indem das -Ereignis festlegen. An diesem Punkt wird garantiert, dass die **Receive-Methode** zurückkommt, und das **Flag m \_ bFlushing** verhindert, dass neue **Receive-Aufrufe** arbeiten.

Bei einigen Filtern ist dies alles, was **BeginFlush** tun muss. Die **EndFlush-Methode** signalisiert dem Filter, dass sie wieder Stichproben empfangen kann. Andere Filter müssen möglicherweise Variablen oder Ressourcen in **BeginFlush verwenden,** die auch in **Receive verwendet werden.** In diesem Fall sollte der Filter zuerst die Streamingsperre halten. Achten Sie darauf, dies nicht vor einem der vorherigen Schritte zu tun, da Sie möglicherweise einen Deadlock verursachen.

Die **EndFlush-Methode** enthält die Filtersperre und gibt den Aufruf nachgeschaltet weiter:


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



Die [**CBaseInputPin::EndFlush-Methode**](cbaseinputpin-endflush.md) setzt das **m \_ bFlushing-Flag** auf **FALSE** zurück, wodurch die **Receive-Methode** wieder Mit dem Empfang von Stichproben beginnen kann. Dies sollte der letzte Schritt in **EndFlush** sein, da der Pin keine Stichproben empfangen darf, bis das Leeren abgeschlossen ist und alle Downstreamfilter benachrichtigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Threads und kritische Abschnitte](threads-and-critical-sections.md)
</dt> </dl>

 

 



