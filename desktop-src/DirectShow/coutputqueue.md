---
description: Die coutputqueue-Klasse implementiert eine Warteschlange zur Bereitstellung von Medien Beispielen.
ms.assetid: da35bdac-fdc2-4b38-8253-547a19213cce
title: Coutputqueue-Klasse (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd6167402abd36db8f436f6e27b18213642f010b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358123"
---
# <a name="coutputqueue-class"></a>Coutputqueue-Klasse

![coutputqueue](images/oput01.png)

Die- `COutputQueue` Klasse implementiert eine Warteschlange zur Bereitstellung von Medien Beispielen.

Diese Klasse ermöglicht es einer Ausgabe-PIN, Beispiele asynchron bereitzustellen. Beispiele werden in eine Warteschlange gestellt, und ein Arbeits Thread übergibt sie an die Eingabe-PIN. Die Warteschlange kann auch Steuerungs Nachrichten enthalten, die ein neues Segment, eine Benachrichtigung über das Ende des Datenstroms oder einen Löschvorgang angeben.

Um diese Klasse zu verwenden, erstellen Sie ein **coutputqueue** -Objekt für jede Ausgabepin im Filter. Geben Sie in der Konstruktormethode die Eingabe-PIN an, die mit der Ausgabepin verbunden ist. Mit dieser Klasse ruft die Ausgabe-PIN Methoden nicht direkt für die eingabepin auf. Stattdessen werden die entsprechenden Methoden in aufgerufen `COutputQueue` , wie in der folgenden Tabelle gezeigt.



| PIN-Methode                                                            | Coutputqueue-Methode                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------|
| [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)                           | [**Beginflush**](coutputqueue-beginflush.md)           |
| [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)                               | [**Endflush**](coutputqueue-endflush.md)               |
| [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)                         | [**Stereo**](coutputqueue-eos.md)                         |
| [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)                           | [**Newsegment**](coutputqueue-newsegment.md)           |
| [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)                 | [**Medizinisch**](coutputqueue-receive.md)                 |
| [**IMemInputPin:: receivemultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) | [**Receivemultiple**](coutputqueue-receivemultiple.md) |



 

Optional können Sie das-Objekt so konfigurieren, dass `COutputQueue` Beispiele synchron, ohne einen Arbeits Thread, bereitzustellen. Das Objekt kann auch zur Laufzeit entscheiden, ob ein Arbeits Thread auf der Grundlage der Merkmale der Eingabe-PIN verwendet werden soll. Weitere Informationen finden Sie unter [**coutputqueue:: coutputqueue**](coutputqueue-coutputqueue.md).



| Geschützte Member-Variablen                                   | BESCHREIBUNG                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**m \_ ppin**](coutputqueue-m-ppin.md)                       | Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Eingabe-PIN.                                               |
| [**m \_ pinputpin**](coutputqueue-m-pinputpin.md)             | Ein Zeiger auf die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle der Eingabe-PIN.                               |
| [**m \_ bbatchexact**](coutputqueue-m-bbatchexact.md)         | Flag, das angibt, ob das Objekt Stichproben in exakten Batches bereitstellt.                                |
| [**m \_ lbatchsize**](coutputqueue-m-lbatchsize.md)           | Batch Größe.                                                                                              |
| [**m- \_ Liste**](coutputqueue-m-list.md)                       | Medien Beispiel Warteschlange.                                                                                      |
| [**m \_ hsem**](coutputqueue-m-hsem.md)                       | Handle für ein Semaphor, das vom Thread verwendet wird, um auf Beispiele zu warten.                                           |
| [**m \_ evflushcomplete**](coutputqueue-m-evflushcomplete.md) | Das Ereignis, das signalisiert, wenn ein Löschvorgang abgeschlossen wurde.                                                  |
| [**m \_ hThread**](coutputqueue-m-hthread.md)                 | Handle für den Arbeits Thread.                                                                             |
| [**m \_ ppsamples**](coutputqueue-m-ppsamples.md)             | Array von Stichproben der Größe [**coutputqueue:: m \_ lbatchsize**](coutputqueue-m-lbatchsize.md).               |
| [**Mio. \_ nbatch**](coutputqueue-m-nbatched.md)               | Anzahl der Abtastungen, die momentan verarbeitet werden und auf die Verarbeitung warten                                             |
| [**m \_ lwarteschlange**](coutputqueue-m-lwaiting.md)               | Flag, das einen Wert ungleich 0 (null) aufweist, wenn der Thread auf eine Stichprobe wartet.                                   |
| [**m \_ bleeren**](coutputqueue-m-bflushing.md)             | Flag, das angibt, ob das Objekt einen Löschvorgang ausführt.                                  |
| [**m \_ bBeenden**](coutputqueue-m-bterminate.md)           | Flag, das angibt, ob der Thread beendet werden soll.                                                 |
| [**m \_ bsendanyway**](coutputqueue-m-bsendanyway.md)         | Flag zum Überschreiben der Batch Verarbeitung.                                                                       |
| [**Mio. \_ Stunde**](coutputqueue-m-hr.md)                           | **HRESULT** -Wert, der angibt, ob das Objekt Beispiele akzeptiert.                                 |
| [**m \_ heventpop**](coutputqueue-m-heventpop.md)             | Das Ereignis, das signalisiert wird, wenn das Objekt eine Stichprobe aus der Warteschlange entfernt.                              |
| Geschützte Methoden                                            | BESCHREIBUNG                                                                                              |
| [**Initialthumproc**](coutputqueue-initialthreadproc.md)  | Ruft die [**coutputqueue:: Thread proc**](coutputqueue-threadproc.md) -Methode auf, wenn der Thread erstellt wird. |
| [**ThreadProc**](coutputqueue-threadproc.md)                | Ruft Beispiele aus der Warteschlange ab und übergibt sie an die eingabepin.                                     |
| [**In Warteschlange eingereiht**](coutputqueue-isqueued.md)                    | Bestimmt, ob das Objekt einen Arbeits Thread zum Übermitteln von Beispielen verwendet.                               |
| [**Queue Sample**](coutputqueue-queuesample.md)              | Fügt eine Medien Stichprobe oder eine Kontroll Nachricht in die Warte                                                                |
| [**Isspecialsample**](coutputqueue-isspecialsample.md)      | Bestimmt, ob Daten in der Warteschlange eine Kontroll Meldung sind.                                                     |
| [**Freesamples**](coutputqueue-freesamples.md)              | Gibt alle ausstehenden Beispiele frei.                                                                               |
| [**Notifythread**](coutputqueue-notifythread.md)            | Benachrichtigt den Thread, dass die Warteschlange Daten enthält.                                                        |
| Öffentliche Methoden                                               | BESCHREIBUNG                                                                                              |
| [**Coutputqueue**](coutputqueue-coutputqueue.md)            | Konstruktormethode.                                                                                      |
| [**~ Coutputqueue**](coutputqueue--coutputqueue.md)          | Dekonstruktormethode.                                                                                       |
| [**Beginflush**](coutputqueue-beginflush.md)                | Startet einen Löschvorgang.                                                                                |
| [**Endflush**](coutputqueue-endflush.md)                    | Beendet einen Löschvorgang.                                                                                  |
| [**Stereo**](coutputqueue-eos.md)                              | Übermittelt einen End-of-Stream-Rückruf für die Eingabe-PIN.                                                         |
| [**Sendanyway**](coutputqueue-sendanyway.md)                | Stellt alle ausstehenden Beispiele bereit.                                                                            |
| [**Newsegment**](coutputqueue-newsegment.md)                | Übergibt ein neues Segment an die eingabepin.                                                                 |
| [**Medizinisch**](coutputqueue-receive.md)                      | Übermittelt ein Medien Beispiel an die Eingabe-PIN.                                                                |
| [**Receivemultiple**](coutputqueue-receivemultiple.md)      | Übermittelt einen Batch von Medien Beispielen an die eingabepin.                                                      |
| [**Zurücksetzen**](coutputqueue-reset.md)                          | Setzt das-Objekt zurück, sodass mehr Daten empfangen werden können.                                                      |
| [**IsIdle**](coutputqueue-isidle.md)                        | Bestimmt, ob das Objekt auf Daten wartet.                                                       |
| [**Setpopevent**](coutputqueue-setpopevent.md)              | Gibt ein Ereignis an, das signalisiert wird, wenn das Objekt ein Beispiel aus der Warteschlange entfernt.                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




