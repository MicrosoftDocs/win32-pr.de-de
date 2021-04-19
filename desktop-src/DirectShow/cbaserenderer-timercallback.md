---
description: Die TimerCallback-Methode ist eine Rückruf Methode für das End-of-Stream-Timer-Ereignis.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: Cbaserderderer. TimerCallback-Methode (renbase. h)
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
ms.openlocfilehash: cfa59ca6bed0539caa7eb650458c168999b0de5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359805"
---
# <a name="cbaserenderertimercallback-method"></a>Cbaserderderer. TimerCallback-Methode

Die- `TimerCallback` Methode ist eine Rückruf Methode für das End-of-Stream-Timer-Ereignis.

## <a name="syntax"></a>Syntax


```C++
void TimerCallback();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**cbaserderderer:: sendendofstream**](cbaserenderer-sendendofstream.md) -Methode verwendet ein Timer-Ereignis, um EC-Complete-Benachrichtigungen zu planen \_ . Die **cbaserenderer:: TimerCallback** -Methode ist die Rückruffunktion für das Timer-Ereignis. `TimerCallback`Von der-Methode wird " **sendendofstream** " erneut aufgerufen, und " **sendendofstream** " bestimmt, ob die ausführliche EC- \_ Benachrichtigung gesendet oder ein anderer Timer festgelegt

Die [**cbaserrederer:: rectendof Stream Timer**](cbaserenderer-resetendofstreamtimer.md) -Methode bricht das Timer-Ereignis ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




