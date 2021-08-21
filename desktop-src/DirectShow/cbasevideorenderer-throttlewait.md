---
description: Die ThrottleWait-Methode fügt nach jedem Frame eine Wartezeit ein.
ms.assetid: 69306093-f5db-4170-b30f-e33cfa448e9f
title: CBaseVideoRenderer.ThrottleWait-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ThrottleWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d61c0e934208ad72e678595ce668c6c7ff72eda3371c792b294df9f2d5915612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954749"
---
# <a name="cbasevideorendererthrottlewait-method"></a>CBaseVideoRenderer.ThrottleWait-Methode

Die `ThrottleWait` -Methode fügt nach jedem Frame eine Wartezeit ein.

## <a name="syntax"></a>Syntax


```C++
void ThrottleWait();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion wartet für einen Zeitraum, der vom **m \_ trThrottle-Datenmember** abgerufen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




