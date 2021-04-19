---
description: Die setcontrolvideopin-Methode legt die vom Filter verwendete PIN fest.
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: Cbasecontrolvideo. setcontrolvideopin-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetControlVideoPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4cf47469800a4d1ecd8abe373d6f3c1fd53ece5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369422"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a>Cbasecontrolvideo. setcontrolvideopin-Methode

Die- `SetControlVideoPin` Methode legt die vom Filter verwendete PIN fest.

## <a name="syntax"></a>Syntax


```C++
void SetControlVideoPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppin* 
</dt> <dd>

Zeiger auf die PIN, mit der die Schnittstelle synchronisiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die-Schnittstelle kann nur aufgerufen werden, wenn der Filter erfolgreich verbunden wurde. Das-Objekt wird durch diese Methode an die PIN übergeben, mit der es synchronisiert wird. in den meisten Fällen wird festgestellt, ob die PIN verbunden ist, wenn Sie über eine Schnittstellen Methode mit dem Namen verfügt, und \_ \_ \_ Wenn Sie fehlschlägt, wird VFW E nicht verbunden zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




