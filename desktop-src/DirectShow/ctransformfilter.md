---
description: Die CTransformFilter-Klasse ist eine Basisklasse zum Implementieren von Transformationsfiltern.
ms.assetid: 99db8252-a8db-4995-b4be-a6cf944be869
title: CTransformFilter-Klasse (Transfrm.h)
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
ms.openlocfilehash: 9d199a406fa1934fb63625cd258baee8d69c20c17992a7d1d3bbd2c83956a1f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633894"
---
# <a name="ctransformfilter-class"></a>CTransformFilter-Klasse

![ctransformfilter-Klassenhierarchie](images/tfrm03.png)

Die `CTransformFilter` -Klasse ist eine Basisklasse zum Implementieren von Transformationsfiltern. Diese Klasse ist für die Implementierung eines Transformationsfilters mit einem Eingabepin und einem Ausgabepin konzipiert. Es werden separate Zuweisungen für den Eingabepin und den Ausgabepin verwendet. Um einen Filter zu erstellen, der Daten direkt verarbeitet, verwenden Sie die [**CTransInPlaceFilter-Klasse.**](ctransinplacefilter.md)

Dieser Filter verwendet die [**CTransformInputPin-Klasse**](ctransforminputpin.md) für den Eingabepin und die [**CTransformOutputPin-Klasse**](ctransformoutputpin.md) für den Ausgabepin. In der Regel müssen Sie diese Pinklassen nicht überschreiben. Die meisten pin-Methoden rufen entsprechende Methoden für die -Klasse `CTransformFilter` auf, sodass Sie die Filtermethoden bei Bedarf überschreiben können. Der Filter erstellt beide Pins in der [**CTransformFilter::GetPin-Methode.**](ctransformfilter-getpin.md) Wenn Sie die Pinklassen überschreiben, müssen Sie **GetPin überschreiben,** um Ihre benutzerdefinierten Pins zu erstellen.

Um diese Klasse zu verwenden, leiten Sie eine neue Klasse von ab `CTransformFilter` und implementieren die folgenden Methoden:

-   [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md)
-   [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md)
-   [**CTransformFilter::D ecideBufferSize**](ctransformfilter-decidebuffersize.md)
-   [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md)
-   [**CTransformFilter::Transform**](ctransformfilter-transform.md)

Abhängig von den Anforderungen Ihres Filters müssen Sie möglicherweise auch andere Methoden überschreiben.

## <a name="media-types"></a>Medientypen

Der Eingabepin dieses Filters schlägt keine Medientypen vor. es basiert auf dem Upstreamfilter, um die Medientypen für die Verbindung vorzuschlagen. Der Grund für diesen Entwurf ist, dass der Upstreamfilter in den meisten Fällen weitere Informationen zum Format bereitstellen kann. Bei Videoformaten kennt der Upstreamfilter beispielsweise die Videodimensionen und die Bildfrequenz, während der Transformationsfilter keine Möglichkeit hat, diese Informationen zu bestimmen. Wenn Sie dieses Verhalten ändern möchten, überschreiben Sie die [**GetMediaType-Methode**](ctransformfilter-getmediatype.md) des Eingabepins. Wenn der Upstreamfilter einen Medientyp vorschlägt, ruft der Eingabepin die [**CheckInputType-Methode**](ctransformfilter-checkinputtype.md) des Filters (rein virtuell) auf.

Solange der Eingabepin nicht verbunden ist, verweigert der Ausgabepin alle Verbindungen und gibt keine bevorzugten Medientypen zurück. Nachdem der Eingabepin verbunden wurde, gibt der Ausgabepin eine Liste der bevorzugten Typen zurück, indem die [**GetMediaType-Methode**](ctransformfilter-getmediatype.md) des Filters aufruft. Die Ausgabetypen für die Verbindung werden über die [**CheckTransform-Methode**](ctransformfilter-checktransform.md) des Filters überprüft. (Beide Methoden sind rein virtuell.) In der Regel bestimmt der Eingabetyp teilweise die zulässigen Ausgabetypen.

Je nach Filter können Sie einige der vom Filter unterstützten Medientypen registrieren, damit das [Filterzuordnungsobjekt](filter-mapper.md) ihren Filter finden kann. Weitere Informationen finden Sie unter [Registrieren von DirectShow-Filtern.](how-to-register-directshow-filters.md)

## <a name="streaming"></a>Streaming

Diese Klasse stellt die Ausgabedaten nicht in die Warteschlange. Jedes Ausgabebeispiel wird innerhalb der [**IMemInputPin::Receive-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) übermittelt. Die **Receive-Methode** ruft die [**Transformationsmethode**](ctransformfilter-transform.md) des Filters (auch rein virtuell) auf, um die Daten zu verarbeiten.

Weitere Informationen zur Verwendung dieser Klasse finden Sie unter Writing Transform Filters ( [Schreiben von Transformationsfiltern](writing-transform-filters.md)).



