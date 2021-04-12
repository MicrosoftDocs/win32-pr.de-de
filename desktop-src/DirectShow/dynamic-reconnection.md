---
description: Dynamische erneute Verbindung
ms.assetid: 5b777f64-6b62-48dd-8eae-6603582a452a
title: Dynamische erneute Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704178a28b91c6f78bea20b9c73c9a61f80be881
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481851"
---
# <a name="dynamic-reconnection"></a><span data-ttu-id="d7eee-103">Dynamische erneute Verbindung</span><span class="sxs-lookup"><span data-stu-id="d7eee-103">Dynamic Reconnection</span></span>

<span data-ttu-id="d7eee-104">In den meisten DirectShow-filtern kann Pins nicht wieder hergestellt werden, während das Diagramm aktiv Daten gestreamt.</span><span class="sxs-lookup"><span data-stu-id="d7eee-104">In most DirectShow filters, pins cannot be reconnected while the graph is actively streaming data.</span></span> <span data-ttu-id="d7eee-105">Die Anwendung muss das Diagramm vor dem erneuten Verbinden der Pins abbrechen.</span><span class="sxs-lookup"><span data-stu-id="d7eee-105">The application must stop the graph before reconnecting the pins.</span></span> <span data-ttu-id="d7eee-106">Einige Filter unterstützen jedoch Pin-Verbindungen, während das Diagramm ausgeführt wird. Dies ist ein Prozess, der als Dynamic Reconnection bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d7eee-106">However, some filters do support pin reconnections while the graph is running, a process known as dynamic reconnection.</span></span> <span data-ttu-id="d7eee-107">Dies kann entweder durch die Anwendung oder durch einen Filter im Diagramm erfolgen.</span><span class="sxs-lookup"><span data-stu-id="d7eee-107">This can be done either by the application, or by a filter in the graph.</span></span>

<span data-ttu-id="d7eee-108">Sehen Sie sich als Beispiel das Diagramm in der folgenden Abbildung an.</span><span class="sxs-lookup"><span data-stu-id="d7eee-108">As an example, consider the graph in the following illustration.</span></span>

![Dynamisches Diagramm: Aufbau Diagramm](images/dyngraph.png)

<span data-ttu-id="d7eee-110">Ein Szenario für die dynamische erneute Verbindungs Herstellung besteht darin, den Filter 2 aus dem Diagramm zu entfernen, während das Diagramm ausgeführt wird, und es durch einen anderen Filter zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="d7eee-110">One scenario for dynamic reconnection might be to remove Filter 2 from the graph, while the graph is running, and replace it with another filter.</span></span> <span data-ttu-id="d7eee-111">Damit dieses Szenario funktioniert, muss Folgendes zutreffen:</span><span class="sxs-lookup"><span data-stu-id="d7eee-111">For this scenario to work, the following must be true:</span></span>

-   <span data-ttu-id="d7eee-112">Die Eingabe-PIN in Filter 3 (Pin D) muss die [**ipinconnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) -Schnittstelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d7eee-112">The input pin on Filter 3 (pin D) must support the [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) interface.</span></span> <span data-ttu-id="d7eee-113">Diese Schnittstelle ermöglicht das erneute Verbinden der PIN, ohne den Filter zu beenden.</span><span class="sxs-lookup"><span data-stu-id="d7eee-113">This interface enables the pin to be reconnected without stopping the filter.</span></span>
-   <span data-ttu-id="d7eee-114">Die Ausgabepin in Filter 1 (PIN A) muss in der Lage sein, den Fluss von Mediendaten zu blockieren, während die erneute Verbindung auftritt.</span><span class="sxs-lookup"><span data-stu-id="d7eee-114">The output pin on Filter 1 (pin A) must be able to block the flow of media data while the reconnection occurs.</span></span> <span data-ttu-id="d7eee-115">Während der erneuten Verbindung können keine Daten zwischen Pin A und Pin D übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="d7eee-115">No data can travel between pin A and pin D during the reconnection.</span></span> <span data-ttu-id="d7eee-116">Im Allgemeinen bedeutet dies, dass die Ausgabe-PIN die [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) -Schnittstelle unterstützen muss.</span><span class="sxs-lookup"><span data-stu-id="d7eee-116">Generally, this means the output pin must support the [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) interface.</span></span> <span data-ttu-id="d7eee-117">Wenn Filter 1 jedoch der Filter ist, der die erneute Verbindung initiiert, verfügt er möglicherweise über einen internen Mechanismus zum Blockieren seines eigenen Datenflusses.</span><span class="sxs-lookup"><span data-stu-id="d7eee-117">However, if Filter 1 is the filter that initiates the reconnection, it might have some internal mechanism to block its own data flow.</span></span>

