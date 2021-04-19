---
description: 'Die ctransinplacefilter-Klasse wurde für direkte Transformations Filter entwickelt, bei denen es sich um Filter handelt, die die Eingabedaten ändern, anstatt die Daten über Puffer hinweg zu kopieren. Um diese Klasse zu verwenden, leiten Sie eine neue Klasse von ctransinplacefilter ab, und implementieren Sie die folgenden Methoden:'
ms.assetid: 3d6d5436-f280-4e36-96e4-40161e8115c2
title: Ctransinplacefilter-Klasse (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f59dd312adbb95797caf695aecea082f296df5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372642"
---
# <a name="ctransinplacefilter-class"></a>Ctransinplacefilter-Klasse

![ctransinplacefilter-Klassenhierarchie](images/tsip03.png)

Die- `CTransInPlaceFilter` Klasse wurde für direkte Transformations Filter entwickelt, bei denen es sich um Filter handelt, die die Eingabedaten ändern, anstatt die Daten über Puffer hinweg zu kopieren. Um diese Klasse zu verwenden, leiten Sie eine neue Klasse von ab, `CTransInPlaceFilter` und implementieren Sie die folgenden Methoden:

-   [**Ctransformfilter:: checkinputtype**](ctransformfilter-checkinputtype.md)
-   [**Ctransinplacefilter:: Transform**](ctransinplacefilter-transform.md)

Diese Klasse verwendet die [**ctransinplaceinputpin**](ctransinplaceinputpin.md) -Klasse für Ihre Eingabe-PIN und die [**ctransinplaceoutputpin**](ctransinplaceoutputpin.md) -Klasse für Ihre Ausgabe-PIN. In der Regel müssen Sie diese Pin-Klassen nicht überschreiben. Der Filter erstellt beide Pins in der [**ctransinplacefilter:: getpin**](ctransinplacefilter-getpin.md) -Methode. Wenn Sie die PIN-Klassen überschreiben, müssen Sie **getpin** überschreiben, um Ihre benutzerdefinierten Pins zu erstellen.

Diese Klasse ist so konzipiert, dass der Eingabetyp immer dem Ausgabetyp entspricht. Wenn möglich, verwendet der Filter einen einzelnen Zuweiser für beide Pin-Verbindungen.

## <a name="preferred-media-types"></a>Bevorzugte Medientypen

Wenn die Ausgabe-PIN bereits verbunden ist, bietet die Eingabe-PIN die bevorzugten Typen der nachgeschalteten Filter. (In der Tat gibt es einfach das Enumeratorobjekt des downstreamfilters zurück.) Andernfalls weist Sie keine bevorzugten Typen auf. Die Ausgabe-PIN weist das gleiche Verhalten auf, aber umgekehrt: Wenn die Eingabe-PIN bereits verbunden ist, bietet die Ausgabepin die bevorzugten Typen des upstreamfilters. Andernfalls gibt es keine bevorzugten Typen.

## <a name="pin-connections"></a>PIN-Verbindungen

Wenn eine PIN eine Verbindung herstellt, verbindet der Filter die andere PIN im allgemeinen erneut, um sicherzustellen, dass beide Pins denselben Medientyp und denselben Zuweiser verwenden. (Der Mechanismus zum erneuten Verbinden von Pins wird unter [Verbinden von Pins](reconnecting-pins.md)beschrieben.) Zwei Szenarien sind möglich: entweder wird die Eingabe-PIN zuerst hergestellt, oder die Ausgabe-PIN stellt zuerst eine Verbindung her.

Angenommen, die Eingabe-PIN stellt zuerst eine Verbindung her. Dabei werden die folgenden Schritte ausgeführt:

1.  Mit der Eingabe-PIN wird die [**checkinputtype**](ctransformfilter-checkinputtype.md) -Methode des Filters aufgerufen, um den Medientyp zu überprüfen.
2.  Der upstreamfilter wählt einen Zuweiser aus. An diesem Punkt weist die eingabepin keine zuordneranforderungen auf und akzeptiert jede Zuweisung für die Verbindung. Wenn der upstreamfilter eine Zuweisung anfordert, erstellt die PIN einen neuen. Aus den in Kürze beschriebenen Gründen wird diese Zuweisung nicht in der endgültigen Verbindung verwendet. Sie wird nur bereitgestellt, um die Beendigung dieser Phase des Verbindungs Vorgangs zu unterstützen.

Wenn die Ausgabepin später eine Verbindung herstellt:

1.  Mit der Ausgabe-PIN wird die [**checkinputtype**](ctransformfilter-checkinputtype.md) -Methode des Filters aufgerufen, um den Medientyp zu überprüfen. Außerdem wird [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) für den upstreamfilter aufgerufen. Dadurch wird sichergestellt, dass die Eingabe-PIN den Medientyp entsprechend ändern kann.
2.  Mit der Ausgabe-PIN wird die [**checkinputtype**](ctransformfilter-checkinputtype.md) -Methode des Filters aufgerufen, um den Medientyp zu überprüfen. Außerdem wird [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) für den upstreamfilter aufgerufen. Dadurch wird sichergestellt, dass die Eingabe-PIN den Medientyp entsprechend ändern kann.
3.  Mit der Ausgabe-PIN wird die [**checkinputtype**](ctransformfilter-checkinputtype.md) -Methode des Filters aufgerufen, um den Medientyp zu überprüfen. Außerdem wird [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) für den upstreamfilter aufgerufen. Dadurch wird sichergestellt, dass die Eingabe-PIN den Medientyp entsprechend ändern kann.
4.  Dieses Mal gibt die [**getallocator**](ctransinplaceinputpin-getallocator.md) -Methode der Eingabe-PIN die Downstream-Zuweisung zurück, und [**getallocatorrequirements**](ctransinplaceinputpin--getallocatorrequirements.md) gibt die zuordneranforderungen des Downstream-Filters zurück. Die eingabepin akzeptiert die Zuordnung, die der Upstream-Filter auswählt.
5.  Dieses Mal gibt die [**getallocator**](ctransinplaceinputpin-getallocator.md) -Methode der Eingabe-PIN die Downstream-Zuweisung zurück, und [**getallocatorrequirements**](ctransinplaceinputpin--getallocatorrequirements.md) gibt die zuordneranforderungen des Downstream-Filters zurück. Die eingabepin akzeptiert die Zuordnung, die der Upstream-Filter auswählt.

Sehen Sie sich nun das umgekehrte Szenario an, in dem die Ausgabepin die erste PIN für die Verbindung ist.

1.  Mit der Ausgabe-PIN wird die [**checkinputtype**](ctransformfilter-checkinputtype.md) -Methode des Filters aufgerufen, um den Medientyp zu überprüfen.
2.  Es wählt einen Zuweiser aus, und bevorzugt die Zuweisung des nachgelagerten Filters.

Wenn die Eingabe-PIN eine Verbindung herstellt:

1.  Die Eingabe-PIN überprüft den Medientyp durch Aufrufen von [**checkinputtype**](ctransformfilter-checkinputtype.md) für den Filter und durch Aufrufen von [**queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) für den Ausgabepin des downstreamfilters.
2.  Wenn der Eingabetyp nicht mit dem Ausgabetyp identisch ist, verbindet der Filter die Ausgabepin erneut.
3.  Der upstreamfilter wählt einen Zuweiser aus. Die [**getallocator**](ctransinplaceinputpin-getallocator.md) -Methode der Eingabe-PIN gibt die Downstream-Zuweisung zurück, und die Eingabe-PIN akzeptiert den vom upstreamfilter ausgewählten Zuweiser.
4.  Der Filter verwendet die gleiche Zuweisung für die Downstreamverbindung und kann möglicherweise die ursprüngliche Downstream-Zuweisung überschreiben.

Diese Abfolge von Ereignissen ändert sich geringfügig, wenn eine der beteiligten Zuweisungen schreibgeschützt ist, da der Downstream-Zuweisungs Vorgang beschreibbar sein muss. In diesem Fall verwendet der Filter möglicherweise zwei separate Zuweisungen.

Weitere Informationen zum Verwenden dieser Klasse finden Sie unter [Schreiben von Transformations Filtern](writing-transform-filters.md).



| Geschützte Member-Variablen                                                        | BESCHREIBUNG                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**m \_ bmodifiesdata**](ctransinplacefilter-m-bmodifiesdata.md)                   | Gibt an, ob der Filter die Beispiel Daten ändert.                           |
| Geschützte Methoden                                                                 | BESCHREIBUNG                                                                      |
| [**Kopieren**](ctransinplacefilter-copy.md)                                          | Kopiert ein Medien Beispiel.                                                           |
| [**InputPin**](ctransinplacefilter-inputpin.md)                                  | Ruft einen Zeiger auf die Eingabe-PIN des Filters ab.                                   |
| [**OutputPin**](ctransinplacefilter-outputpin.md)                                | Ruft einen Zeiger auf den Ausgabepin des Filters ab.                                  |
| [**Typesmatch**](ctransinplacefilter-typesmatch.md)                              | Bestimmt, ob der Eingabe Medientyp mit dem Ausgabe Medientyp übereinstimmt.           |
| [**Usingdifferenentzuweisungen**](ctransinplacefilter--usingdifferentallocators.md) | Bestimmt, ob die Eingabe-und Ausgabe Pins verschiedene Zuweisungen verwenden.     |
| Öffentliche Methoden                                                                    | BESCHREIBUNG                                                                      |
| [**Ctransinplacefilter**](ctransinplacefilter-ctransinplacefilter.md)            | Konstruktormethode.                                                              |
| [**Getpin**](ctransinplacefilter-getpin.md)                                      | Ruft eine PIN ab.                                                                 |
| [**Getmediatype**](ctransinplacefilter-getmediatype.md)                          | Ruft einen bevorzugten Medientyp für die Ausgabepin ab.                             |
| [**Decidebuffersize**](ctransinplacefilter-decidebuffersize.md)                  | Legt die Puffer Anforderungen der Ausgabe-PIN fest.                                       |
| [**Checktransform**](ctransinplacefilter-checktransform.md)                      | Überprüft, ob ein Eingabe Medientyp mit einem Ausgabe Medientyp kompatibel ist.      |
| [**Completeconnect**](ctransinplacefilter-completeconnect.md)                    | Schließt eine PIN-Verbindung ab.                                                      |
| [**Medizinisch**](ctransinplacefilter-receive.md)                                    | Empfängt ein Medien Beispiel, verarbeitet es und übergibt es an den downstreamfilter. |
| Reine virtuelle Methoden                                                              | BESCHREIBUNG                                                                      |
| [**Transform**](ctransinplacefilter-transform.md)                                | Transformiert ein Beispiel direkt.                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




