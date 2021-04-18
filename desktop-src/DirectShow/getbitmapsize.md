---
description: Die getbitmapsize-Funktion berechnet die Anzahl der Bytes, die für eine geräteunabhängige Bitmap (DIB) erforderlich sind. Diese Funktion ruft einfach das dibsize-Makro auf.
ms.assetid: ce23cdf2-9804-4d2e-b9ef-16e54b2d571e
title: Getbitmapsize-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 004201cf3ff839aa1301dcfff0240a73a9128e50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351334"
---
# <a name="getbitmapsize-function"></a>Getbitmapsize-Funktion

Die- `GetBitmapSize` Funktion berechnet die Anzahl der Bytes, die für eine geräteunabhängige Bitmap (DIB) erforderlich sind. Diese Funktion ruft einfach das [**dibsize**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) -Makro auf.

## <a name="syntax"></a>Syntax


```C++
DWORD GetBitmapSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pheader* 
</dt> <dd>

Zeiger auf eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Größe in Bytes zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video-und Bildfunktionen](video-and-image-functions.md)
</dt> </dl>

 

 




