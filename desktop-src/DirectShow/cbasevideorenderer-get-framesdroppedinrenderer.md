---
description: Die get \_ framesdroppedinrenderer-Methode ruft die Anzahl der Frames ab, die vom Renderer gelöscht wurden.
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: CBaseVideoRenderer.get_FramesDroppedInRenderer-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDroppedInRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef81678fce8d349c7c047b0453cc480d8673f8f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370620"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a>Cbasevideorenderer. get \_ framesdroppedinrenderer-Methode

Die- `get_FramesDroppedInRenderer` Methode ruft die Anzahl der Frames ab, die vom Renderer gelöscht wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_FramesDroppedInRenderer(
   int *pcFramesDropped
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcframesdrop* 
</dt> <dd>

Zeiger auf die Anzahl der gelöschten Frames.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die [**iqualprop:: get \_ framesdroppedinrenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) -Methode. Auf diese Weise Ruft die Eigenschaften Seite die Daten aus dem Scheduler ab. Frames können auch Upstream abgelegt werden, ohne dass der Renderer Sie sehen kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




