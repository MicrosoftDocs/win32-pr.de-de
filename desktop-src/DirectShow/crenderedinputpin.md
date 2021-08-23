---
description: Die CRenderedInputPin-Klasse ist eine Basisklasse zum Implementieren eines Eingabepins auf einem Renderer.
ms.assetid: 644dc6ef-eefa-4dfa-a27e-cab690b6e1db
title: CRenderedInputPin-Klasse (Amextra.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 139b0ebd887dc81efd19953d48f3caa8fd6377acde8723de23178ee7a0278c8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585295"
---
# <a name="crenderedinputpin-class"></a>CRenderedInputPin-Klasse

![crenderedinputpin-Klassenhierarchie](images/rbase04.png)

Die **CRenderedInputPin-Klasse** ist eine Basisklasse zum Implementieren eines Eingabepins auf einem Renderer. Diese Klasse ist für Rendererfilter konzipiert, die nicht von der [**CBaseRenderer-Klasse ableiten.**](cbaserenderer.md) (Filter, die von **CBaseRenderer ableiten,** sollten die [**CRendererInputPin-Klasse**](crendererinputpin.md) für den Eingabepin verwenden.)

Um diese Klasse verwenden zu können, müssen Sie mindestens folgende Schritte unternehmen:

-   Deklarieren Sie eine neue PIN-Klasse, die **CRenderedInputPin erbt.**
-   Deklarieren Sie in Ihrer Pin-Klasse ein kritisches Abschnittsobjekt, um die Streamingsperre zu halten. Zu diesem Zweck [**können Sie die CCritSec-Klasse**](ccritsec.md) verwenden. Weitere Informationen finden Sie unter [Threads und kritische Abschnitte](threads-and-critical-sections.md).
-   Überschreiben [**Sie CRenderedInputPin::EndOfStream,**](crenderedinputpin-endofstream.md) um die Streamingsperre zu halten.
-   Implementieren Sie [**die Methoden IMemInputPin::Receive,**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)und [**CBasePin::GetMediaType.**](cbasepin-getmediatype.md)
-   Implementieren Sie in Ihrem Filter [**CBaseFilter::GetPin,**](cbasefilter-getpin.md) um eine Instanz Ihrer Pin-Klasse zurück zu geben.

Sie können diese Klasse in einem Renderer verwenden, der über mehrere Eingabepins verfügt. Diese Klasse erbt die [**CBaseInputPin-Klasse.**](cbaseinputpin.md)



| Geschützte Membervariablen                                            | Beschreibung                                                                                                  |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**m \_ bAtEndOfStream**](crenderedinputpin-m-batendofstream.md)       | Gibt an, ob das Ende des Streams erreicht wurde.                                                         |
| [**m \_ bCompleteNomost**](crenderedinputpin-m-bcompletenotified.md) | Gibt an, ob der Pin ein [**EC \_ COMPLETE-Ereignis**](ec-complete.md) an den Filter-Graph gesendet hat. |
| Öffentliche Methoden                                                        | Beschreibung                                                                                                  |
| [**Aktiv**](crenderedinputpin-active.md)                            | Benachrichtigt den Pin, dass der Filter jetzt aktiv ist.                                                              |
| [**CRenderedInputPin**](crenderedinputpin-crenderedinputpin.md)      | Konstruktormethode.                                                                                          |
| [**Ausführung**](crenderedinputpin-run.md)                                  | Benachrichtigt den Pin, dass der Filter jetzt ausgeführt wird.                                                             |
| IPin-Methoden                                                          | Beschreibung                                                                                                  |
| [**EndFlush**](crenderedinputpin-endflush.md)                        | Beendet einen Leerungsvorgang.                                                                                      |
| [**EndOfStream**](crenderedinputpin-endofstream.md)                  | Benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden, bis der Filter einen neuen Ausführungsbefehl empfängt.            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amextra.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




