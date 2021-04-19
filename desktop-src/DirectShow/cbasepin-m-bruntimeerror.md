---
description: Flag, das angibt, ob ein Laufzeitfehler aufgetreten ist.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: 'Cbasepin:: m_bRunTimeError Member (amfilter. h)'
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
ms.openlocfilehash: 5e8b0c5548d3089a6e619f88db5e4eed19b12be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370825"
---
# <a name="cbasepinm_bruntimeerror-member"></a>Cbasepin:: m- \_ Member von bruntimeerror

Flag, das angibt, ob ein Laufzeitfehler aufgetreten ist.

## <a name="syntax"></a>Syntax


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a>Bemerkungen

Dieses Flag ist standardmäßig auf **false** eingestellt. Legen Sie das-Flag auf **true** fest, wenn beim Streaming ein Laufzeitfehler auftritt. Die [**cbasepin:: inaktive**](cbasepin-inactive.md) -Methode setzt das Flag auf **false** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




