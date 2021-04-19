---
description: Die onrenderend-Methode führt Glättung für Fälle aus, bei denen die Renderingzeit aufgrund von Unterbrechungen variiert.
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: Cbasevideorenderer. onrenderend-Methode (renbase. h)
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
ms.openlocfilehash: 8f37b4d03f77090f4cac40a218fd3ac27c0c349d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365392"
---
# <a name="cbasevideorendereronrenderend-method"></a>Cbasevideorenderer. onrenderend-Methode

Die- `OnRenderEnd` Methode führt Glättung in Fällen aus, in denen die Renderingzeit aufgrund von Unterbrechungen variiert

## <a name="syntax"></a>Syntax


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediasample* 
</dt> <dd>

Zeiger auf das Medien Beispiel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion sollte direkt nach dem Zeichnen eines Bilds aufgerufen werden.

Diese Member-Funktion überschreibt [**cbaserenderer:: onrenderend**](cbaserenderer-onrenderend.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




