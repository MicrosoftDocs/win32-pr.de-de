---
description: Die getbitmapformatsize-Funktion berechnet die erforderliche Größe für eine videoinfo-Struktur, die eine angegebene BITMAPINFOHEADER-Struktur enthalten kann.
ms.assetid: a559415a-070f-4674-be12-a65a46025809
title: Getbitmapformatsize-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapFormatSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39a64f6d975e403de6c177906b23ef7e09f29ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373776"
---
# <a name="getbitmapformatsize-function"></a>Getbitmapformatsize-Funktion

Die- `GetBitmapFormatSize` Funktion berechnet die erforderliche Größe für eine [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur, die eine angegebene [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur enthalten kann.

## <a name="syntax"></a>Syntax


```C++
LONG GetBitmapFormatSize(
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

## <a name="remarks"></a>Bemerkungen

Auf eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur folgen möglicherweise Farb Masken oder Paletteneinträge, sodass es schwierig sein kann, die Anzahl von Bytes zu bestimmen, die erforderlich sind, um eine [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur aus einer vorhandenen **BITMAPINFOHEADER** -Struktur zu erstellen.

Um eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur in eine [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur zu kopieren, verwenden Sie das [**Header**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) Makro, das den korrekten Offset berechnet.

## <a name="examples"></a>Beispiele


```
LONG size = GetBitmapFormatSize(&bmi);

VIDEOINFO *pVi = static_cast<VIDEOINFO*>(CoTaskMemAlloc(size));

if (pVi != NULL)
{
    CopyMemory(HEADER(pVi), &bmi, sizeof(BITMAPINFOHEADER));
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video-und Bildfunktionen](video-and-image-functions.md)
</dt> </dl>

 

 




