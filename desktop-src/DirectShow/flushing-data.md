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
# <a name="flushing-data"></a><span data-ttu-id="653db-103">Leeren von Daten</span><span class="sxs-lookup"><span data-stu-id="653db-103">Flushing Data</span></span>

<span data-ttu-id="653db-104">Der folgende Pseudo Code zeigt, wie die [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode implementiert wird:</span><span class="sxs-lookup"><span data-stu-id="653db-104">The following pseudocode shows how to implement the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method:</span></span>


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



<span data-ttu-id="653db-105">Wenn das leeren gestartet wird, übernimmt die **beginflush** -Methode die Filter Sperre, die die Zustandsänderung serialisiert.</span><span class="sxs-lookup"><span data-stu-id="653db-105">When flushing starts, the **BeginFlush** method takes the filter lock, which serializes the state change.</span></span> <span data-ttu-id="653db-106">Es ist noch nicht sicher, die streamingsperre zu übernehmen, da das leeren im Anwendungs Thread erfolgt und sich der streamingingthread in der Mitte eines **Empfangs** Aufrufens befinden kann.</span><span class="sxs-lookup"><span data-stu-id="653db-106">It is not yet safe to take the streaming lock, because flushing happens on the application thread, and the streaming thread might be in the middle of a **Receive** call.</span></span> <span data-ttu-id="653db-107">Die PIN muss gewährleisten, dass der **Empfangs** Vorgang nicht blockiert wird und dass alle nachfolgenden **Empfangs** Aufrufe fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="653db-107">The pin needs to guarantee that **Receive** is not blocked, and that any subsequent calls to **Receive** will fail.</span></span> <span data-ttu-id="653db-108">Die [**cbaseinputpin:: beginflush**](cbaseinputpin-beginflush.md) -Methode legt das interne Flag [**cbaseinputpin:: m \_ bflush**](cbaseinputpin-m-bflushing.md)fest.</span><span class="sxs-lookup"><span data-stu-id="653db-108">The [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) method sets an internal flag, [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md).</span></span> <span data-ttu-id="653db-109">Wenn das-Flag den Wert **true** hat, schlägt die **Receive** -Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="653db-109">When the flag is **TRUE**, the **Receive** method fails.</span></span>

<span data-ttu-id="653db-110">Durch die Bereitstellung des **beginflush** -Aufrufs nach unten stellt die PIN sicher, dass alle downstreamfilter Ihre Beispiele freigeben und von **Empfangs** Aufrufen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="653db-110">By delivering the **BeginFlush** call downstream, the pin guarantees that all downstream filters release their samples and return from **Receive** calls.</span></span> <span data-ttu-id="653db-111">Dadurch wird sichergestellt, dass die Eingabe-PIN nicht blockiert wird, um auf **GetBuffer** oder **Receive** zu warten.</span><span class="sxs-lookup"><span data-stu-id="653db-111">This in turn guarantees that the input pin is not blocked waiting for **GetBuffer** or **Receive**.</span></span> <span data-ttu-id="653db-112">Wenn die **Receive** -Methode der PIN jemals auf ein Ereignis wartet (z. b. zum Abrufen von Ressourcen), sollte die **beginflush** -Methode die Wartezeit erzwingen, indem das-Ereignis festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="653db-112">If your pin's **Receive** method ever waits on an event (for example, to get resources), the **BeginFlush** method should force the wait to terminate by setting the event.</span></span> <span data-ttu-id="653db-113">An diesem Punkt wird die **Receive** -Methode garantiert zurückgegeben, und das **m \_ bgeleert** -Flag verhindert, dass neue **Empfangs** Aufrufe durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="653db-113">At this point, the **Receive** method is guaranteed to return, and the **m\_bFlushing** flag prevents new **Receive** calls from doing any work.</span></span>

<span data-ttu-id="653db-114">Für einige Filter ist dies alles, was **beginflush** tun muss.</span><span class="sxs-lookup"><span data-stu-id="653db-114">For some filters, that is all **BeginFlush** needs to do.</span></span> <span data-ttu-id="653db-115">Die **endflush** -Methode signalisiert dem Filter, dass Sie die Beispiele erneut empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="653db-115">The **EndFlush** method will signal to the filter that it can start receiving samples again.</span></span> <span data-ttu-id="653db-116">Andere Filter müssen möglicherweise Variablen oder Ressourcen in **beginflush** verwenden, die auch beim **Empfang** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="653db-116">Other filters may need to use variables or resources in **BeginFlush** that are also used in **Receive**.</span></span> <span data-ttu-id="653db-117">In diesem Fall sollte der Filter zuerst die streamingsperre enthalten.</span><span class="sxs-lookup"><span data-stu-id="653db-117">In that case, the filter should hold the streaming lock first.</span></span> <span data-ttu-id="653db-118">Stellen Sie sicher, dass Sie dies vor den vorherigen Schritten nicht durchführen, da Sie möglicherweise einen Deadlock verursachen.</span><span class="sxs-lookup"><span data-stu-id="653db-118">Be sure not to do this before any of the previous steps, because you might cause a deadlock.</span></span>

<span data-ttu-id="653db-119">Die **endflush** -Methode enthält die Filter Sperre und gibt den nachfolgenden Rückruf aus:</span><span class="sxs-lookup"><span data-stu-id="653db-119">The **EndFlush** method holds the filter lock and propagates the call downstream:</span></span>


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



<span data-ttu-id="653db-120">Die [**cbaseinputpin:: endflush**](cbaseinputpin-endflush.md) -Methode setzt das **m \_ bflush** -Flag auf " **false**" zurück. Dadurch kann die **Receive** -Methode erneut Beispiele empfangen.</span><span class="sxs-lookup"><span data-stu-id="653db-120">The [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method resets the **m\_bFlushing** flag to **FALSE**, which allows the **Receive** method to start receiving samples again.</span></span> <span data-ttu-id="653db-121">Dies sollte der letzte Schritt in **endflush** sein, da die PIN keine Stichproben erhalten darf, bis der Löschvorgang vollständig ist und alle downstreamfilter benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="653db-121">This should be the last step in **EndFlush**, because the pin must not receive any samples until flushing is complete and all downstream filters are notified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="653db-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="653db-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="653db-123">Threads und kritische Abschnitte</span><span class="sxs-lookup"><span data-stu-id="653db-123">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



