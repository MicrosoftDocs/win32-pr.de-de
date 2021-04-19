---
description: Die schedulesample-Methode überschreibt die Basisklasse, die die Hauptarbeit durchführt, um die Anzahl der gezeichneten und gelöschten Stichproben zu erhalten (die von der iqualprop-Implementierung verwendet werden).
ms.assetid: 66e4e318-a7ff-4ba0-9ac5-24ba39ac86f1
title: Cbasevideorenderer. schedulesample-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62827f1cda9423f9a5128c35289803027bfa78a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369419"
---
# <a name="cbasevideorendererschedulesample-method"></a>Cbasevideorenderer. schedulesample-Methode

Die- `ScheduleSample` Methode überschreibt die Basisklasse, die die Hauptarbeit durchführt, um die Anzahl der gezeichneten und gelöschten Stichproben zu erhalten (die von der [**iqualprop**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) -Implementierung verwendet werden).

## <a name="syntax"></a>Syntax


```C++
BOOL ScheduleSample(
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

Gibt " **true** " zurück, wenn das Beispiel geplant ist. Andernfalls wird **false** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




