---
description: Die Remove-Methode entfernt das Element an der angegebenen Position.
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: CGenericList.Remove-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40b00d0772f391978fa6e581623446c67c2f37deabb1737e2602d7da7382fbaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317760"
---
# <a name="cgenericlistremove-method"></a>CGenericList.Remove-Methode

Die `Remove` -Methode entfernt das Element an der angegebenen Position.

## <a name="syntax"></a>Syntax


```C++
OBJECT* Remove(
   POSITION pos
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* 
</dt> <dd>

POSITION-Wert, der das zu entfernende Element angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf ein Objekt vom Typ **OBJECT** (vorlagentyp) zurück.

## <a name="remarks"></a>Hinweise

Diese Methode löscht den Knoten aus der Liste, aber nicht das in diesem Knoten enthaltene Element.

Wenn *pos* **NULL** ist, gibt die Methode **NULL** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CGenericList-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




