---
description: Die OnStopStreaming-Methode wird am Ende des Streamings aufgerufen, um die Zeiten für den Eigenschaftenseitenbericht zu korrigieren.
ms.assetid: 92174edb-2f6c-4bad-91c5-769aaebcc495
title: CBaseVideoRenderer.OnStopStreaming-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38e1e3fef83bab4d598cfd36294c5c405c1eca938372b43f12a6401c4be3c46b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586040"
---
# <a name="cbasevideorendereronstopstreaming-method"></a>CBaseVideoRenderer.OnStopStreaming-Methode

Die `OnStopStreaming` -Methode wird am Ende des Streamings aufgerufen, um die Zeiten für den Eigenschaftenseitenbericht zu korrigieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion wird zweimal aufgerufen, einmal beim Anhalten und erneut, wenn der Stream tatsächlich beendet wird.

Diese Memberfunktion überschreibt [**CBaseRenderer::OnStopStreaming**](cbaserenderer-onstopstreaming.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




