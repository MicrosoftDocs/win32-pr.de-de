---
description: Die OnRenderEnd-Methode führt die Glättung für Fälle aus, in denen die Renderingzeit aufgrund von Unterbrechungen variiert.
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: CBaseVideoRenderer.OnRenderEnd-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24d622ec62b27ae2e85eb9bef37516c82acbb17e03bef9a51b161edacd0b95c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658687"
---
# <a name="cbasevideorendereronrenderend-method"></a>CBaseVideoRenderer.OnRenderEnd-Methode

Die `OnRenderEnd` -Methode führt die Glättung für Fälle aus, in denen die Renderingzeit aufgrund von Unterbrechungen variiert.

## <a name="syntax"></a>Syntax


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Zeiger auf das Medienbeispiel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion sollte direkt nach dem Zeichnen eines Bilds aufgerufen werden.

Diese Memberfunktion überschreibt [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




