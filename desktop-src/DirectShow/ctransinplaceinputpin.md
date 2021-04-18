---
description: Die ctransinplaceinputpin-Klasse implementiert eine Eingabe-PIN, die von der ctransinplacefilter-Klasse verwendet wird.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: Ctransinplaceinputpin-Klasse (transip. h)
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
ms.openlocfilehash: 242e3c09a3fb569036a22b515d4da9c49b6178da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371026"
---
# <a name="ctransinplaceinputpin-class"></a>Ctransinplaceinputpin-Klasse

![ctransinplaceinputpin-Klassenhierarchie](images/tsip01.png)

Die- `CTransInPlaceInputPin` Klasse implementiert eine Eingabe-PIN, die von der [**ctransinplacefilter**](ctransinplacefilter.md) -Klasse verwendet wird.

In der Regel müssen Sie keine Ableitung von dieser Klasse durchführen. Wenn Sie dies tun, müssen Sie die [**ctransinplacefilter:: getpin**](ctransinplacefilter-getpin.md) -Methode des Filters überschreiben, um Instanzen ihrer abgeleiteten Klasse zu erstellen.



| Geschützte Member-Variablen                                                          | BESCHREIBUNG                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**\_nur m Brot**](ctransinplaceinputpin-m-breadonly.md)                           | Flag, das angibt, ob der Eingabestream schreibgeschützt ist. |
| [**m \_ ptipfilter**](ctransinplaceinputpin-m-ptipfilter.md)                         | Zeiger auf den Filter, der diese Pin erstellt hat.               |
| Öffentliche Methoden                                                                      | BESCHREIBUNG                                                |
| [**Ctransinplaceinputpin**](ctransinplaceinputpin-ctransinplaceinputpin.md)        | Konstruktormethode.                                        |
| [**Checkmediatype**](ctransinplaceinputpin-checkmediatype.md)                      | Bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.       |
| [**Peer Zuordnung**](ctransinplaceinputpin-peekallocator.md)                        | Ruft einen Zeiger auf die Zuweisung der PIN ab.                |
| [**ReadOnly**](ctransinplaceinputpin-readonly.md)                                  | Gibt an, ob der Eingabestream schreibgeschützt ist.           |
| IPin-Methoden                                                                        | BESCHREIBUNG                                                |
| [**Enummediatypes**](ctransinplaceinputpin-enummediatypes.md)                      | Listet die bevorzugten Medientypen der PIN auf.                |
| IMemInputPin-Methoden                                                                | BESCHREIBUNG                                                |
| [**Getallocator**](ctransinplaceinputpin-getallocator.md)                          | Ruft die von dieser Pin vorgeschlagene Speicherzuweisung ab.       |
| [**Notifyzukator**](ctransinplaceinputpin-notifyallocator.md)                    | Gibt eine Zuweisung für die Verbindung an.                 |
| [**Getalloserorrequirements**](ctransinplaceinputpin--getallocatorrequirements.md) | Ruft die von der PIN angeforderten zuordnereigenschaften ab.   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




