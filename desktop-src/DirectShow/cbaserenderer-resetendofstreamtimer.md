---
description: Die ResetEndOfStreamTimer-Methode bricht den Timer ab, der EC \_ COMPLETE-Benachrichtigungen geplant.
ms.assetid: 9d423241-1401-4181-8fbf-c409a1e8abdd
title: CBaseRenderer.ResetEndOfStreamTimer-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStreamTimer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e589288059eabbbbaaa23904ba021199cb051d9034345cb2c92ac946a6cba9c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502680"
---
# <a name="cbaserendererresetendofstreamtimer-method"></a>CBaseRenderer.ResetEndOfStreamTimer-Methode

Die `ResetEndOfStreamTimer` -Methode bricht den Timer ab, der [**EC \_ COMPLETE-Benachrichtigungen**](ec-complete.md) geplant.

## <a name="syntax"></a>Syntax


```C++
void ResetEndOfStreamTimer();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md)
</dt> <dt>

[**CBaseRenderer::TimerCallback**](cbaserenderer-timercallback.md)
</dt> </dl>

 

 




