---
description: Die SetControlVideoPin-Methode legt den vom Filter verwendeten Pin fest.
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: CBaseControlVideo.SetControlVideoPin-Methode (Ctlutil.h)
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
ms.openlocfilehash: 6169b5d2ec71148cd868e340c5a2f4e206355044ce55e0905c20787ddb3a263e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660785"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a>CBaseControlVideo.SetControlVideoPin-Methode

Die `SetControlVideoPin` -Methode legt den vom Filter verwendeten Pin fest.

## <a name="syntax"></a>Syntax


```C++
void SetControlVideoPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPin* 
</dt> <dd>

Zeiger auf den Stecknadel, mit dem die Schnittstelle synchronisiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die Schnittstelle kann nur aufgerufen werden, wenn der Filter erfolgreich verbunden wurde. Das -Objekt wird durch diese Methode an den Pin übergeben, mit dem es synchronisiert wird. in den meisten Fällen wird ermittelt, ob der Pin verbunden ist, wenn er über eine Schnittstellenmethode namens verfügt, und gibt VFW \_ E \_ NOT CONNECTED \_ zurück, wenn er ausfällt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




