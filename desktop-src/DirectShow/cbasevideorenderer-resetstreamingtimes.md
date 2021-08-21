---
description: Die ResetStreamingTimes-Methode setzt alle Zeiten zurück, die das Streaming steuern.
ms.assetid: 8a596760-a45a-4486-bb91-aab10bbf927f
title: CBaseVideoRenderer.ResetStreamingTimes-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ResetStreamingTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bebf6f827cac883660b383b76f3a6ead7987e9fb468d0fd6f14205f59ad4d530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074774"
---
# <a name="cbasevideorendererresetstreamingtimes-method"></a>CBaseVideoRenderer.ResetStreamingTimes-Methode

Die `ResetStreamingTimes` -Methode setzt alle Zeiten zurück, die das Streaming steuern.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT ResetStreamingTimes();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Die Zeiten werden so festgelegt, dass Frames anfänglich nicht gelöscht werden und der erste Frame gezeichnet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




