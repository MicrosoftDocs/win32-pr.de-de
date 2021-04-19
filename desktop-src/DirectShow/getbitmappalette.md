---
description: Die GetBitmapPalette-Funktion gibt den ersten Paletteneintrag in einer videoinfoheader-Struktur zurück.
ms.assetid: 7c620f81-31d9-408f-954d-aeff39f93956
title: GetBitmapPalette-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa4139c7aaece3e92a26fbf69fc02b8759f1613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354179"
---
# <a name="getbitmappalette-function"></a>GetBitmapPalette-Funktion

Die- `GetBitmapPalette` Funktion gibt den ersten Paletteneintrag in einer [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur zurück.

## <a name="syntax"></a>Syntax


```C++
const RGBQUAD* GetBitmapPalette(
   const VIDEOINFOHEADER *pVideoInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvideoinfo* 
</dt> <dd>

Zeiger auf eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf den ersten Paletteneintrag zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




