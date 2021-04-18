---
description: Die ctransinplaceoutputpin-Klasse implementiert eine Ausgabe-PIN, die von der ctransinplacefilter-Klasse verwendet wird.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: Ctransinplaceoutputpin-Klasse (transip. h)
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
ms.openlocfilehash: e41fbff07a9bdeb8990bbf3ddba6d9f7455d1bad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359289"
---
# <a name="ctransinplaceoutputpin-class"></a>Ctransinplaceoutputpin-Klasse

![ctransinplaceoutputpin-Klassenhierarchie](images/tsip02.png)

Die- `CTransInPlaceOutputPin` Klasse implementiert eine Ausgabe-PIN, die von der [**ctransinplacefilter**](ctransinplacefilter.md) -Klasse verwendet wird.

In der Regel müssen Sie keine Ableitung von dieser Klasse durchführen. Wenn Sie dies tun, müssen Sie die [**ctransinplacefilter:: getpin**](ctransinplacefilter-getpin.md) -Methode des Filters überschreiben, um Instanzen ihrer abgeleiteten Klasse zu erstellen.



| Geschützte Member-Variablen                                                      | BESCHREIBUNG                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [**m \_ ptipfilter**](ctransinplaceoutputpin-m-ptipfilter.md)                    | Zeiger auf den Filter, der diese Pin erstellt hat.         |
| Öffentliche Methoden                                                                  | BESCHREIBUNG                                          |
| [**Ctransinplaceoutputpin**](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | Konstruktormethode.                                  |
| [**Checkmediatype**](ctransinplaceoutputpin-checkmediatype.md)                 | Bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert. |
| [**"Stallocator"**](ctransinplaceoutputpin-setallocator.md)                     | Gibt eine Zuweisung für die Verbindung an.           |
| [**Connectedimeminputpin**](ctransinplaceoutputpin-connectedimeminputpin.md)   | Ruft einen Zeiger auf die nachgelagerte Eingabe-PIN ab.     |
| [**Peer Zuordnung**](ctransinplaceoutputpin-peekallocator.md)                   | Ruft einen Zeiger auf die Zuweisung der PIN ab.          |
| IPin-Methoden                                                                    | BESCHREIBUNG                                          |
| [**Enummediatypes**](ctransinplaceoutputpin-enummediatypes.md)                 | Listet die bevorzugten Medientypen der PIN auf.          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