<span data-ttu-id="d7eee-118">Die dynamische erneute Verbindung umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="d7eee-118">The dynamic reconnection will involve the following steps:</span></span>

1.  <span data-ttu-id="d7eee-119">Blockiert den Datenstrom aus Pin A.</span><span class="sxs-lookup"><span data-stu-id="d7eee-119">Block the data stream from pin A.</span></span>
2.  <span data-ttu-id="d7eee-120">Verbinden Sie die PIN A erneut mit Pin D, möglicherweise über einen neuen zwischen Filter.</span><span class="sxs-lookup"><span data-stu-id="d7eee-120">Reconnect pin A to pin D, possibly through a new intermediate filter.</span></span>
3.  <span data-ttu-id="d7eee-121">Lösen Sie die Blockierung von PIN A aus, sodass die Daten erneut übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="d7eee-121">Unblock pin A so that data starts to flow again.</span></span>

<span data-ttu-id="d7eee-122">**Schritt 1: Datenstrom blockieren**</span><span class="sxs-lookup"><span data-stu-id="d7eee-122">**Step 1. Block the Data Stream**</span></span>

<span data-ttu-id="d7eee-123">Um den Datenstream zu blockieren, nennen Sie [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) für PIN A. Diese Methode kann asynchron oder synchron aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d7eee-123">To block the data stream, call [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) on pin A. This method can be called either asynchronously or synchronously.</span></span> <span data-ttu-id="d7eee-124">Um die-Methode *asynchron* aufzurufen, erstellen Sie ein Win32-Ereignis Objekt und übergeben das Ereignis Handle an die **Block** -Methode.</span><span class="sxs-lookup"><span data-stu-id="d7eee-124">To call the method *asynchronously*, create a Win32 event object and pass the event handle to the **Block** method.</span></span> <span data-ttu-id="d7eee-125">Die Methode wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7eee-125">The method will return immediately.</span></span> <span data-ttu-id="d7eee-126">Warten Sie, bis das Ereignis signalisiert wurde, indem Sie eine Funktion wie **WaitForSingleObject** verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7eee-126">Wait for the event to be signaled, using a function such as **WaitForSingleObject**.</span></span> <span data-ttu-id="d7eee-127">Die PIN signalisiert das Ereignis, wenn es den Datenfluss blockiert hat.</span><span class="sxs-lookup"><span data-stu-id="d7eee-127">The pin signals the event when it has blocked the data flow.</span></span> <span data-ttu-id="d7eee-128">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d7eee-128">For example:</span></span>


```C++
// Create an event
HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (hEvent != NULL)
{
    // Block the data flow.
    hr = pFlowControl->Block(AM_PIN_FLOW_CONTROL_BLOCK, hEvent); 
    if (SUCCEEDED(hr))
    {
        // Wait for the pin to finish.
        DWORD dwRes = WaitForSingleObject(hEvent, dwMilliseconds);
    }
}
```



