---
description: Die setmediatype-Methode legt den Medientyp für die Verbindung fest.
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Cbasepin. setmediatype-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 07ac736558cea12a16c695cf109c3d6283ce4a13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371223"
---
# <a name="cbasepinsetmediatype-method"></a>Cbasepin. setmediatype-Methode

Die- `SetMediaType` Methode legt den Medientyp für die Verbindung fest.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode wird das Format für eine PIN-Verbindung festgelegt. Vor dem Aufrufen dieser Methode ruft die PIN die [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode auf, um zu bestimmen, ob der Medientyp zulässig ist. Daher wird davon ausgegangen, dass der *PMT* -Parameter ein akzeptabler Medientyp ist.

In der Basisklasse legt diese Methode die Member-Variable [**cbasepin:: m \_ MT**](cbasepin-m-mt.md) fest und gibt S \_ OK zurück. Eine abgeleitete Klasse kann diese Methode überschreiben, wenn Sie eine Benachrichtigung erfordert, wenn der Medientyp festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




