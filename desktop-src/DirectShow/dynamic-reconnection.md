---
description: Dynamische Wiederherstellung der Verbindung
ms.assetid: 5b777f64-6b62-48dd-8eae-6603582a452a
title: Dynamische Wiederherstellung der Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b558a2e00ee2577cf1d31dda7aaebb15b5bd740c6dad5689e70b950c02d4d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966155"
---
# <a name="dynamic-reconnection"></a>Dynamische Wiederherstellung der Verbindung

In den meisten DirectShow-Filtern können Pins nicht wiederhergestellt werden, während der Graph aktiv Daten streamt. Die Anwendung muss das Diagramm beenden, bevor die Stecknadeln erneut verbunden werden. Einige Filter unterstützen jedoch pin-Wiederherstellungsverbindungen, während der Graph ausgeführt wird. Dies ist ein Prozess, der als dynamische wiederhergestellte Verbindung bezeichnet wird. Dies kann entweder durch die Anwendung oder durch einen Filter im Diagramm erfolgen.

Betrachten Sie als Beispiel das Diagramm in der folgenden Abbildung.

![Diagramm zum Erstellen dynamischer Diagramme](images/dyngraph.png)

Ein Szenario für die dynamische wiederhergestellte Verbindung könnte sein, Filter 2 aus dem Diagramm zu entfernen, während das Diagramm ausgeführt wird, und es durch einen anderen Filter zu ersetzen. Damit dieses Szenario funktioniert, muss Folgendes zutreffen:

-   Der Eingabepin für Filter 3 (Stift D) muss die [**IPinConnection-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) unterstützen. Mit dieser Schnittstelle kann die Verbindung mit dem Pin wiederhergestellt werden, ohne den Filter zu beenden.
-   Der Ausgabepin auf Filter 1 (Pin A) muss in der Lage sein, den Fluss der Mediendaten zu blockieren, während die verbindung erneut hergestellt wird. Während der erneuten Verbindung können keine Daten zwischen Anheftung A und Anheftung D gespeichert werden. Im Allgemeinen bedeutet dies, dass der Ausgabepin die [**IPinFlowControl-Schnittstelle unterstützen**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) muss. Wenn Filter 1 jedoch der Filter ist, der die erneute Verbindung initiiert, kann ein interner Mechanismus zum Blockieren des eigenen Datenflusses verwendet werden.

Die dynamische wiederhergestellte Verbindung umfasst die folgenden Schritte:

1.  Blockieren Sie den Datenstrom von Anheftung A.
2.  Verbinden Sie Anheften A erneut an Anheften D, möglicherweise über einen neuen Zwischenfilter.
3.  Entsperren Sie Anheften A, damit die Daten wieder fließen.

**Schritt 1: Blockieren des Datenstroms**

Um den Datenstrom zu blockieren, rufen Sie [**IPinFlowControl::Block an Pin**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) A auf. Diese Methode kann entweder asynchron oder synchron aufgerufen werden. Erstellen Sie zum *asynchronen Aufrufen der -Methode* ein Win32-Ereignisobjekt, und übergeben Sie das Ereignishand handle an die **Block-Methode.** Die -Methode gibt sofort zurück. Warten Sie mithilfe einer Funktion wie **WaitForSingleObject,** bis das Ereignis signalisiert wird. Der Pin signalisiert das Ereignis, wenn er den Datenfluss blockiert hat. Beispiel:


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



Um die Methode synchron *auf aufruft,* übergeben Sie einfach den Wert **NULL** anstelle des Ereignishandpunkts. Jetzt wird die -Methode blockiert, bis der Vorgang abgeschlossen ist. Dies geschieht möglicherweise erst, wenn die Stecknadel bereit ist, ein neues Beispiel zu liefern. Wenn der Filter angehalten wird, kann dies eine beliebige Zeit dauern. Daher sollten Sie den synchronen Aufruf nicht von Ihrem Hauptanwendungsthread aus machen. Verwenden Sie einen Arbeitsthread, oder rufen Sie die Methode asynchron auf.

**Schritt 2: Erneutes Verbinden der Stecknadeln**

