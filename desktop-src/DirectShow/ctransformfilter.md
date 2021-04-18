---
description: Die ctransformfilter-Klasse ist eine Basisklasse zum Implementieren von Transformations filtern.
ms.assetid: 99db8252-a8db-4995-b4be-a6cf944be869
title: Ctransformfilter-Klasse (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d24c305b28641fcee366b4e906b87008decac014
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368350"
---
# <a name="ctransformfilter-class"></a>Ctransformfilter-Klasse

![ctransformfilter-Klassenhierarchie](images/tfrm03.png)

Die- `CTransformFilter` Klasse ist eine Basisklasse zum Implementieren von Transformations filtern. Diese Klasse ist für die Implementierung eines Transformations Filters mit einer Eingabe-und einer Ausgabe-PIN konzipiert. Dabei werden separate Zuweisungen für die Eingabe-und die Ausgabepin verwendet. Verwenden Sie zum Erstellen eines Filters, der Daten an Ort und Stelle verarbeitet, die [**ctransinplacefilter**](ctransinplacefilter.md) -Klasse.

Dieser Filter verwendet die [**ctransforminputpin**](ctransforminputpin.md) -Klasse für seine Eingabe-PIN und die [**ctransformoutputpin**](ctransformoutputpin.md) -Klasse für die Ausgabepin. In der Regel müssen Sie diese Pin-Klassen nicht überschreiben. In den meisten der PIN-Methoden werden die entsprechenden Methoden für die `CTransformFilter` Klasse aufgerufen, sodass Sie ggf. die Filter Methoden überschreiben können. Der Filter erstellt beide Pins in der [**ctransformfilter:: getpin**](ctransformfilter-getpin.md) -Methode. Wenn Sie die PIN-Klassen überschreiben, müssen Sie **getpin** überschreiben, um Ihre benutzerdefinierten Pins zu erstellen.

Um diese Klasse zu verwenden, leiten Sie eine neue Klasse von ab, `CTransformFilter` und implementieren Sie die folgenden Methoden:

-   [**Ctransformfilter:: checkinputtype**](ctransformfilter-checkinputtype.md)
-   [**Ctransformfilter:: checktransform**](ctransformfilter-checktransform.md)
-   [**Ctransformfilter::D ecidebuffersize**](ctransformfilter-decidebuffersize.md)
-   [**Ctransformfilter:: getmediatype**](ctransformfilter-getmediatype.md)
-   [**Ctransformfilter:: Transform**](ctransformfilter-transform.md)

Abhängig von den Anforderungen Ihres Filters müssen Sie möglicherweise auch andere Methoden außer Kraft setzen.

## <a name="media-types"></a>Medientypen

Mit der Eingabe-PIN dieses Filters werden keine Medientypen vorgeschlagen. Er basiert auf dem Upstream-Filter, um die Medientypen für die Verbindung vorzuschlagen. Der Grund für diesen Entwurf ist, dass der upstreamfilter in den meisten Fällen weitere Informationen über das Format bereitstellen kann. Der upstreamfilter kennt z. b. die Video Abmessungen und die Framerate, während der Transformations Filter keine Möglichkeit hat, diese Informationen zu bestimmen. Wenn Sie dieses Verhalten ändern möchten, überschreiben Sie die [**getmediatype**](ctransformfilter-getmediatype.md) -Methode der Eingabe-PIN. Wenn der upstreamfilter einen Medientyp vorschlägt, ruft die Eingabe-PIN die [**checkinputtype**](ctransformfilter-checkinputtype.md) -Methode des Filters auf (rein virtuell).

Bis die Eingabe-PIN verbunden ist, lehnt die Ausgabe-PIN alle Verbindungen ab und gibt keine bevorzugten Medientypen zurück. Nachdem die Eingabe-PIN verbunden ist, gibt die Ausgabe-PIN eine Liste der bevorzugten Typen zurück, indem die [**getmediatype**](ctransformfilter-getmediatype.md) -Methode des Filters aufgerufen wird. Er überprüft die Ausgabetypen für die Verbindung über die [**checktransform**](ctransformfilter-checktransform.md) -Methode des Filters. (Beide Methoden sind rein virtuell.) In der Regel bestimmt der Eingabetyp teilweise die zulässigen Ausgabetypen.

Abhängig vom Filter sollten Sie möglicherweise einige der unterstützten Medientypen des Filters registrieren, damit das [Filter Mapper](filter-mapper.md) -Objekt den Filter finden kann. Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md).

## <a name="streaming"></a>Streaming

