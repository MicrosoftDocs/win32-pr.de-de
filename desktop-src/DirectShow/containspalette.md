---
description: Die ContainsPalette-Funktion bestimmt, ob eine angegebene VIDEOINFOHEADER-Struktur eine Palette enthält.
ms.assetid: e87ab1af-a822-45d8-9326-08b450e11279
title: ContainsPalette-Funktion (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContainsPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c9e5ab793dfaadb868cc09cfbe25e59c02dc338b470992b81ab1990581e5c19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954169"
---
# <a name="containspalette-function"></a>ContainsPalette-Funktion

Die **ContainsPalette-Funktion** bestimmt, ob eine angegebene [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) eine Palette enthält.

## <a name="syntax"></a>Syntax


```C++
BOOL ContainsPalette(
   const VIDEOINFOHEADER *pVideoInfo

);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Zeiger auf eine [**VIDEOINFOHEADER-Struktur.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn der Bitdepth 8 oder weniger **(bmiHeader.biBitCount)** oder die Anzahl der Farbindizes größer als 0 **(bmiHeader.biClrUsed)** ist. Gibt andernfalls **FALSE zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Video- und Bildfunktionen](video-and-image-functions.md)
</dt> </dl>

 

 