| Geschützte Membervariablen                                                | Beschreibung                                                                                             |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**m \_ bEOSDelivered**](ctransformfilter-m-beosdelivered.md)              | Flag, das angibt, ob der Filter eine Benachrichtigung zum Streamende gesendet hat.                          |
| [**m \_ bSampleSkipped**](ctransformfilter-m-bsampleskipped.md)            | Flag, das angibt, ob das letzte Beispiel gelöscht wurde.                                         |
| [**m \_ bQualityChanged**](ctransformfilter-m-bqualitychanged.md)          | Flag, das angibt, ob sich die Qualität geändert hat.                                                    |
| [**m \_ csFilter**](ctransformfilter-m-csfilter.md)                        | Kritischer Abschnitt, der den Filterzustand schützt.                                                        |
| [**m \_ csReceive**](ctransformfilter-m-csreceive.md)                      | Abschnitt "Kritisch", der den Streamingzustand schützt.                                                     |
| [**m \_ pInput**](ctransformfilter-m-pinput.md)                            | Zeiger auf den Eingabepin.                                                                               |
| [**m \_ pOutput**](ctransformfilter-m-poutput.md)                          | Zeiger auf den Ausgabepin.                                                                              |
| Öffentliche Methoden                                                            | Beschreibung                                                                                             |
| [**CTransformFilter**](ctransformfilter-ctransformfilter.md)             | Konstruktormethode.                                                                                     |
| [**~ CTransformFilter**](ctransformfilter--ctransformfilter.md)          | Destruktormethode.                                                                                      |
| [**GetPinCount**](ctransformfilter-getpincount.md)                       | Ruft die Anzahl der Stecknadeln im Filter ab. Virtuellen.                                                    |
| [**GetPin**](ctransformfilter-getpin.md)                                 | Ruft eine Stecknadel ab. Virtuellen.                                                                               |
| [**Transform**](ctransformfilter-transform.md)                           | Transformiert ein Eingabebeispiel, um ein Ausgabebeispiel zu erzeugen. Virtuellen.                                        |
| [**StartStreaming**](ctransformfilter-startstreaming.md)                 | Wird aufgerufen, wenn der Filter in den angehaltenen Zustand wechselt. Virtuellen.                                           |
| [**StopStreaming**](ctransformfilter-stopstreaming.md)                   | Wird aufgerufen, wenn der Filter in den Zustand "Beendet" wechselt. Virtuellen.                                          |
| [**AlterQuality**](ctransformfilter-alterquality.md)                     | Benachrichtigt den Filter, dass eine Qualitätsänderung angefordert wird. Virtuellen.                                        |
| [**SetMediaType**](ctransformfilter-setmediatype.md)                     | Wird aufgerufen, wenn der Medientyp an einem der Pins des Filters festgelegt wird. Virtuellen.                                 |
| [**CheckConnect**](ctransformfilter-checkconnect.md)                     | Bestimmt, ob eine Stecknadelverbindung geeignet ist. Virtuellen.                                               |
| [**BreakConnect**](ctransformfilter-breakconnect.md)                     | Gibt eine Stecknadel aus einer Verbindung frei. Virtuellen.                                                              |
| [**CompleteConnect**](ctransformfilter-completeconnect.md)               | Schließt eine Stecknadelverbindung ab. Virtuellen.                                                                    |
| [**Erhalten**](ctransformfilter-receive.md)                               | Empfängt ein Medienbeispiel, verarbeitet es und übergibt ein Ausgabebeispiel an den Downstreamfilter. Virtuellen. |
| [**InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) | Ruft ein neues Ausgabebeispiel ab und initialisiert es.                                                       |
| [**EndOfStream**](ctransformfilter-endofstream.md)                       | Benachrichtigt den Filter, dass keine zusätzlichen Daten vom Eingabepin erwartet werden. Virtuellen.                    |
| [**BeginFlush**](ctransformfilter-beginflush.md)                         | Startet einen Leerungsvorgang. Virtuellen.                                                                      |
| [**EndFlush**](ctransformfilter-endflush.md)                             | Beendet einen Leerungsvorgang. Virtuellen.                                                                        |
| [**NewSegment**](ctransformfilter-newsegment.md)                         | Benachrichtigt den Filter, dass medienbeispiele, die nach diesem Aufruf empfangen wurden, als Segment gruppiert werden. Virtuellen.      |
| Rein virtuelle Methoden                                                      | Beschreibung                                                                                             |
| [**CheckInputType**](ctransformfilter-checkinputtype.md)                 | Überprüft, ob ein angegebener Medientyp für die Eingabe akzeptabel ist.                                          |
| [**CheckTransform**](ctransformfilter-checktransform.md)                 | Überprüft, ob ein Eingabemedientyp mit einem Ausgabemedientyp kompatibel ist.                             |
| [**DecideBufferSize**](ctransformfilter-decidebuffersize.md)             | Legt die Pufferanforderungen des Ausgabepins fest.                                                              |
| [**GetMediaType**](ctransformfilter-getmediatype.md)                     | Ruft einen bevorzugten Medientyp für den Ausgabepin ab.                                                    |
| IMediaFilter-Methoden                                                      | Beschreibung                                                                                             |
| [**Beenden**](ctransformfilter-stop.md)                                     | Beendet den Filter.                                                                                       |
| [**Anhalten**](ctransformfilter-pause.md)                                   | Hält den Filter an.                                                                                      |
| IBaseFilter-Methoden                                                       | Beschreibung                                                                                             |
| [**FindPin**](ctransformfilter-findpin.md)                               | Ruft den Pin mit dem angegebenen Bezeichner ab.                                                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




