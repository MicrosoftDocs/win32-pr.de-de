---
description: Die Remove-Methode entfernt das Element an der angegebenen Position.
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: Cgenericlist. Remove-Methode (wxlist. h)
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
ms.openlocfilehash: d5fc3d0cd76cd78c83fa210d8b91ba97b93b92f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358624"
---
# <a name="cgenericlistremove-method"></a>Cgenericlist. Remove-Methode

Die- `Remove` Methode entfernt das Element an der angegebenen Position.

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

Positionswert, der das zu entfern gende Element angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp) zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode löscht den Knoten aus der Liste, löscht jedoch nicht das Element, das in diesem Knoten enthalten ist.

Wenn *POS* **null** ist, gibt die Methode **null** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cgenericlist-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