<span data-ttu-id="d7eee-129">Um die Methode *synchron* aufzurufen, übergeben Sie einfach den Wert **null** anstelle des Ereignis Handles.</span><span class="sxs-lookup"><span data-stu-id="d7eee-129">To call the method *synchronously*, simply pass the value **NULL** instead of the event handle.</span></span> <span data-ttu-id="d7eee-130">Nun wird die Methode blockiert, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d7eee-130">Now the method will block until the operation completes.</span></span> <span data-ttu-id="d7eee-131">Dies geschieht möglicherweise erst, wenn die PIN bereit ist, ein neues Beispiel zu liefern.</span><span class="sxs-lookup"><span data-stu-id="d7eee-131">This may not happen until the pin is ready to deliver a new sample.</span></span> <span data-ttu-id="d7eee-132">Wenn der Filter angehalten ist, kann dies einen willkürlichen Zeitraum in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="d7eee-132">If the filter is paused, this can take an arbitrary length of time.</span></span> <span data-ttu-id="d7eee-133">Führen Sie daher den synchronen-Befehl nicht aus Ihrem Hauptanwendungs Thread aus.</span><span class="sxs-lookup"><span data-stu-id="d7eee-133">Therefore, do not make the synchronous call from your main application thread.</span></span> <span data-ttu-id="d7eee-134">Verwenden Sie einen Arbeits Thread, oder verwenden Sie die-Methode.</span><span class="sxs-lookup"><span data-stu-id="d7eee-134">Use a worker thread, or else call the method asynchronously.</span></span>

<span data-ttu-id="d7eee-135">**Schritt 2: Verbinden Sie die Pins erneut.**</span><span class="sxs-lookup"><span data-stu-id="d7eee-135">**Step 2. Reconnect the Pins**</span></span>

<span data-ttu-id="d7eee-136">Zum erneuten Verbinden der Pins Fragen Sie den Filter Graph-Manager nach der **igraphconfig** -Schnittstelle ab und wenden entweder [**igraphconfig:: Verbindung**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) oder [**igraphconfig:: RECONFIGURE**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure)an.</span><span class="sxs-lookup"><span data-stu-id="d7eee-136">To reconnect the pins, query the Filter Graph Manager for the **IGraphConfig** interface and call either [**IGraphConfig::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) or [**IGraphConfig::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure).</span></span> <span data-ttu-id="d7eee-137">Die Methode zum **erneuten Verbinden** ist einfacher zu verwenden. Dies geschieht wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d7eee-137">The **Reconnect** method is simpler to use; it does the following:</span></span>

-   <span data-ttu-id="d7eee-138">Stoppt die zwischen Filter (im Beispiel Filter 2) und entfernt Sie aus dem Diagramm.</span><span class="sxs-lookup"><span data-stu-id="d7eee-138">Stops the intermediate filters (Filter 2 in the example) and removes them from the graph.</span></span>
-   <span data-ttu-id="d7eee-139">Fügt bei Bedarf neue zwischen Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="d7eee-139">Adds new intermediate filters, if needed.</span></span>
-   <span data-ttu-id="d7eee-140">Verbindet alle Pins.</span><span class="sxs-lookup"><span data-stu-id="d7eee-140">Connects all the pins.</span></span>
-   <span data-ttu-id="d7eee-141">Hält neue Filter an oder führt Sie aus, um den Status des Diagramms abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="d7eee-141">Pauses or runs any new filters, to match the state of the graph.</span></span>

<span data-ttu-id="d7eee-142">Die Methode zum **erneuten Verbinden** verfügt über mehrere optionale Parameter, die verwendet werden können, um den Medientyp für die PIN-Verbindung und den zu verwendenden zwischen Filter anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d7eee-142">The **Reconnect** method has several optional parameters that can be used to specify the media type for the pin connection and the intermediate filter to use.</span></span> <span data-ttu-id="d7eee-143">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d7eee-143">For example:</span></span>


