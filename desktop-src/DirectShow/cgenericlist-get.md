---
description: Die Get-Methode ruft das Element an der angegebenen Position ab.
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: CGenericList.Get-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Get
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dae90872ea607571b215aafe3f9f35a645cd50d140dcbad0783369ce2189c881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813770"
---
# <a name="cgenericlistget-method"></a>CGenericList.Get-Methode

Die `Get` -Methode ruft das Element an der angegebenen Position ab.

## <a name="syntax"></a>Syntax


```C++
OBJECT* Get(
   POSITION pos
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* 
</dt> <dd>

Positionsindikator für das abzurufende Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf ein Objekt vom Typ **OBJECT** (vorlagentyp) zurück.

## <a name="remarks"></a>Hinweise

Wenn *pos* NULL **ist,** gibt die Methode **NULL zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CGenericList-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




