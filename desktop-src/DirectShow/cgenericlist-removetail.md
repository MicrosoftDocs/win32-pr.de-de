---
description: Die removetail-Methode entfernt das letzte Element in der Liste.
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: Cgenericlist. removetail-Methode (wxlist. h)
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
ms.openlocfilehash: a7b98187c663f643acdce28b4f12ebc37b1d4c25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371406"
---
# <a name="cgenericlistremovetail-method"></a>Cgenericlist. removetail-Methode

Die- `RemoveTail` Methode entfernt das letzte Element in der Liste.

## <a name="syntax"></a>Syntax


```C++
OBJECT* RemoveTail();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp) oder **null** zurück, wenn die Liste leer ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode löscht den Listen Knoten, jedoch nicht das Element, das im Knoten enthalten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cgenericlist-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