```C++
pGraph->AddFilter(pNewFilter, L"New Filter for the Graph");
pConfig->Reconnect(
    pPinA,      // Reconnect this output pin...
    pPinD,      // ... to this input pin.
    pMediaType, // Use this media type.
    pNewFilter, // Connect them through this filter.
    NULL, 
    0);     
```



<span data-ttu-id="d7eee-144">Weitere Informationen finden Sie auf der Referenzseite.</span><span class="sxs-lookup"><span data-stu-id="d7eee-144">For details, consult the reference page.</span></span> <span data-ttu-id="d7eee-145">Wenn die **Verbindung** -Methode nicht flexibel genug ist, können Sie die **RECONFIGURE** -Methode verwenden, die eine Anwendungs definierte Rückruf Methode zum erneuten Verbinden der Pins aufruft.</span><span class="sxs-lookup"><span data-stu-id="d7eee-145">If the **Reconnect** method is not flexible enough, you can use the **Reconfigure** method, which calls an application-defined callback method to reconnect the pins.</span></span> <span data-ttu-id="d7eee-146">Um diese Methode zu verwenden, implementieren Sie die [**igraphconfigcallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) -Schnittstelle in Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d7eee-146">To use this method, implement the [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) interface in your application.</span></span>

<span data-ttu-id="d7eee-147">Bevor Sie **RECONFIGURE** aufrufen, blockieren Sie den Datenfluss aus der Ausgabe-PIN, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d7eee-147">Before calling **Reconfigure**, block the data flow from the output pin, as described previously.</span></span> <span data-ttu-id="d7eee-148">Verschieben Sie dann alle Daten, die noch ausstehend sind, im Abschnitt des Diagramms, für das Sie die Verbindung wiederherstellen, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d7eee-148">Then push any data that is still pending in the section of the graph that you are reconnecting, as follows:</span></span>

