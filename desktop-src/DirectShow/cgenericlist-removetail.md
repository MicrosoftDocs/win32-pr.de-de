---
description: Die RemoveTail-Methode entfernt das letzte Element in der Liste.
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: CGenericList.RemoveTail-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed0b39d72eac68310dacdf2bfdc1d3c28bb35695b3d77230ba37f6fe81c417ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656155"
---
# <a name="cgenericlistremovetail-method"></a>CGenericList.RemoveTail-Methode

Die `RemoveTail` -Methode entfernt das letzte Element in der Liste.

## <a name="syntax"></a>Syntax


```C++
OBJECT* RemoveTail();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf ein Objekt vom Typ **OBJECT** (vorlagentyp) oder **NULL** zurück, wenn die Liste leer ist.

## <a name="remarks"></a>Hinweise

Diese Methode löscht den Listenknoten, aber nicht das Element, das im Knoten enthalten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CGenericList-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




