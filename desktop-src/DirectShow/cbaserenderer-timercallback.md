---
description: Die TimerCallback-Methode ist eine Rückrufmethode für das End-of-Stream-Timerereignis.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: CBaseRenderer.TimerCallback-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.TimerCallback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d3164959ecaa701397b5550c43449884208df1110300b6a042879ac4f146584
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537430"
---
# <a name="cbaserenderertimercallback-method"></a>CBaseRenderer.TimerCallback-Methode

Die `TimerCallback` -Methode ist eine Rückrufmethode für das Timerereignis am Ende des Streams.

## <a name="syntax"></a>Syntax


```C++
void TimerCallback();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die [**CBaseRenderer::SendEndOfStream-Methode**](cbaserenderer-sendendofstream.md) verwendet ein Timerereignis, um EC \_ COMPLETE-Benachrichtigungen zu planen. Die **CBaseRenderer::TimerCallback-Methode** ist die Rückruffunktion für das Timerereignis. Die `TimerCallback` -Methode ruft **SendEndOfStream** erneut auf, und **SendEndOfStream** bestimmt, ob die EC COMPLETE-Benachrichtigung gesendet oder \_ ein anderer Timer festgelegt werden soll.

Die [**CBaseRenderer::ResetEndOfStreamTimer-Methode**](cbaserenderer-resetendofstreamtimer.md) bricht das Timerereignis ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




