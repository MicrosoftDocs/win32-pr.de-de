---
description: Die throttlewait-Methode fügt eine Wartezeit nach jedem Frame ein.
ms.assetid: 69306093-f5db-4170-b30f-e33cfa448e9f
title: Cbasevideorenderer. throttlewait-Methode (renbase. h)
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
ms.openlocfilehash: 7408cfb011fa0fbbb223b6757ddb10ff9cbd357b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367577"
---
# <a name="cbasevideorendererthrottlewait-method"></a>Cbasevideorenderer. throttlewait-Methode

Die- `ThrottleWait` Methode fügt eine Wartezeit nach jedem Frame ein.

## <a name="syntax"></a>Syntax


```C++
void ThrottleWait();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion wartet auf einen Zeitraum, der vom **m \_ trthrottle** -Datenmember abgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




