---
description: Die CTransformInputPin-Klasse implementiert einen Eingabepin, der von der CTransformFilter-Klasse verwendet wird.
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: CTransformInputPin-Klasse (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3df5da0ee6e80dd1da147563ef698a520222531de5cee9656ec52cb14301f66e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087014"
---
# <a name="ctransforminputpin-class"></a>CTransformInputPin-Klasse

![ctransforminputpin-Klassenhierarchie](images/tfrm01.png)

Die `CTransformInputPin` -Klasse implementiert einen Eingabepin, der von der [**CTransformFilter-Klasse verwendet**](ctransformfilter.md) wird.

In der Regel müssen Sie nicht von dieser Klasse ableiten. Die meisten Methoden in dieser Klasse rufen entsprechende Methoden für die **CTransformFilter-Klasse** auf, die Sie überschreiben können. Wenn Sie von dieser Klasse ableiten, müssen Sie die [**CTransformFilter::GetPin-Methode**](ctransformfilter-getpin.md) des Filters überschreiben, um Instanzen der abgeleiteten Klasse zu erstellen.



| Geschützte Membervariablen                                           | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ pTransformFilter**](ctransforminputpin-m-ptransformfilter.md) | Zeiger auf den besitzenden Filter.                                                          |
| Öffentliche Methoden                                                       | BESCHREIBUNG                                                                            |
| [**CTransformInputPin**](ctransforminputpin-ctransforminputpin.md)  | Konstruktormethode.                                                                    |
| [**CheckConnect**](ctransforminputpin-checkconnect.md)              | Bestimmt, ob eine Stecknadelverbindung geeignet ist.                                       |
| [**BreakConnect**](ctransforminputpin-breakconnect.md)              | Gibt den Pin von einer Verbindung frei.                                                    |
| [**CompleteConnect**](ctransforminputpin-completeconnect.md)        | Schließt eine Verbindung mit einem anderen Pin ab.                                                 |
| [**CheckMediaType**](ctransforminputpin-checkmediatype.md)          | Bestimmt, ob die Stecknadel einen bestimmten Medientyp akzeptiert.                                   |
| [**SetMediaType**](ctransforminputpin-setmediatype.md)              | Legt den Medientyp für die Verbindung fest.                                                |
| [**CheckStreaming**](ctransforminputpin-checkstreaming.md)          | Bestimmt, ob der Pin Stichproben akzeptieren kann. Virtuellen.                                |
| [**CurrentMediaType**](ctransforminputpin-currentmediatype.md)      | Ruft den Medientyp für die aktuelle Pinverbindung ab.                               |
| IPin-Methoden                                                         | BESCHREIBUNG                                                                            |
| [**QueryId**](ctransforminputpin-queryid.md)                        | Ruft einen Bezeichner für den Pin ab.                                                   |
| [**EndOfStream**](ctransforminputpin-endofstream.md)                | Benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden.                                  |
| [**BeginFlush**](ctransforminputpin-beginflush.md)                  | Startet einen Leerungsvorgang.                                                              |
| [**EndFlush**](ctransforminputpin-endflush.md)                      | Beendet einen Leerungsvorgang.                                                                |
| [**NewSegment**](ctransforminputpin-newsegment.md)                  | Benachrichtigt den Pin, dass medienbeispiele, die nach diesem Aufruf empfangen wurden, als Segment gruppiert werden. |
| IMemInputPin-Methoden                                                 | BESCHREIBUNG                                                                            |
| [**Erhalten**](ctransforminputpin-receive.md)                        | Empfängt das nächste Medienbeispiel im Stream.                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