Um die Pins erneut zu verbinden, fragen Sie den Filter Graph Manager für die **IGraphConfig-Schnittstelle** ab, und rufen Sie [**entweder IGraphConfig::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) oder [**IGraphConfig::Reconfigure auf.**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure) Die **Reconnect-Methode** ist einfacher zu verwenden. Dies führt folgende Schritte aus:

-   Beendet die Zwischenfilter (Filter 2 im Beispiel) und entfernt sie aus dem Diagramm.
-   Fügt bei Bedarf neue Zwischenfilter hinzu.
-   Verbindet alle Stecknadeln.
-   Hält neue Filter an oder führt sie aus, um mit dem Zustand des Diagramms zu übereinstimmen.

Die **Reconnect-Methode** verfügt über mehrere optionale Parameter, die verwendet werden können, um den Medientyp für die Pinverbindung und den zu verwendenden Zwischenfilter anzugeben. Beispiel:


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



Weitere Informationen finden Sie auf der Referenzseite. Wenn die **Reconnect-Methode** nicht flexibel genug ist, können Sie die **Reconfigure-Methode** verwenden, die eine anwendungsdefinierte Rückrufmethode aufruft, um die Verbindung mit den Pins wiederherzustellen. Um diese Methode zu verwenden, implementieren Sie die [**IGraphConfigCallback-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) in Ihrer Anwendung.

Blockieren Sie **vor dem Aufruf von Reconfigure** den Datenfluss über den Ausgabepin, wie zuvor beschrieben. Pushen Sie dann alle Daten, die noch ausstehend sind, wie folgt im Abschnitt des Graphen, den Sie erneut verbinden:

1.  Rufen [**Sie IPinConnection::NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) am weitesten nachgeschalteten Eingabepin in der Wiederherstellungskette auf (pin D im Beispiel). Übergeben Sie ein Handle an ein Win32-Ereignis.
2.  Rufen [**Sie IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) auf dem Eingabepin auf, der unmittelbar nach dem Ausgabepin liegt, an dem Sie den Datenfluss blockiert haben. (In diesem Beispiel wurde der Datenfluss an Pin A blockiert, sodass Sie **EndOfStream** an Pin B aufrufen.)
3.  Warten Sie, bis das Ereignis signalisiert wird. Der Eingabepin (Pin D) signalisiert das Ereignis, wenn er die Benachrichtigung zum Ende des Streams empfängt. Dies weist darauf hin, dass keine Daten zwischen den Stecknadeln unterwegs sind und dass der Aufrufer die Stecknadeln sicher wieder verbinden kann.

Beachten Sie, dass **die IGraphConfig::Reconnect-Methode** die vorherigen Schritte automatisch verarbeitet. Sie müssen diese Schritte nur ausführen, wenn Sie die **Reconfigure-Methode** verwenden.

Nachdem die Daten durch das Diagramm geschubst wurden, rufen Sie **Reconfigure** auf, und übergeben Sie einen Zeiger auf Ihre **IGraphConfigCallback-Rückrufschnittstelle.** Der Filter Graph-Manager aufruft die von Ihnen [**bereitgestellte IGraphConfigCallback::Reconfigure-Methode.**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure)

**Schritt 3: Entsperren sie die Flow**

Nachdem Sie die Verbindung mit den Stecknadeln wiederhergestellt haben, entsperren Sie die Blockierung des Datenflusses, indem Sie **IPinFlowControl::Block** mit dem Wert 0 (null) für den ersten Parameter aufrufen.

> [!Note]  
> Wenn eine dynamische wiederhergestellte Verbindung von einem Filter ausgeführt wird, müssen Sie einige Threadingprobleme beachten. Wenn der Filter Graph-Manager versucht, den Filter zu beenden, kann dies zu einem Deadlock führen, da das Diagramm auf das Beenden des Filters wartet, während der Filter gleichzeitig auf das Pushen von Daten durch das Diagramm wartet. Um einen möglichen Deadlock zu verhindern, übernehmen einige der in diesem Abschnitt beschriebenen Methoden ein Handle für ein Win32-Ereignis. Der Filter sollte das Ereignis signalisieren, wenn der Filter Graph-Manager versucht, den Filter zu beenden. Weitere Informationen finden Sie unter [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) und [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dynamic Graph Building](dynamic-graph-building.md)
</dt> </dl>

 

 



