---
description: Mit der CopyPalette-Methode wird die Palette aus einer beliebigen videoinfo-Struktur in eine beliebige, von einer beliebigen Struktur über videoinfo-Struktur
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: Cimagepalette. CopyPalette-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CopyPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b429c5fd4d3d0e0e28cd0662fbee0a1ac926ddc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371512"
---
# <a name="cimagepalettecopypalette-method"></a>Cimagepalette. CopyPalette-Methode

Die- `CopyPalette` Methode kopiert die Palette aus einer beliebigen [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur in eine beliebige paletsierte **videoinfo** -Struktur.

## <a name="syntax"></a>Syntax


```C++
HRESULT CopyPalette(
   const CMediaType *pSrc,
   const CMediaType *pDest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrc* 
</dt> <dd>

Zeiger auf den Quell Medientyp.

</dd> <dt>

*pDest* 
</dt> <dd>

Zeiger auf den Zielmedientyp.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "S OK" zurück, \_ Wenn die Palette kopiert wurde. Gibt "false" zurück, \_ Wenn entweder der Quell-oder Ziel Medientyp keine Palette hat.

## <a name="remarks"></a>Bemerkungen

Der *pdest* -Medientyp muss ein paletsiertes Format mit einer Farbtiefe von 8 Bits oder weniger sein. Der *psrc* -Medientyp kann ein beliebiger [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Typ mit einer Palette sein, einschließlich YUV-und True-Color-Formaten mit paletteneinträgen. Die-Methode kopiert die Paletteneinträge aus *psrc* in eine neue Palette und fügt die neue Palette an den *pdest* an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagepalette-Klasse**](cimagepalette.md)
</dt> </dl>

 

 




