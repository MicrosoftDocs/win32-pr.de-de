---
description: Die \_ get AvgFrameRate-Methode berechnet und ruft die durchschnittliche erzielten Bildfrequenz ab.
ms.assetid: f36fc020-8c1a-491f-9f55-18265fde8bf8
title: CBaseVideoRenderer.get_AvgFrameRate-Methode (Renbase.h)
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
ms.openlocfilehash: 79aab0677cfd5cba5f6a889519e0c12ed2236d8f82eca28b3fa7b227b941b2b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658783"
---
# <a name="cbasevideorendererget_avgframerate-method"></a>CBaseVideoRenderer.get \_ AvgFrameRate-Methode

Die `get_AvgFrameRate` -Methode berechnet und ruft die durchschnittliche erzielten Bildfrequenz ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_AvgFrameRate(
   int *piAvgFrameRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*piAvgFrameRate* 
</dt> <dd>

Zeiger auf die Anzahl der Frames pro Sekunde seit Beginn des Streamings.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die [**IQualProp::get \_ AvgFrameRate-Methode.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




