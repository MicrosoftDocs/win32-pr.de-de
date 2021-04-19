---
description: Die resetstreamingtimes-Methode setzt alle Zeiten zurück, die das Streaming steuern.
ms.assetid: 8a596760-a45a-4486-bb91-aab10bbf927f
title: Cbasevideorenderer. resetstreamingtimes-Methode (renbase. h)
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
ms.openlocfilehash: d887ca9e246d5e3fb746c119b1ed6784201ec702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373640"
---
# <a name="cbasevideorendererresetstreamingtimes-method"></a>Cbasevideorenderer. resetstreamingtimes-Methode

Die- `ResetStreamingTimes` Methode setzt alle Zeiten zurück, die das Streaming steuern.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT ResetStreamingTimes();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Uhrzeiten werden so festgelegt, dass Frames nicht anfänglich abgelegt werden und dass der erste Frame gezeichnet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




