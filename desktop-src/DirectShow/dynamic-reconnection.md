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
# <a name="dynamic-reconnection"></a>Dynamische erneute Verbindung

In den meisten DirectShow-filtern kann Pins nicht wieder hergestellt werden, während das Diagramm aktiv Daten gestreamt. Die Anwendung muss das Diagramm vor dem erneuten Verbinden der Pins abbrechen. Einige Filter unterstützen jedoch Pin-Verbindungen, während das Diagramm ausgeführt wird. Dies ist ein Prozess, der als Dynamic Reconnection bezeichnet wird. Dies kann entweder durch die Anwendung oder durch einen Filter im Diagramm erfolgen.

Sehen Sie sich als Beispiel das Diagramm in der folgenden Abbildung an.

![Dynamisches Diagramm: Aufbau Diagramm](images/dyngraph.png)

Ein Szenario für die dynamische erneute Verbindungs Herstellung besteht darin, den Filter 2 aus dem Diagramm zu entfernen, während das Diagramm ausgeführt wird, und es durch einen anderen Filter zu ersetzen. Damit dieses Szenario funktioniert, muss Folgendes zutreffen:

-   Die Eingabe-PIN in Filter 3 (Pin D) muss die [**ipinconnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) -Schnittstelle unterstützen. Diese Schnittstelle ermöglicht das erneute Verbinden der PIN, ohne den Filter zu beenden.
-   Die Ausgabepin in Filter 1 (PIN A) muss in der Lage sein, den Fluss von Mediendaten zu blockieren, während die erneute Verbindung auftritt. Während der erneuten Verbindung können keine Daten zwischen Pin A und Pin D übertragen werden. Im Allgemeinen bedeutet dies, dass die Ausgabe-PIN die [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) -Schnittstelle unterstützen muss. Wenn Filter 1 jedoch der Filter ist, der die erneute Verbindung initiiert, verfügt er möglicherweise über einen internen Mechanismus zum Blockieren seines eigenen Datenflusses.

Die dynamische erneute Verbindung umfasst die folgenden Schritte:

1.  Blockiert den Datenstrom aus Pin A.
2.  Verbinden Sie die PIN A erneut mit Pin D, möglicherweise über einen neuen zwischen Filter.
3.  Lösen Sie die Blockierung von PIN A aus, sodass die Daten erneut übertragen werden.

**Schritt 1: Datenstrom blockieren**

Um den Datenstream zu blockieren, nennen Sie [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) für PIN A. Diese Methode kann asynchron oder synchron aufgerufen werden. Um die-Methode *asynchron* aufzurufen, erstellen Sie ein Win32-Ereignis Objekt und übergeben das Ereignis Handle an die **Block** -Methode. Die Methode wird sofort zurückgegeben. Warten Sie, bis das Ereignis signalisiert wurde, indem Sie eine Funktion wie **WaitForSingleObject** verwenden. Die PIN signalisiert das Ereignis, wenn es den Datenfluss blockiert hat. Beispiel:


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



Um die Methode *synchron* aufzurufen, übergeben Sie einfach den Wert **null** anstelle des Ereignis Handles. Nun wird die Methode blockiert, bis der Vorgang abgeschlossen ist. Dies geschieht möglicherweise erst, wenn die PIN bereit ist, ein neues Beispiel zu liefern. Wenn der Filter angehalten ist, kann dies einen willkürlichen Zeitraum in Anspruch nehmen. Führen Sie daher den synchronen-Befehl nicht aus Ihrem Hauptanwendungs Thread aus. Verwenden Sie einen Arbeits Thread, oder verwenden Sie die-Methode.

**Schritt 2: Verbinden Sie die Pins erneut.**

Zum erneuten Verbinden der Pins Fragen Sie den Filter Graph-Manager nach der **igraphconfig** -Schnittstelle ab und wenden entweder [**igraphconfig:: Verbindung**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) oder [**igraphconfig:: RECONFIGURE**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure)an. Die Methode zum **erneuten Verbinden** ist einfacher zu verwenden. Dies geschieht wie folgt:

