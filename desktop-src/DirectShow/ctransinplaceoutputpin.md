---
description: Die CTransInPlaceOutputPin-Klasse implementiert einen Ausgabepin, der von der CTransInPlaceFilter-Klasse verwendet wird.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: CTransInPlaceOutputPin-Klasse (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2462843f9ad42793a9e0666dd96aaf7387a1f5f0f1749f97cc4e2ca4d3ed051a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076154"
---
# <a name="ctransinplaceoutputpin-class"></a>CTransInPlaceOutputPin-Klasse

![ctransinplaceoutputpin-Klassenhierarchie](images/tsip02.png)

Die `CTransInPlaceOutputPin` -Klasse implementiert einen Ausgabepin, der von der [**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md) verwendet wird.

In der Regel müssen Sie nicht von dieser Klasse ableiten. In diesem Fall müssen Sie die [**CTransInPlaceFilter::GetPin-Methode**](ctransinplacefilter-getpin.md) des Filters überschreiben, um Instanzen der abgeleiteten Klasse zu erstellen.



| Geschützte Membervariablen                                                      | BESCHREIBUNG                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [**m \_ pTIPFilter**](ctransinplaceoutputpin-m-ptipfilter.md)                    | Zeiger auf den Filter, der diese Stecknadel erstellt hat.         |
| Öffentliche Methoden                                                                  | BESCHREIBUNG                                          |
| [**CTransInPlaceOutputPin**](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | Konstruktormethode.                                  |
| [**CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md)                 | Bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert. |
| [**SetAllocator**](ctransinplaceoutputpin-setallocator.md)                     | Gibt eine Zuweisung für die Verbindung an.           |
| [**ConnectedIMemInputPin**](ctransinplaceoutputpin-connectedimeminputpin.md)   | Ruft einen Zeiger auf den nachgeschalteten Eingabepin ab.     |
| [**PeekAllocator**](ctransinplaceoutputpin-peekallocator.md)                   | Ruft einen Zeiger auf die Zuweisung des Stecknadels ab.          |
| IPin-Methoden                                                                    | BESCHREIBUNG                                          |
| [**EnumMediaTypes**](ctransinplaceoutputpin-enummediatypes.md)                 | Listet die bevorzugten Medientypen des Pins auf.          |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