1.  <span data-ttu-id="d7eee-149">Nennen Sie [**ipinconnection:: notifyendofstream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) an der Eingabe-PIN am weitesten unten in der Kette der erneuten Verbindung (Pin D im Beispiel).</span><span class="sxs-lookup"><span data-stu-id="d7eee-149">Call [**IPinConnection::NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) on the input pin furthest downstream in the reconnection chain (pin D in the example).</span></span> <span data-ttu-id="d7eee-150">Übergibt ein Handle an ein Win32-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d7eee-150">Pass in a handle to a Win32 event.</span></span>
2.  <span data-ttu-id="d7eee-151">Nennen Sie [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) in der eingabepin, die direkt aus der Ausgabe-PIN entfernt wird, in der Sie den Datenfluss blockiert haben.</span><span class="sxs-lookup"><span data-stu-id="d7eee-151">Call [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the input pin that is immediately downstream from the output pin where you blocked the data flow.</span></span> <span data-ttu-id="d7eee-152">(In diesem Beispiel wurde der Datenfluss bei Pin a blockiert, sodass Sie **EndOfStream** in Pin B aufzurufen.)</span><span class="sxs-lookup"><span data-stu-id="d7eee-152">(In this example, the data flow was blocked at pin A, so you would call **EndOfStream** on pin B.)</span></span>
3.  <span data-ttu-id="d7eee-153">Warten Sie, bis das Ereignis signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d7eee-153">Wait for the event to be signaled.</span></span> <span data-ttu-id="d7eee-154">Die Eingabe-PIN (Pin D) signalisiert das Ereignis, wenn es die Benachrichtigung über das Ende des Datenstroms empfängt.</span><span class="sxs-lookup"><span data-stu-id="d7eee-154">The input pin (pin D) signals the event when it receives the end-of-stream notification.</span></span> <span data-ttu-id="d7eee-155">Dies weist darauf hin, dass keine Daten zwischen den Pins übertragen werden und dass der Aufrufer die Pins sicher erneut verbinden kann.</span><span class="sxs-lookup"><span data-stu-id="d7eee-155">This indicates that no data is traveling between the pins, and that the caller can safely reconnect the pins.</span></span>

<span data-ttu-id="d7eee-156">Beachten Sie, dass die **igraphconfig:: Reconnect** -Methode die vorherigen Schritte automatisch verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d7eee-156">Note that the **IGraphConfig::Reconnect** method automatically handles the previous steps.</span></span> <span data-ttu-id="d7eee-157">Sie müssen diese Schritte nur ausführen, wenn Sie die **RECONFIGURE** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7eee-157">You only need to perform these steps if you are using the **Reconfigure** method.</span></span>

<span data-ttu-id="d7eee-158">Nachdem die Daten durch das Diagramm übertragen wurden, rufen Sie **RECONFIGURE** auf und übergeben einen Zeiger an Ihre **igraphconfigcallback** -Rückruf Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d7eee-158">After the data is pushed through the graph, call **Reconfigure** and pass a pointer to your **IGraphConfigCallback** callback interface.</span></span> <span data-ttu-id="d7eee-159">Der Filter Graph-Manager ruft die von Ihnen bereitgestellte [**igraphconfigcallback:: RECONFIGURE**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="d7eee-159">The Filter Graph Manager will call the [**IGraphConfigCallback::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) method that you have provided.</span></span>

<span data-ttu-id="d7eee-160">**Schritt 3. Blockierung des Datenflusses**</span><span class="sxs-lookup"><span data-stu-id="d7eee-160">**Step 3. Unblock the Data Flow**</span></span>

<span data-ttu-id="d7eee-161">Nachdem Sie die Pins erneut angeschlossen haben, entsperren Sie den Datenfluss, indem Sie **IPinFlowControl:: Block** mit dem Wert 0 (null) für den ersten Parameter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d7eee-161">After you have reconnected the pins, unblock the data flow by calling **IPinFlowControl::Block** with a value of zero for the first parameter.</span></span>

> [!Note]  
> <span data-ttu-id="d7eee-162">Wenn eine dynamische erneute Verbindung von einem Filter durchgeführt wird, gibt es einige Thread Probleme, die Sie kennen müssen.</span><span class="sxs-lookup"><span data-stu-id="d7eee-162">If a dynamic reconnection is performed by a filter, there are some threading issues that you must be aware of.</span></span> <span data-ttu-id="d7eee-163">Wenn der Filter Graph-Manager versucht, den Filter anzuhalten, kann ein Deadlock auftreten, da das Diagramm darauf wartet, dass der Filter beendet wird, während der Filter gleichzeitig darauf wartet, dass Daten durch das Diagramm übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="d7eee-163">If the Filter Graph Manager tries to stop the filter, it can deadlock, because the graph waits for the filter to stop, while at the same time the filter may be waiting for data to be pushed through the graph.</span></span> <span data-ttu-id="d7eee-164">Um den möglichen Deadlock zu vermeiden, übernehmen einige der in diesem Abschnitt beschriebenen Methoden ein Handle für ein Win32-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d7eee-164">To prevent the possible deadlock, some of the methods described in this section take a handle to a Win32 event.</span></span> <span data-ttu-id="d7eee-165">Der Filter sollte das Ereignis signalisieren, wenn der Filter Graph-Manager versucht, den Filter anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="d7eee-165">The filter should signal the event if the Filter Graph Manager attempts to stop the filter.</span></span> <span data-ttu-id="d7eee-166">Weitere Informationen finden Sie unter [**igraphconfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) und [**ipinconnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).</span><span class="sxs-lookup"><span data-stu-id="d7eee-166">For more information, see [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) and [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d7eee-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7eee-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7eee-168">Dynamische Diagramm Bildung</span><span class="sxs-lookup"><span data-stu-id="d7eee-168">Dynamic Graph Building</span></span>](dynamic-graph-building.md)
</dt> </dl>

 

 



