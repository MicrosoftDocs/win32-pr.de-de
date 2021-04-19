---
description: Die cpullpin-Klasse bietet Unterstützung für Eingabe Pins, die Daten über die iasynkreader-Schnittstelle abrufen.
ms.assetid: 33a6c342-3896-41f8-b32d-01db3eed003e
title: Cpullpin-Klasse (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3039f97ca7fda43e4ecc6bd4eae05fff2ce90e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371264"
---
# <a name="cpullpin-class"></a>Cpullpin-Klasse

![cpullpin-Klassenhierarchie](images/pulpin01.png)

Die- `CPullPin` Klasse bietet Unterstützung für Eingabe Pins, die Daten über die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle abrufen. Verwenden Sie diese Klasse, wenn Sie einen Filter implementieren, der das Pull-Modell verwendet, um Daten aus dem upstreamfilter anzufordern. Weitere Informationen finden Sie unter Datenfluss im Filter Diagramm und Pull-Modell.

Diese Klasse wird nicht von **cbasepin** abgeleitet oder implementiert die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle, und einige Methodennamen kollidieren mit **IPin**, sodass Sie am besten als Hilfsobjekt in der PIN verwendet wird. Gehen Sie folgendermaßen vor, um diese Klasse zu verwenden:

1.  Leiten Sie eine Hilfsklasse von ab `CPullPin` , und leiten Sie eine Eingabe-PIN-Klasse von **cbasepin** ab. Deklarieren Sie eine Instanz des- `CPullPin` Objekts als Member-Variable der PIN-Klasse.
2.  Überschreiben Sie die [**cbasepin:: checkConnect**](cbasepin-checkconnect.md) -Methode, um [**cpullpin:: Connect**](cpullpin-connect.md)aufzurufen. Diese Methode fragt die andere PIN für **iasynkreader** ab.
3.  Überschreiben Sie die [**cbasepin:: breakconnect**](cbasepin-breakconnect.md) -Methode, um [**cpullpin::D isconnect**](cpullpin-disconnect.md)aufzurufen.
4.  Überschreiben Sie die [**cbasepin:: Active**](cbasepin-active.md) -Methode, um [**cpullpin:: Active**](cpullpin-active.md)aufzurufen. Diese Methode startet einen Arbeits Thread, der Beispiele aus dem upstreamfilter abruft. Wenn die Pins eine Verbindung herstellen, können Sie angeben, ob der Arbeits Thread asynchrone oder synchrone Lese Anforderungen erstellen soll.
5.  Überschreiben Sie die [**cbasepin:: inaktive**](cbasepin-inactive.md) -Methode, um [**cpullpin:: inaktiv**](cpullpin-inactive.md)aufzurufen. Diese Methode fährt den Arbeits Thread herunter.
6.  Implementieren Sie die reine virtuelle [**cpullpin:: Receive**](cpullpin-receive.md) -Methode, um eingehende Beispiele zu verarbeiten und Sie nachgelagert zu übermitteln.
7.  Um die Start-und Startpositionen festzulegen, oder, um den Stream zu suchen, nennen Sie die [**cpullpin:: Seek**](cpullpin-seek.md) -Methode. Diese Methode hält den Arbeits Thread an und leert das Filter Diagramm.
8.  Implementieren Sie die reinen Virtual [**cpullpin:: endolstream**](cpullpin-endofstream.md), [**cpullpin:: beginflush**](cpullpin-beginflush.md)und [**cpullpin:: endflush**](cpullpin-endflush.md) -Methoden, wie in den Hinweisen für diese Methoden beschrieben.
9.  Implementieren Sie die reine virtuelle [**cpullpin:: OnError**](cpullpin-onerror.md) -Methode, um Streamingfehler zu behandeln.



| Öffentliche Element Variablen                             | BESCHREIBUNG                                                                           |
|-----------------------------------------------------|---------------------------------------------------------------------------------------|
| [**m \_ palloc**](cpullpin-m-palloc.md)              | Ein Zeiger auf die **imemzuordcator** -Schnittstelle der Speicherzuweisung.                   |
| Öffentliche Methoden                                      | BESCHREIBUNG                                                                           |
| [**Aktiv**](cpullpin-active.md)                   | Erstellt einen Arbeits Thread, der Daten aus der Ausgabe-PIN abruft.                          |
| [**Aligndown**](cpullpin-aligndown.md)             | Verkürzt einen Wert auf eine angegebene Ausrichtungs Grenze.                                  |
| [**Ausrichtungen**](cpullpin-alignup.md)                 | Rundet einen Wert auf eine angegebene Ausrichtungs Grenze.                                  |
| [**Verbinden**](cpullpin-connect.md)                 | Schließt eine Verbindung mit der Ausgabepin ab.                                             |
| [**Cpullpin**](cpullpin-cpullpin.md)               | Konstruktormethode.                                                                   |
| [**~ Cpullpin**](cpullpin--cpullpin.md)             | Dekonstruktormethode. Virtu.                                                           |
| [**Decidezuordcator**](cpullpin-decideallocator.md) | Aushandiert eine Zuweisung mit der Ausgabepin. Virtu.                                 |
| [**Trennen**](cpullpin-disconnect.md)           | Gibt die Verbindung mit der Ausgabepin an.                                             |
| [**Duration**](cpullpin-duration.md)               | Ruft die Dauer des Streams ab.                                                 |
| [**GetReader**](cpullpin-getreader.md)             | Gibt einen Zeiger auf die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle der Ausgabe-PIN zurück. |
| [**Inaktiv**](cpullpin-inactive.md)               | Beendet den Arbeits Thread, der Daten aus der Ausgabe-PIN abruft.                     |
| [**Seek**](cpullpin-seek.md)                       | Legt die Anfangs-und Endposition des Streams fest.                                      |
| Reine virtuelle Methoden                                | BESCHREIBUNG                                                                           |
| [**Beginflush**](cpullpin-beginflush.md)           | Informiert den besitzenden Filter, die downstreamfilter zu leeren.                            |
| [**Endflush**](cpullpin-endflush.md)               | Informiert den besitzenden Filter, einen Leerungs Vorgang zu beenden.                                   |
| [**EndOfStream**](cpullpin-endofstream.md)         | Wird aufgerufen, nachdem das-Objekt das letzte Beispiel übermittelt hat.                                     |
| [**OnError**](cpullpin-onerror.md)                 | Wird aufgerufen, wenn beim Streaming ein Fehler auftritt.                                           |
| [**Medizinisch**](cpullpin-receive.md)                 | Wird aufgerufen, wenn das-Objekt ein Medien Beispiel aus der Ausgabe-PIN empfängt.                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




