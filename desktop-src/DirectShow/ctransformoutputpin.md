---
description: Die CTransformOutputPin-Klasse implementiert einen Ausgabepin, der von der CTransformFilter-Klasse verwendet wird.
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: CTransformOutputPin-Klasse (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f99b0d03eb3b2b1ac63c69620346e4db663c75730ff773de2fb1429b268aefb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756785"
---
# <a name="ctransformoutputpin-class"></a>CTransformOutputPin-Klasse

![ctransformoutputpin-Klassenhierarchie](images/tfrm02.png)

Die `CTransformOutputPin` -Klasse implementiert einen Ausgabepin, der von der [**CTransformFilter-Klasse**](ctransformfilter.md) verwendet wird.

In der Regel müssen Sie nicht von dieser Klasse ableiten. Die meisten Methoden in dieser Klasse rufen entsprechende Methoden für die **CTransformFilter-Klasse** auf, die Sie überschreiben können. Wenn Sie von dieser Klasse ableiten, müssen Sie die [**CTransformFilter::GetPin-Methode**](ctransformfilter-getpin.md) des Filters überschreiben, um Instanzen Ihrer abgeleiteten Klasse zu erstellen.

Diese Klasse macht die **Schnittstellen IMediaSeeking** und **IMediaPosition** über das [**CPosPassThru-Objekt**](cpospassthru.md) verfügbar. Er übergibt alle Suchanforderungen an den nächsten Filter upstream.



| Geschützte Membervariablen                                               | Beschreibung                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**m \_ pTransformFilter**](ctransformoutputpin-m-ptransformfilter.md)    | Zeiger auf den besitzenden Filter.                            |
| Öffentliche Membervariablen                                                  | Beschreibung                                              |
| [**m \_ pPosition**](ctransformoutputpin-m-pposition.md)                  | Hilfsobjekt zum Übergeben von Suchbefehlen upstream.            |
| Öffentliche Methoden                                                           | Beschreibung                                              |
| [**CTransformOutputPin**](ctransformoutputpin-ctransformoutputpin.md)   | Konstruktormethode.                                      |
| [**~CTransformOutputPin**](ctransformoutputpin--ctransformoutputpin.md) | Destruktormethode.                                       |
| [**CheckConnect**](ctransformoutputpin-checkconnect.md)                 | Bestimmt, ob eine Stecknadelverbindung geeignet ist.         |
| [**BreakConnect**](ctransformoutputpin-breakconnect.md)                 | Gibt den Pin von einer Verbindung frei.                      |
| [**CompleteConnect**](ctransformoutputpin-completeconnect.md)           | Schließt eine Verbindung mit einem anderen Pin ab.                   |
| [**CheckMediaType**](ctransformoutputpin-checkmediatype.md)             | Bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.     |
| [**SetMediaType**](ctransformoutputpin-setmediatype.md)                 | Legt den Medientyp für die Verbindung fest.                  |
| [**DecideBufferSize**](ctransformoutputpin-decidebuffersize.md)         | Legt die Pufferanforderungen fest.                            |
| [**GetMediaType**](ctransformoutputpin-getmediatype.md)                 | Ruft einen bevorzugten Medientyp nach Indexwert ab.        |
| [**CurrentMediaType**](ctransformoutputpin-currentmediatype.md)         | Ruft den Medientyp für die aktuelle Pinverbindung ab. |
| IPin-Methoden                                                             | Beschreibung                                              |
| [**QueryId**](ctransformoutputpin-queryid.md)                           | Ruft einen Bezeichner für den Stecknadel ab.                     |
| IQualityControl-Methoden                                                  | Beschreibung                                              |
| [**Benachrichtigen**](ctransformoutputpin-notify.md)                             | Benachrichtigt den Pin, dass eine Qualitätsänderung angefordert wird.     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




