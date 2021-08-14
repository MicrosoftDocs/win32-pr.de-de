---
description: Die CPullPin-Klasse bietet Unterstützung für Eingabepins, die Daten über die IAsyncReader-Schnittstelle pullen.
ms.assetid: 33a6c342-3896-41f8-b32d-01db3eed003e
title: CPullPin-Klasse (Pullpin.h)
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
ms.openlocfilehash: d70217fa60afdae3f588f98ecbe61a728ace6ec0b0d78859f55cd241cbc00e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119330845"
---
# <a name="cpullpin-class"></a>CPullPin-Klasse

![cpullpin-Klassenhierarchie](images/pulpin01.png)

Die `CPullPin` -Klasse bietet Unterstützung für Eingabepins, die Daten über die [**IAsyncReader-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) pullen. Verwenden Sie diese Klasse, wenn Sie einen Filter implementieren, der das Pullmodell verwendet, um Daten vom Upstreamfilter anzufordern. Weitere Informationen finden Sie unter Daten Flow im Filter Graph und Pullmodell.

Diese Klasse wird nicht von **CBasePin** abgeleitet oder implementiert die [**IPin-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-ipin) und einige der Methodennamen treten mit **IPin** in Konflikt, daher wird sie am besten als Hilfsobjekt innerhalb ihrer Stecknadel verwendet. Gehen Sie wie folgt vor, um diese Klasse zu verwenden:

1.  Leiten Sie eine Hilfsklasse von `CPullPin` ab, und leiten Sie eine Eingabe-PIN-Klasse von **CBasePin** ab. Deklarieren Sie eine Instanz des `CPullPin` -Objekts als Membervariable der pin-Klasse.
2.  Überschreiben Sie die [**CBasePin::CheckConnect-Methode,**](cbasepin-checkconnect.md) um [**CPullPin::Verbinden**](cpullpin-connect.md)aufzurufen. Diese Methode fragt den anderen Pin für **IAsyncReader** ab.
3.  Überschreiben Sie die [**CBasePin::BreakConnect-Methode,**](cbasepin-breakconnect.md) um [**CPullPin::D isconnect**](cpullpin-disconnect.md)aufzurufen.
4.  Überschreiben Sie die [**CBasePin::Active-Methode,**](cbasepin-active.md) um [**CPullPin::Active**](cpullpin-active.md)aufzurufen. Diese Methode startet einen Arbeitsthread, der Stichproben aus dem Upstreamfilter abruft. Wenn die Pins verbunden sind, können Sie angeben, ob der Arbeitsthread asynchrone oder synchrone Leseanforderungen stellen soll.
5.  Überschreiben Sie die [**CBasePin::Inactive-Methode,**](cbasepin-inactive.md) um [**CPullPin::Inactive**](cpullpin-inactive.md)aufzurufen. Diese Methode fährt den Arbeitsthread herunter.
6.  Implementieren Sie die reine virtuelle [**CPullPin::Receive-Methode,**](cpullpin-receive.md) um eingehende Stichproben zu verarbeiten und nachgeschaltet zu übermitteln.
7.  Um die Stopp- und Startpositionen festzulegen oder den Stream zu suchen, rufen Sie die [**CPullPin::Seek-Methode**](cpullpin-seek.md) auf. Diese Methode hält den Arbeitsthread an und leert das Filterdiagramm.
8.  Implementieren Sie die rein virtuellen [**Methoden CPullPin::EndOfStream,**](cpullpin-endofstream.md) [**CPullPin::BeginFlush**](cpullpin-beginflush.md)und [**CPullPin::EndFlush,**](cpullpin-endflush.md) wie in den Hinweisen für diese Methoden beschrieben.
9.  Implementieren Sie die reine virtuelle [**CPullPin::OnError-Methode,**](cpullpin-onerror.md) um Streamingfehler zu behandeln.



| Öffentliche Membervariablen                             | BESCHREIBUNG                                                                           |
|-----------------------------------------------------|---------------------------------------------------------------------------------------|
| [**m \_ pAlloc**](cpullpin-m-palloc.md)              | Zeiger auf die **IMemAllocator-Schnittstelle** der Speicherzuweisung.                   |
| Öffentliche Methoden                                      | BESCHREIBUNG                                                                           |
| [**Aktiv**](cpullpin-active.md)                   | Erstellt einen Arbeitsthread, der Daten vom Ausgabepin abruft.                          |
| [**AlignDown**](cpullpin-aligndown.md)             | Schneidet einen Wert auf eine angegebene Ausrichtungsgrenze ab.                                  |
| [**AlignUp**](cpullpin-alignup.md)                 | Rundet einen Wert auf eine angegebene Ausrichtungsgrenze.                                  |
| [**Verbinden**](cpullpin-connect.md)                 | Schließt eine Verbindung mit dem Ausgabepin ab.                                             |
| [**CPullPin**](cpullpin-cpullpin.md)               | Konstruktormethode.                                                                   |
| [**~CPullPin**](cpullpin--cpullpin.md)             | Destruktormethode. Virtuellen.                                                           |
| [**DecideAllocator**](cpullpin-decideallocator.md) | Handelt eine Zuweisung mit dem Ausgabepin aus. Virtuellen.                                 |
| [**Trennen**](cpullpin-disconnect.md)           | Bekennt die Verbindung mit dem Ausgabepin.                                             |
| [**Duration**](cpullpin-duration.md)               | Ruft die Dauer des Streams ab.                                                 |
| [**GetReader**](cpullpin-getreader.md)             | Gibt einen Zeiger auf die [**IAsyncReader-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) des Ausgabepins zurück. |
| [**Inaktiv**](cpullpin-inactive.md)               | Fährt den Arbeitsthread herunter, der Daten vom Ausgabepin abruft.                     |
| [**Seek**](cpullpin-seek.md)                       | Legt die Start- und Stopppositionen des Streams fest.                                      |
| Reine virtuelle Methoden                                | BESCHREIBUNG                                                                           |
| [**BeginFlush**](cpullpin-beginflush.md)           | Informiert den besitzenden Filter, um die Downstreamfilter zu leeren.                            |
| [**EndFlush**](cpullpin-endflush.md)               | Informiert den besitzenden Filter, um einen Leerungsvorgang zu beenden.                                   |
| [**EndOfStream**](cpullpin-endofstream.md)         | Wird aufgerufen, nachdem das -Objekt das letzte Beispiel übermittelt hat.                                     |
| [**OnError**](cpullpin-onerror.md)                 | Wird aufgerufen, wenn während des Streamings ein Fehler auftritt.                                           |
| [**Erhalten**](cpullpin-receive.md)                 | Wird aufgerufen, wenn das Objekt ein Medienbeispiel vom Ausgabepin empfängt.                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




