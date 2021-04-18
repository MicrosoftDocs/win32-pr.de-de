---
description: Die cbaseinputpin-Klasse ist eine abstrakte Basisklasse für die Implementierung von Eingabe Pins. Diese Klasse fügt zusätzlich zur Unterstützung der IPin-Schnittstelle, die von cbasepin bereitgestellt wird, Unterstützung für die IMemInputPin-Schnittstelle hinzu.
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: Cbaseingeputpin-Klasse (amfilter. h)
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
ms.openlocfilehash: ba55006438a8484b0bf10b95ac8b9d8bbdb56e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361522"
---
# <a name="cbaseinputpin-class"></a>Cbaseingeputpin-Klasse

![cbaseingeputpin-Klassenhierarchie](images/filter07.png)

Bei der- `CBaseInputPin` Klasse handelt es sich um eine abstrakte Basisklasse zum Implementieren von Eingabe Pins. Diese Klasse fügt zusätzlich zur Unterstützung der [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle, die von [**cbasepin**](cbasepin.md)bereitgestellt wird, Unterstützung für die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle hinzu.

Um diese Klasse zu verwenden, leiten Sie eine neue Klasse ab, und überschreiben Sie mindestens die folgenden Methoden:

-   [**Cbaseiniputpin:: beginflush**](cbaseinputpin-beginflush.md)
-   [**Cbaseingeputpin:: endflush**](cbaseinputpin-endflush.md)
-   [**Cbaseingeputpin:: Receive**](cbaseinputpin-receive.md)
-   [**Cbasepin:: checkmediatype**](cbasepin-checkmediatype.md)
-   [**Cbasepin:: getmediatype**](cbasepin-getmediatype.md)

Abhängig von der Funktion der PIN müssen Sie möglicherweise zusätzliche Methoden in `CBaseInputPin` oder **cbasepin** überschreiben.



| Geschützte Member-Variablen                                                 | BESCHREIBUNG                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**m- \_ pallocator**](cbaseinputpin-m-pallocator.md)                        | Zeiger auf die Speicherzuweisung.                                                                            |
| [**\_nur m Brot**](cbaseinputpin-m-breadonly.md)                          | Flag, das angibt, ob die Zuweisung schreibgeschützte Medien Beispiele erzeugt.                                 |
| [**m \_ bleeren**](cbaseinputpin-m-bflushing.md)                          | Flag, das angibt, ob die PIN zurzeit geleert wird.                                                  |
| [**m \_ Sample-Eigenschaften**](cbaseinputpin-m-sampleprops.md)                      | Eigenschaften des neuesten Beispiels.                                                                       |
| Öffentliche Methoden                                                             | BESCHREIBUNG                                                                                                 |
| [**Cbaseingeputpin**](cbaseinputpin-cbaseinputpin.md)                       | Konstruktormethode.                                                                                         |
| [**~ Cbaseingeputpin**](cbaseinputpin--cbaseinputpin.md)                     | Dekonstruktormethode.                                                                                          |
| [**Breakconnect**](cbaseinputpin-breakconnect.md)                         | Gibt die PIN von einer Verbindung frei.                                                                         |
| [**IsReadOnly**](cbaseinputpin-isreadonly.md)                             | Fragt ab, ob die Zuweisung schreibgeschützte Medien Beispiele verwendet.                                                 |
| [**Isleerung**](cbaseinputpin-isflushing.md)                             | Fragt ab, ob der Filter zurzeit geleert wird.                                                           |
| [**Checkstreaming**](cbaseinputpin-checkstreaming.md)                     | Bestimmt, ob die PIN Beispiele annehmen kann. Virtu.                                                     |
| [**Passnotify**](cbaseinputpin-passnotify.md)                             | Übergibt eine Qualitäts Steuerungs Meldung an das entsprechende-Objekt.                                                 |
| [**Inaktiv**](cbaseinputpin-inactive.md)                                 | Benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist. Virtu.                                              |
| [**Sample-Eigenschaften**](cbaseinputpin-sampleprops.md)                           | Ruft die Eigenschaften des neuesten Beispiels ab.                                                         |
| IPin-Methoden                                                               | BESCHREIBUNG                                                                                                 |
| [**Beginflush**](cbaseinputpin-beginflush.md)                             | Startet einen Löschvorgang.                                                                                   |
| [**Endflush**](cbaseinputpin-endflush.md)                                 | Beendet einen Löschvorgang.                                                                                     |
| IMemInputPin-Methoden                                                       | BESCHREIBUNG                                                                                                 |
| [**Getallocator**](cbaseinputpin-getallocator.md)                         | Ruft die von dieser Pin vorgeschlagene Speicherzuweisung ab.                                                        |
| [**Notifyzukator**](cbaseinputpin-notifyallocator.md)                   | Gibt eine Zuweisung für die Verbindung an.                                                                  |
| [**Getalloserorrequirements**](cbaseinputpin-getallocatorrequirements.md) | Ruft die von der eingabepin angeforderten zuordnereigenschaften ab.                                              |
| [**Medizinisch**](cbaseinputpin-receive.md)                                   | Empfängt das nächste Medien Beispiel im Stream.                                                               |
| [**Receivemultiple**](cbaseinputpin-receivemultiple.md)                   | Empfängt mehrere Stichproben im Stream.                                                                    |
| [**Receivecanblock**](cbaseinputpin-receivecanblock.md)                   | Bestimmt, ob Aufrufe der [**cbasinput PIN:: Receive**](cbaseinputpin-receive.md) -Methode blockiert werden könnten. |
| Iqualitycontrol-Methoden                                                    | BESCHREIBUNG                                                                                                 |
| [**Benachrichtigen**](cbaseinputpin-notify.md)                                     | Empfängt eine Qualitäts Steuerungs Meldung.                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




