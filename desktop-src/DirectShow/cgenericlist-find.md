---
description: Die Find-Methode ruft die erste Position ab, die das angegebene Element enthält.
ms.assetid: 8e2a3e5d-96e6-4f40-8e2a-4dc8c21088cd
title: Cgenericlist. Find-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Find
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a21f16e25d8a2ebba4494a850bc456a7b579f2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355953"
---
# <a name="cgenericlistfind-method"></a>Cgenericlist. Find-Methode

Die- `Find` Methode ruft die erste Position ab, die das angegebene Element enthält.

## <a name="syntax"></a>Syntax


```C++
POSITION Find(
   OBJECT *pObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pobj* 
</dt> <dd>

Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Positionswert oder **null** zurück, wenn das Element nicht in der Liste enthalten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cgenericlist-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




