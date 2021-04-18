---
description: Die cdynamicoutputpin-Klasse implementiert eine Ausgabe-PIN, die dynamische erneute Verbindungen unterstützt und Änderungen formatiert.
ms.assetid: d2488fba-a653-4b6e-b786-ce95f9e20daa
title: Cdynamicoutputpin-Klasse (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c6dab41c122456076299df22bf90d886c905cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371407"
---
# <a name="cdynamicoutputpin-class"></a>Cdynamicoutputpin-Klasse

Die `CDynamicOutputPin` -Klasse implementiert eine Ausgabe-PIN, die dynamische erneute Verbindungen unterstützt und Änderungen formatiert.

Diese Klasse wird von der [**cbaseoutputpin**](cbaseoutputpin.md) -Klasse abgeleitet und implementiert die [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) -Schnittstelle. Es werden mehrere Vorgänge unterstützt, die für die dynamische Diagramm Bildung wichtig sind:

-   Dynamische erneute Verbindung: die PIN kann die Verbindung trennen und wiederherstellen, während der Filter noch aktiv ist (angehalten oder ausgeführt wird).
-   Dynamische Formatänderung: die PIN kann einen neuen Medientyp aushandeln, während der Filter noch aktiv ist, ohne dass eine erneute Verbindung hergestellt wird.
-   Fluss Steuerung: der besitzende Filter (oder eine Anwendung) kann den Datenfluss von der PIN blockieren, ohne den Filter zu beenden.

Weitere Informationen finden Sie unter [Dynamic Graph Building](dynamic-graph-building.md).

Die PIN weist drei mögliche Zustände auf: "blockiert", "Blockierung" und "Ausstehend". Im Zustand " *Ausstehend* " wartet die PIN, bis ein Vorgang in einem anderen Thread abgeschlossen ist, bevor die PIN in den blockierten Zustand wechselt. Während die PIN blockiert ist, kann der Filter keine Daten über die PIN übermitteln oder die Verbindung der PIN ändern.

Um zwischen mehreren Threads zu koordinieren, muss der besitzende Filter bestimmte Regeln einhalten. (Weitere Informationen zu Threads im Filter Diagramm finden Sie unter [Threads und kritische Abschnitte](threads-and-critical-sections.md).) Zuerst muss der streamingingthread immer die [**cdynamicoutputpin:: startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md) -Methode aufrufen, bevor er eine der folgenden Methoden aufruft:

-   [**Cdynamicoutputpin:: changeoutputformat**](cdynamicoutputpin-changeoutputformat.md)
-   [**Cdynamicoutputpin:: changemediatype**](cdynamicoutputpin-changemediatype.md)
-   [**Cdynamicoutputpin::D ynamikreconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**Cbaseoutputpin::D eliver**](cbaseoutputpin-deliver.md)
-   [**Cbaseoutputpin::D eliverendof Stream**](cbaseoutputpin-deliverendofstream.md)
-   [**Cbaseoutputpin::D elivernewsegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin:: receivemultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Danach muss die [**cdynamicoutputpin:: stopusingoutputpin**](cdynamicoutputpin-stopusingoutputpin.md) -Methode aufgerufen werden.

Zweitens darf der Anwendungs Thread keine der Methoden in der vorherigen Liste abrufen. Drittens darf der streamingthread nicht die Klassen Methoden zum Blockieren oder Entsperren der PIN aufzurufen. Diese Methoden sind: [**cdynamicoutputpin:: Block**](cdynamicoutputpin-block.md), [**cdynamicoutputpin:: synchronousblockoutputpin**](cdynamicoutputpin-synchronousblockoutputpin.md), [**cdynamicoutputpin:: asynchronousblockoutputpin**](cdynamicoutputpin-asynchronousblockoutputpin.md)und [**cdynamicoutputpin:: unblockoutputpin**](cdynamicoutputpin-unblockoutputpin.md).

Diese Regeln stellen sicher, dass der Anwendungs Thread die PIN nicht blockieren kann, während er vom streamingthread verwendet wird, und umgekehrt. Nachdem der streamingthread **startusingoutputpin** aufgerufen hat, wird die PIN erst blockiert, wenn der streamingintthread **stopusingoutputpin** aufruft. Wenn die PIN hingegen blockiert ist, wartet **startusingoutputpin** , bis die Blockierung der PIN aufgehoben wird.

Um zu verhindern, dass **stopusingoutputpin** aufgerufen wird, können Sie die [**cautousingoutputpin**](cautousingoutputpin-cautousingoutputpin.md) -Klasse verwenden. **Stopusingoutputpin** wird automatisch aufgerufen, wenn Sie den Gültigkeitsbereich verlässt.

Wenn der besitzende Filter das Filter Diagramm (in der [**ibasefilter:: joinfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) -Methode) anfügt oder durchblättert, muss er die [**cdynamicoutputpin:: setconfiginfo**](cdynamicoutputpin-setconfiginfo.md) -Methode der PIN aufrufen.



| Geschützte Member-Variablen                                                                      | BESCHREIBUNG                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ blockstatus**](cdynamicoutputpin-m-blockstatelock.md)                                 | Kritischer Abschnitt, der den Blockierungs Zustand schützt.                                                                            |
| [**m \_ hunblockoutputpinevent**](cdynamicoutputpin-m-hunblockoutputpinevent.md)                 | Das Ereignis, das signalisiert wird, wenn die PIN nicht blockiert wird.                                                                           |
| [**m \_ hnotifycallerpinblockedevent**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)     | Das Ereignis, das signalisiert wird, wenn die PIN erfolgreich blockiert wird, oder der Benutzer bricht einen ausstehenden Block ab.                                 |
| [**m \_ blockstate**](cdynamicoutputpin-m-blockstate.md)                                         | Blockierender Zustand.                                                                                                               |
| [**m \_ dwblockcallerthreadid**](cdynamicoutputpin-m-dwblockcallerthreadid.md)                   | Der Bezeichner des Threads, der zuletzt die [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) -Methode für diese Pin aufgerufen hat. |
| [**m \_ dwnumoutstandingoutputpinusers**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md) | Anzahl der streamingthreads, die diese PIN verwenden.                                                                                   |
| [**m \_ hstopevent**](cdynamicoutputpin-m-hstopevent.md)                                         | Das Ereignis, das signalisiert wird, wenn der Filter beendet wird, oder die PIN leert Daten.                                                         |
| [**m \_ pgraphconfig**](cdynamicoutputpin-m-pgraphconfig.md)                                     | Zeiger auf die [**igraphconfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) -Schnittstelle zum durchführen dynamischer Neuverbindungen.                           |
| [**m \_ bpinseressoronlyzuweisung**](cdynamicoutputpin-m-bpinusesreadonlyallocator.md)           | Flag, das angibt, ob Beispiele aus der Zuweisung der PIN schreibgeschützt sind.                                                   |
| Geschützte Methoden                                                                               | BESCHREIBUNG                                                                                                                   |
| [**Synchronousblockoutputpin**](cdynamicoutputpin-synchronousblockoutputpin.md)                | Blockiert die PIN. gibt erst zurück, wenn die PIN blockiert ist.                                                                     |
| [**Asynchronousblockoutputpin**](cdynamicoutputpin-asynchronousblockoutputpin.md)              | Blockiert die PIN. gibt möglicherweise zurück, bevor die PIN blockiert wird.                                                                       |
| [**Unblockoutputpin**](cdynamicoutputpin-unblockoutputpin.md)                                  | Hebt die Blockierung der PIN auf.                                                                                                             |
| [**Blockoutputpin**](cdynamicoutputpin-blockoutputpin.md)                                      | Blockiert die PIN.                                                                                                               |
| [**Waitevent**](cdynamicoutputpin-waitevent.md)                                                | Wartet, bis das angegebene Ereignis signalisiert wird.                                                                                  |
| Öffentliche Methoden                                                                                  | BESCHREIBUNG                                                                                                                   |
| [**Cdynamicoutputpin**](cdynamicoutputpin-cdynamicoutputpin.md)                                | Konstruktormethode.                                                                                                           |
| [**~ Cdynamicoutputpin**](cdynamicoutputpin--cdynamicoutputpin.md)                              | Dekonstruktormethode.                                                                                                            |
| [**Setconfiginfo**](cdynamicoutputpin-setconfiginfo.md)                                        | Gibt den [**igraphconfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) -Zeiger und das-Ereignis zum Abbrechen an.                                                |
| [**Deliverbeginflush**](cdynamicoutputpin-deliverbeginflush.md)                                | Fordert an, dass die verbundene Eingabe-PIN einen Leerungs Vorgang startet.                                                                  |
| [**Deliverendflush**](cdynamicoutputpin-deliverendflush.md)                                    | Fordert die verbundene Eingabe-PIN an, einen Leerungs Vorgang zu beenden.                                                                    |
| [**Inaktiv**](cdynamicoutputpin-inactive.md)                                                  | Benachrichtigt die PIN, dass der Filter beendet wurde.                                                                                 |
| [**Aktiv**](cdynamicoutputpin-active.md)                                                      | Benachrichtigt die PIN, dass der Filter jetzt aktiv ist.                                                                               |
| [**Completeconnect**](cdynamicoutputpin-completeconnect.md)                                    | Schließt eine Verbindung mit einer Eingabe-PIN ab. Virtu.                                                                              |
| [**Startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md)                            | Erhält Zugriff auf die PIN für einen Streamingvorgang. Virtu.                                                                 |
| [**Stopusingoutputpin**](cdynamicoutputpin-stopusingoutputpin.md)                              | Gibt den Zugriff auf die PIN nach einem Streamingvorgang frei. Virtu.                                                              |
| [**Streamingthreadusingoutputpin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)        | Bestimmt, ob ein Thread einen Streamingvorgang auf der PIN ausführt. Virtu.                                        |
| [**Changeoutputformat**](cdynamicoutputpin-changeoutputformat.md)                              | Ändert den Medientyp für die Verbindung dynamisch und liefert neue Segmentinformationen.                                  |
| [**Changemediatype**](cdynamicoutputpin-changemediatype.md)                                    | Ändert den Medientyp für die Verbindung dynamisch.                                                                        |
| [**Dynamikreconnect**](cdynamicoutputpin-dynamicreconnect.md)                                  | Führt eine dynamische erneute Verbindung mit einem neuen Medientyp aus.                                                                        |
| IPin-Methoden                                                                                    | BESCHREIBUNG                                                                                                                   |
| [**Trennen**](cdynamicoutputpin-disconnect.md)                                              | Unterbricht die aktuelle PIN-Verbindung.                                                                                            |
| IPinFlowControl-Methoden                                                                         | BESCHREIBUNG                                                                                                                   |
| [**Block**](cdynamicoutputpin-block.md)                                                        | Blockiert oder entsperrt den Datenfluss aus der PIN.                                                                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




