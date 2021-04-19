---
description: Konstruktormethode.
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Cimagepalette. cimagepalette-Konstruktor (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CImagePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38b5766617e1d17fa3917048c2fb845b5194cc42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366875"
---
# <a name="cimagepalettecimagepalette-constructor"></a>Cimagepalette. cimagepalette-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbasefilter* 
</dt> <dd>

Zeiger auf den besitzenden Filter.

</dd> <dt>

*pbasewindow* 
</dt> <dd>

Zeiger auf ein **cbasewindow** -Objekt, das das Fenster verwaltet, in dem die Palette realisiert wird. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pdrawimage* 
</dt> <dd>

Zeiger auf ein **cdrawimage** -Objekt, das das Videobild zeichnet. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagepalette-Klasse**](cimagepalette.md)
</dt> </dl>

 

 