-   Stoppt die zwischen Filter (im Beispiel Filter 2) und entfernt Sie aus dem Diagramm.
-   Fügt bei Bedarf neue zwischen Filter hinzu.
-   Verbindet alle Pins.
-   Hält neue Filter an oder führt Sie aus, um den Status des Diagramms abzugleichen.

Die Methode zum **erneuten Verbinden** verfügt über mehrere optionale Parameter, die verwendet werden können, um den Medientyp für die PIN-Verbindung und den zu verwendenden zwischen Filter anzugeben. Beispiel:


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



Weitere Informationen finden Sie auf der Referenzseite. Wenn die **Verbindung** -Methode nicht flexibel genug ist, können Sie die **RECONFIGURE** -Methode verwenden, die eine Anwendungs definierte Rückruf Methode zum erneuten Verbinden der Pins aufruft. Um diese Methode zu verwenden, implementieren Sie die [**igraphconfigcallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) -Schnittstelle in Ihrer Anwendung.

Bevor Sie **RECONFIGURE** aufrufen, blockieren Sie den Datenfluss aus der Ausgabe-PIN, wie zuvor beschrieben. Verschieben Sie dann alle Daten, die noch ausstehend sind, im Abschnitt des Diagramms, für das Sie die Verbindung wiederherstellen, wie folgt:

1.  Nennen Sie [**ipinconnection:: notifyendofstream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) an der Eingabe-PIN am weitesten unten in der Kette der erneuten Verbindung (Pin D im Beispiel). Übergibt ein Handle an ein Win32-Ereignis.
2.  Nennen Sie [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) in der eingabepin, die direkt aus der Ausgabe-PIN entfernt wird, in der Sie den Datenfluss blockiert haben. (In diesem Beispiel wurde der Datenfluss bei Pin a blockiert, sodass Sie **EndOfStream** in Pin B aufzurufen.)
3.  Warten Sie, bis das Ereignis signalisiert wird. Die Eingabe-PIN (Pin D) signalisiert das Ereignis, wenn es die Benachrichtigung über das Ende des Datenstroms empfängt. Dies weist darauf hin, dass keine Daten zwischen den Pins übertragen werden und dass der Aufrufer die Pins sicher erneut verbinden kann.

Beachten Sie, dass die **igraphconfig:: Reconnect** -Methode die vorherigen Schritte automatisch verarbeitet. Sie müssen diese Schritte nur ausführen, wenn Sie die **RECONFIGURE** -Methode verwenden.

Nachdem die Daten durch das Diagramm übertragen wurden, rufen Sie **RECONFIGURE** auf und übergeben einen Zeiger an Ihre **igraphconfigcallback** -Rückruf Schnittstelle. Der Filter Graph-Manager ruft die von Ihnen bereitgestellte [**igraphconfigcallback:: RECONFIGURE**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) -Methode auf.

**Schritt 3. Blockierung des Datenflusses**

Nachdem Sie die Pins erneut angeschlossen haben, entsperren Sie den Datenfluss, indem Sie **IPinFlowControl:: Block** mit dem Wert 0 (null) für den ersten Parameter aufrufen.

> [!Note]  
> Wenn eine dynamische erneute Verbindung von einem Filter durchgeführt wird, gibt es einige Thread Probleme, die Sie kennen müssen. Wenn der Filter Graph-Manager versucht, den Filter anzuhalten, kann ein Deadlock auftreten, da das Diagramm darauf wartet, dass der Filter beendet wird, während der Filter gleichzeitig darauf wartet, dass Daten durch das Diagramm übermittelt werden. Um den möglichen Deadlock zu vermeiden, übernehmen einige der in diesem Abschnitt beschriebenen Methoden ein Handle für ein Win32-Ereignis. Der Filter sollte das Ereignis signalisieren, wenn der Filter Graph-Manager versucht, den Filter anzuhalten. Weitere Informationen finden Sie unter [**igraphconfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) und [**ipinconnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dynamische Diagramm Bildung](dynamic-graph-building.md)
</dt> </dl>

 

 



