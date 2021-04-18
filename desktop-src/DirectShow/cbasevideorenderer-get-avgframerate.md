---
description: Die get \_ avgframerate-Methode berechnet die durchschnittliche Frame Rate und ruft Sie ab.
ms.assetid: f36fc020-8c1a-491f-9f55-18265fde8bf8
title: CBaseVideoRenderer.get_AvgFrameRate-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgFrameRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d8fff53f3d56676805eca9029670d51210ef2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365592"
---
# <a name="cbasevideorendererget_avgframerate-method"></a>Cbasevideorenderer. get \_ avgframerate-Methode

Die `get_AvgFrameRate` -Methode berechnet die durchschnittliche Framerate und ruft Sie ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_AvgFrameRate(
   int *piAvgFrameRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*piavgframerate* 
</dt> <dd>

Zeiger auf die Anzahl von Frames pro Sekunde, seit das Streaming begonnen hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die [**iqualprop:: get \_ avgframerate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




