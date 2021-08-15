---
description: Die OnWaitStart-Methode wird aufgerufen, wenn der Filter beginnt, auf die Präsentationszeit eines Beispiels zu warten.
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: CBaseRenderer.OnWaitStart-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eaad14d0eec765a0ad12693c0a1eee67386bc9bb26344ee52c29224d129edf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822647"
---
# <a name="cbaserendereronwaitstart-method"></a>CBaseRenderer.OnWaitStart-Methode

Die `OnWaitStart` -Methode wird aufgerufen, wenn der Filter beginnt, auf die Präsentationszeit eines Beispiels zu warten.

## <a name="syntax"></a>Syntax


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die [**CBaseRenderer::WaitForRenderTime-Methode**](cbaserenderer-waitforrendertime.md) ruft diese Methode auf, wenn sie mit dem Warten auf die Präsentationszeit eines Beispiels beginnt. Diese Methode führt in der Basisklasse nichts aus, aber die abgeleitete Klasse kann sie überschreiben.

Wenn Sie die Qualitätskontrolle implementieren, können Sie diese Methode zusammen mit der [**CBaseRenderer::OnWaitEnd-Methode**](cbaserenderer-onwaitend.md) überschreiben. Mit diesen Methoden können Sie die Leistung des Filters nachverfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




