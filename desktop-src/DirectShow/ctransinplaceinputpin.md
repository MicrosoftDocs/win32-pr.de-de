---
description: Die CTransInPlaceInputPin-Klasse implementiert einen Eingabepin, der von der CTransInPlaceFilter-Klasse verwendet wird.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: CTransInPlaceInputPin-Klasse (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04d30b18d115e7ef03e88deb47355bafc795532a91afa14cf2f4392e658954f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076195"
---
# <a name="ctransinplaceinputpin-class"></a>CTransInPlaceInputPin-Klasse

![ctransinplaceinputpin-Klassenhierarchie](images/tsip01.png)

Die `CTransInPlaceInputPin` -Klasse implementiert einen Eingabepin, der von der [**CTransInPlaceFilter-Klasse verwendet**](ctransinplacefilter.md) wird.

In der Regel müssen Sie nicht von dieser Klasse ableiten. In diesem Fall müssen Sie die [**CTransInPlaceFilter::GetPin-Methode**](ctransinplacefilter-getpin.md) des Filters überschreiben, um Instanzen der abgeleiteten Klasse zu erstellen.



| Geschützte Membervariablen                                                          | BESCHREIBUNG                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**m \_ bReadOnly**](ctransinplaceinputpin-m-breadonly.md)                           | Flag, das angibt, ob der Eingabestream schreibgeschützt ist. |
| [**m \_ pTIPFilter**](ctransinplaceinputpin-m-ptipfilter.md)                         | Zeiger auf den Filter, der diesen Pin erstellt hat.               |
| Öffentliche Methoden                                                                      | BESCHREIBUNG                                                |
| [**CTransInPlaceInputPin**](ctransinplaceinputpin-ctransinplaceinputpin.md)        | Konstruktormethode.                                        |
| [**CheckMediaType**](ctransinplaceinputpin-checkmediatype.md)                      | Bestimmt, ob die Stecknadel einen bestimmten Medientyp akzeptiert.       |
| [**PeekAllocator**](ctransinplaceinputpin-peekallocator.md)                        | Ruft einen Zeiger auf die Zuweisung des Pins ab.                |
| [**Readonly**](ctransinplaceinputpin-readonly.md)                                  | Gibt an, ob der Eingabestream schreibgeschützt ist.           |
| IPin-Methoden                                                                        | BESCHREIBUNG                                                |
| [**EnumMediaTypes**](ctransinplaceinputpin-enummediatypes.md)                      | Enumeriert die bevorzugten Medientypen des Pins.                |
| IMemInputPin-Methoden                                                                | BESCHREIBUNG                                                |
| [**GetAllocator**](ctransinplaceinputpin-getallocator.md)                          | Ruft die von diesem Pin vorgeschlagene Speicherzuweisung ab.       |
| [**NotifyAllocator**](ctransinplaceinputpin-notifyallocator.md)                    | Gibt eine Zuweisung für die Verbindung an.                 |
| [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) | Ruft die vom Pin angeforderten Zuweisungseigenschaften ab.   |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




