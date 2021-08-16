---
description: Flag, das angibt, ob ein Laufzeitfehler aufgetreten ist.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: CBasePin::m_bRunTimeError-Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffc07a15f7c34744be52c5e2c7b5233e1885b58c5b9b7d078871277f8fc0efd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823332"
---
# <a name="cbasepinm_bruntimeerror-member"></a>CBasePin::m \_ bRunTimeError-Member

Flag, das angibt, ob ein Laufzeitfehler aufgetreten ist.

## <a name="syntax"></a>Syntax


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a>Hinweise

Dieses Flag ist standardmäßig auf **FALSE festgelegt.** Legen Sie das Flag auf **TRUE** fest, wenn während des Streamings ein Laufzeitfehler auftritt. Die [**CBasePin::Inactive-Methode**](cbasepin-inactive.md) setzt das Flag auf **FALSE zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




