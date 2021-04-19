---
description: Die Get-Methode ruft das Element an der angegebenen Position ab.
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: Cgenericlist. Get-Methode (wxlist. h)
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
ms.openlocfilehash: 02af7d57d2219e6eb0506a8ab11521b4cf3570eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370192"
---
# <a name="cgenericlistget-method"></a>Cgenericlist. Get-Methode

Die- `Get` Methode ruft das Element an der angegebenen Position ab.

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

Positionsindikator für das Element, das abgerufen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp) zurück.

## <a name="remarks"></a>Bemerkungen

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

 

 




