---
description: Bestimmt, ob ein Quellrechteck gültig ist.
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: CBaseControlVideo.CheckSourceRect-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf7ac41d626eceee048afc4671a5e171e7164adfbd9a941b1b70bc85ea988c3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873010"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a>CBaseControlVideo.CheckSourceRect-Methode

Bestimmt, ob ein Quellrechteck gültig ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Zeiger auf das zu überprüfende Quellrechteck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ INVALIDARG zurück, wenn ungültig; andernfalls gibt NOERROR (S \_ OK) zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion überprüft, ob das angeforderte Quellrechteck das verfügbare Quellvideo nicht überschreitet. Die linke und die obere Koordinate dürfen nicht negativ sein, und breite und höhe dürfen den rechten und unteren Rand des Videos nicht überschreiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




