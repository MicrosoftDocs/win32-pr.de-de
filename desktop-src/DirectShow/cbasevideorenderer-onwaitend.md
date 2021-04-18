---
description: Die onwaitend-Methode wird aufgerufen, wenn eine Wartezeit endet.
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: Cbasevideorenderer. onwaitend-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36377565556a759c9268ef1bf31ff7774933ccc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358258"
---
# <a name="cbasevideorendereronwaitend-method"></a>Cbasevideorenderer. onwaitend-Methode

Die onwaitend-Methode wird aufgerufen, wenn eine Wartezeit endet.

## <a name="syntax"></a>Syntax


```C++
void OnWaitEnd();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion führt nur die Leistungs Protokollierung durch. Sie wird aufgerufen, wenn der Thread nicht im Fenster wartet oder das nächste Beispiel als gerendert wird. Es könnte schließlich verwendet werden, um Informationen zu sammeln, die die Synchronisierung steuern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




