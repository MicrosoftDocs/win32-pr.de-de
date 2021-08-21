---
description: Die GetNext-Methode ruft das Element an der angegebenen Position ab und verfeinert die Position.
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: CGenericList.GetNext-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.GetNext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f116dd1a965145e5bdf4808d25a7406b4709967c5cf971ad3529ae9d301ebc4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539740"
---
# <a name="cgenericlistgetnext-method"></a>CGenericList.GetNext-Methode

Die `GetNext` -Methode ruft das Element an der angegebenen Position ab und verfeinert die Position.

## <a name="syntax"></a>Syntax


```C++
OBJECT* GetNext(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rp* \[ Ref\]
</dt> <dd>

Verweis auf einen POSITION-Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf ein Objekt vom Typ **OBJECT** (vorlagentyp) zurück.

## <a name="remarks"></a>Hinweise

Diese Methode positioniert den Positionsindikator auf die nächste Position. Wenn sich der Positionsindikator über das Ende der Liste hinaus bewegt, legt die Methode ihn auf **NULL fest.**

Wenn *rp* NULL **ist,** gibt die Methode **NULL zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CGenericList-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




