---
description: Die GetRealState-Methode ruft den Filterzustand ab.
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: CBaseRenderer.GetRealState-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c65ac4310abddc619296776981040cc5e1e6c5ad48ce37ea24210bc5a85d94b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403419"
---
# <a name="cbaserenderergetrealstate-method"></a>CBaseRenderer.GetRealState-Methode

Die `GetRealState` -Methode ruft den Filterzustand ab.

## <a name="syntax"></a>Syntax


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert von [**CBaseFilter::m \_ State**](cbasefilter-m-state.md)zurück. Der Wert ist ein Member des aufzählten [**FILTER \_ STATE-Typs.**](/windows/win32/api/strmif/ne-strmif-filter_state)

## <a name="remarks"></a>Hinweise

Diese Methode stellt eine einfachere Alternative zur [**CBaseRenderer::GetState-Methode**](cbaserenderer-getstate.md) zur internen Verwendung bereit.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




