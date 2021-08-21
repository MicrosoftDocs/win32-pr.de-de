---
description: Die ScheduleSample-Methode überschreibt die Basisklasse, die die Hauptarbeit übernimmt, um die Anzahl der gezeichneten und gelöschten Stichproben (die von der IQualProp-Implementierung verwendet werden) zu behalten.
ms.assetid: 66e4e318-a7ff-4ba0-9ac5-24ba39ac86f1
title: CBaseVideoRenderer.ScheduleSample-Methode (Renbase.h)
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
ms.openlocfilehash: f68701fd4c4d682d6bcd89c3b82d6bf054188a9bbdcb47c9019b563fad4a877f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658234"
---
# <a name="cbasevideorendererschedulesample-method"></a>CBaseVideoRenderer.ScheduleSample-Methode

Die -Methode überschreibt die Basisklasse, die die Hauptarbeit übernimmt, um die Anzahl der gezeichneten und gelöschten Stichproben (die von der `ScheduleSample` [**IQualProp-Implementierung verwendet**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) werden) zu behalten.

## <a name="syntax"></a>Syntax


```C++
BOOL ScheduleSample(
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

Gibt **TRUE zurück,** wenn das Beispiel geplant ist. andernfalls gibt **FALSE zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




