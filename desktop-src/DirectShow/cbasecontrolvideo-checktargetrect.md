---
description: Die CheckTargetRect-Methode bestimmt, ob ein Zielrechteck gültig ist.
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: CBaseControlVideo.CheckTargetRect-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8444764af729f9536471a6a9df221cc118edb7d043112eb0b5351f45982d87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057320"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a>CBaseControlVideo.CheckTargetRect-Methode

Die `CheckTargetRect` -Methode bestimmt, ob ein Zielrechteck gültig ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Zeiger auf das zu überprüfende Zielrechteck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ INVALIDARG zurück, wenn ungültig; andernfalls gibt NOERROR (S \_ OK) zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion bestimmt, ob das angeforderte Zielrechteck gültig ist. Da das Zielrechteck eine Position im logischen Client des Fensters angibt, können die Koordinaten negativ sein, obwohl die Gesamtbreite und Höhe nicht 0 (null) oder ein negativer Wert sein darf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




