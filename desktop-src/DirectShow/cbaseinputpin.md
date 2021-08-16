---
description: Die CBaseInputPin-Klasse ist eine abstrakte Basisklasse zum Implementieren von Eingabepins. Diese Klasse fügt zusätzlich zur IPin-Schnittstellenunterstützung von CBasePin Unterstützung für die IMemInputPin-Schnittstelle hinzu.
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: CBaseInputPin-Klasse (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab98a2dcb1503e7593912df0e5dff51539855611311d4704e4045816fd6380e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823884"
---
# <a name="cbaseinputpin-class"></a>CBaseInputPin-Klasse

![cbaseinputpin-Klassenhierarchie](images/filter07.png)

Die `CBaseInputPin` -Klasse ist eine abstrakte Basisklasse zum Implementieren von Eingabepins. Diese Klasse fügt zusätzlich zur IPin-Schnittstellenunterstützung von [**CBasePin**](cbasepin.md)Unterstützung für die [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) hinzu. [](/windows/desktop/api/Strmif/nn-strmif-ipin)

Um diese Klasse zu verwenden, leiten Sie eine neue Klasse ab und überschreiben mindestens die folgenden Methoden:

-   [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md)
-   [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md)
-   [**CBaseInputPin::Receive**](cbaseinputpin-receive.md)
-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md)

Abhängig von der Funktion des Pins müssen Sie möglicherweise zusätzliche Methoden in `CBaseInputPin` oder **CBasePin** überschreiben.



| Geschützte Membervariablen                                                 | Beschreibung                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**m \_ pAllocator**](cbaseinputpin-m-pallocator.md)                        | Zeiger auf die Speicherzuweisung.                                                                            |
| [**m \_ bReadOnly**](cbaseinputpin-m-breadonly.md)                          | Flag, das angibt, ob die Zuweisung schreibgeschützte Medienbeispiele erzeugt.                                 |
| [**m \_ bFlushing**](cbaseinputpin-m-bflushing.md)                          | Flag, das angibt, ob der Pin gerade geleert wird.                                                  |
| [**m \_ SampleProps**](cbaseinputpin-m-sampleprops.md)                      | Eigenschaften des letzten Beispiels.                                                                       |
| Öffentliche Methoden                                                             | Beschreibung                                                                                                 |
| [**CBaseInputPin**](cbaseinputpin-cbaseinputpin.md)                       | Konstruktormethode.                                                                                         |
| [**~CBaseInputPin**](cbaseinputpin--cbaseinputpin.md)                     | Destruktormethode.                                                                                          |
| [**BreakConnect**](cbaseinputpin-breakconnect.md)                         | Gibt den Pin von einer Verbindung frei.                                                                         |
| [**IsReadOnly**](cbaseinputpin-isreadonly.md)                             | Fragt ab, ob die Zuweisung schreibgeschützte Medienbeispiele verwendet.                                                 |
| [**IsFlushing**](cbaseinputpin-isflushing.md)                             | Fragt ab, ob der Filter gerade geleert wird.                                                           |
| [**CheckStreaming**](cbaseinputpin-checkstreaming.md)                     | Bestimmt, ob die Stecknadel Beispiele akzeptieren kann. Virtuellen.                                                     |
| [**PassNotify**](cbaseinputpin-passnotify.md)                             | Übergibt eine Qualitätskontrollmeldung an das entsprechende Objekt.                                                 |
| [**Inaktiv**](cbaseinputpin-inactive.md)                                 | Benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist. Virtuellen.                                              |
| [**SampleProps**](cbaseinputpin-sampleprops.md)                           | Ruft die Eigenschaften des letzten Beispiels ab.                                                         |
| IPin-Methoden                                                               | Beschreibung                                                                                                 |
| [**BeginFlush**](cbaseinputpin-beginflush.md)                             | Startet einen Leerungsvorgang.                                                                                   |
| [**EndFlush**](cbaseinputpin-endflush.md)                                 | Beendet einen Leerungsvorgang.                                                                                     |
| IMemInputPin-Methoden                                                       | Beschreibung                                                                                                 |
| [**GetAllocator**](cbaseinputpin-getallocator.md)                         | Ruft die von dieser Stecknadel vorgeschlagene Speicherbelegung ab.                                                        |
| [**NotifyAllocator**](cbaseinputpin-notifyallocator.md)                   | Gibt eine Zuweisung für die Verbindung an.                                                                  |
| [**GetAllocatorRequirements**](cbaseinputpin-getallocatorrequirements.md) | Ruft die vom Eingabepin angeforderten Zuweisungseigenschaften ab.                                              |
| [**Erhalten**](cbaseinputpin-receive.md)                                   | Empfängt das nächste Medienbeispiel im Stream.                                                               |
| [**ReceiveMultiple**](cbaseinputpin-receivemultiple.md)                   | Empfängt mehrere Beispiele im Stream.                                                                    |
| [**ReceiveCanBlock**](cbaseinputpin-receivecanblock.md)                   | Bestimmt, ob Aufrufe der [**CBaseInputPin::Receive-Methode**](cbaseinputpin-receive.md) blockiert werden können. |
| IQualityControl-Methoden                                                    | Beschreibung                                                                                                 |
| [**Benachrichtigen**](cbaseinputpin-notify.md)                                     | Empfängt eine Qualitätskontrollnachricht.                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




