---
description: Die OnStartStreaming-Methode setzt alle Zeiten zurück, die das Streaming steuern.
ms.assetid: a2bb07f2-6880-4030-96c5-d146982dfe66
title: CBaseVideoRenderer.OnStartStreaming-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2a55d509c900c7be68d3225826c208755d31ef66e0c24119bd1d044dad1aefc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157055"
---
# <a name="cbasevideorendereronstartstreaming-method"></a>CBaseVideoRenderer.OnStartStreaming-Methode

Die `OnStartStreaming` -Methode setzt alle Zeiten zurück, die das Streaming steuern.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnStartStreaming();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion überschreibt [**CBaseRenderer::OnStartStreaming**](cbaserenderer-onstartstreaming.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




