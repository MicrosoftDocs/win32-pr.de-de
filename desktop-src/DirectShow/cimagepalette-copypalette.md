---
description: Die CopyPalette-Methode kopiert die Palette aus einer beliebigen VIDEOINFO-Struktur in eine beliebige palettierte VIDEOINFO-Struktur.
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: CImagePalette.CopyPalette-Methode (Winutil.h)
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
ms.openlocfilehash: 5c6f645d134ccf5fa786ff59cf0bc6cd37211af0cb2571bbc9955e5bb6367a97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055450"
---
# <a name="cimagepalettecopypalette-method"></a>CImagePalette.CopyPalette-Methode

Die `CopyPalette` -Methode kopiert die Palette aus einer beliebigen [**VIDEOINFO-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) in eine beliebige palettierte **VIDEOINFO-Struktur.**

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

Zeiger auf den Quellmedientyp.

</dd> <dt>

*pDest* 
</dt> <dd>

Zeiger auf den Zielmedientyp.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn die Palette kopiert wurde. Gibt S \_ FALSE zurück, wenn der Quell- oder Zielmedientyp nicht über eine Palette verfügt.

## <a name="remarks"></a>Hinweise

Der *pDest-Medientyp* muss ein palettiertes Format mit einer Farbtiefe von mindestens 8 Bits sein. Der *Medientyp pSrc* kann ein [**beliebiger VIDEOINFOHEADER-Typ**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) mit einer Palette sein, einschließlich YUV- und True-Color-Formaten mit Paletteneinträgen. Die -Methode kopiert die Paletteneinträge aus *pSrc* in eine neue Palette und fügt die neue Palette an *pDest* an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImagePalette-Klasse**](cimagepalette.md)
</dt> </dl>

 

 