Diese Klasse fügt die Ausgabedaten nicht in die Warteschlange ein. Jedes Ausgabe Beispiel wird innerhalb der [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode übermittelt. Die **Receive** -Methode ruft die [**Transformations**](ctransformfilter-transform.md) Methode des Filters (auch rein virtuell) auf, um die Daten zu verarbeiten.

Weitere Informationen zum Verwenden dieser Klasse finden Sie unter [Schreiben von Transformations Filtern](writing-transform-filters.md).



| Geschützte Member-Variablen                                                | BESCHREIBUNG                                                                                             |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**m \_ BeOS übermittelt**](ctransformfilter-m-beosdelivered.md)              | Flag, das angibt, ob der Filter eine Benachrichtigung über das Ende des Datenstroms gesendet hat.                          |
| [**m \_ bsampleskipped**](ctransformfilter-m-bsampleskipped.md)            | Flag, das angibt, ob das letzte Beispiel gelöscht wurde.                                         |
| [**m \_ bqualitychanged**](ctransformfilter-m-bqualitychanged.md)          | Flag, das angibt, ob sich die Qualität geändert hat.                                                    |
| [**m \_ CSFilter**](ctransformfilter-m-csfilter.md)                        | Kritischer Abschnitt, der den Filter Zustand schützt.                                                        |
| [**m \_ csreceive**](ctransformfilter-m-csreceive.md)                      | Kritischer Abschnitt, der den streamingstatus schützt.                                                     |
| [**m \_ pinput**](ctransformfilter-m-pinput.md)                            | Zeiger auf die eingabepin.                                                                               |
| [**m \_ poutput**](ctransformfilter-m-poutput.md)                          | Zeiger auf den Ausgabepin.                                                                              |
| Öffentliche Methoden                                                            | BESCHREIBUNG                                                                                             |
| [**Ctransformfilter**](ctransformfilter-ctransformfilter.md)             | Konstruktormethode.                                                                                     |
| [**~ Ctransformfilter**](ctransformfilter--ctransformfilter.md)          | Dekonstruktormethode.                                                                                      |
| [**Getpincount**](ctransformfilter-getpincount.md)                       | Ruft die Anzahl der Pins für den Filter ab. Virtu.                                                    |
| [**Getpin**](ctransformfilter-getpin.md)                                 | Ruft eine PIN ab. Virtu.                                                                               |
| [**Transform**](ctransformfilter-transform.md)                           | Transformiert ein Eingabe Beispiel, um ein Ausgabe Beispiel zu erhalten. Virtu.                                        |
| [**Startstreaming**](ctransformfilter-startstreaming.md)                 | Wird aufgerufen, wenn der Filter in den angehaltenen Zustand wechselt. Virtu.                                           |
| [**Stopstreaming**](ctransformfilter-stopstreaming.md)                   | Wird aufgerufen, wenn der Filter in den Zustand "beendet" wechselt. Virtu.                                          |
| [**Alterquality**](ctransformfilter-alterquality.md)                     | Benachrichtigt den Filter, dass eine Qualitätsänderung angefordert wird. Virtu.                                        |
| [**Setmediatype**](ctransformfilter-setmediatype.md)                     | Wird aufgerufen, wenn der Medientyp für einen der Pins des Filters festgelegt wird. Virtu.                                 |
| [**Check Connect**](ctransformfilter-checkconnect.md)                     | Bestimmt, ob eine PIN-Verbindung geeignet ist. Virtu.                                               |
| [**Breakconnect**](ctransformfilter-breakconnect.md)                     | Gibt eine PIN von einer Verbindung frei. Virtu.                                                              |
| [**Completeconnect**](ctransformfilter-completeconnect.md)               | Schließt eine PIN-Verbindung ab. Virtu.                                                                    |
| [**Medizinisch**](ctransformfilter-receive.md)                               | Empfängt ein Medien Beispiel, verarbeitet es und stellt ein Ausgabe Beispiel für den downstreamfilter bereit. Virtu. |
| [**Initializeoutputsample**](ctransformfilter-initializeoutputsample.md) | Ruft ein neues Ausgabe Beispiel ab und initialisiert es.                                                       |
| [**EndOfStream**](ctransformfilter-endofstream.md)                       | Benachrichtigt den Filter, dass keine weiteren Daten von der eingabepin erwartet werden. Virtu.                    |
| [**Beginflush**](ctransformfilter-beginflush.md)                         | Startet einen Löschvorgang. Virtu.                                                                      |
| [**Endflush**](ctransformfilter-endflush.md)                             | Beendet einen Löschvorgang. Virtu.                                                                        |
| [**Newsegment**](ctransformfilter-newsegment.md)                         | Benachrichtigt den Filter, dass nach diesem-Befehl empfangene Medien Beispiele als Segment gruppiert werden. Virtu.      |
| Reine virtuelle Methoden                                                      | BESCHREIBUNG                                                                                             |
| [**Checkinputtype**](ctransformfilter-checkinputtype.md)                 | Überprüft, ob ein angegebener Medientyp für die Eingabe zulässig ist.                                          |
| [**Checktransform**](ctransformfilter-checktransform.md)                 | Überprüft, ob ein Eingabe Medientyp mit einem Ausgabe Medientyp kompatibel ist.                             |
| [**Decidebuffersize**](ctransformfilter-decidebuffersize.md)             | Legt die Puffer Anforderungen der Ausgabe-PIN fest.                                                              |
| [**Getmediatype**](ctransformfilter-getmediatype.md)                     | Ruft einen bevorzugten Medientyp für die Ausgabepin ab.                                                    |
| Imediafilter-Methoden                                                      | BESCHREIBUNG                                                                                             |
| [**Stop**](ctransformfilter-stop.md)                                     | Beendet den Filter.                                                                                       |
| [**Anhalten**](ctransformfilter-pause.md)                                   | Hält den Filter an.                                                                                      |
| Ibasefilter-Methoden                                                       | BESCHREIBUNG                                                                                             |
| [**Findpin**](ctransformfilter-findpin.md)                               | Ruft die PIN mit dem angegebenen Bezeichner ab.                                                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




