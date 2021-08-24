---
description: Die OnWaitEnd-Methode wird aufgerufen, wenn der Filter auf die Präsentationszeit eines Beispiels gewartet wird.
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: CBaseRenderer.OnWaitEnd-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 451f475f8830e1b6e2c51f3e0fc571f86f520030fe8ec3dad6acf3d9d5e5c6fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537440"
---
# <a name="cbaserendereronwaitend-method"></a>CBaseRenderer.OnWaitEnd-Methode

Die `OnWaitEnd` -Methode wird aufgerufen, wenn der Filter auf die Präsentationszeit eines Beispiels wartet.

## <a name="syntax"></a>Syntax


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die [**CBaseRenderer::WaitForRenderTime-Methode**](cbaserenderer-waitforrendertime.md) ruft diese Methode auf, wenn sie auf die Präsentationszeit eines Beispiels gewartet hat. Diese Methode führt keineRlei In der Basisklasse aus, aber die abgeleitete Klasse kann sie überschreiben.

Wenn Sie die Qualitätskontrolle implementieren, können Sie diese Methode zusammen mit der [**CBaseRenderer::OnWaitStart-Methode**](cbaserenderer-onwaitstart.md) überschreiben. Sie können diese Methoden verwenden, um die Leistung des Filters nachzuverfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




