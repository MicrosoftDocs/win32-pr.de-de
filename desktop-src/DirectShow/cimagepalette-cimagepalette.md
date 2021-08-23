---
description: 'CImagePalette.CImagePalette-Konstruktor : Konstruktormethode.'
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: CImagePalette.CImagePalette-Konstruktor (Winutil.h)
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
ms.openlocfilehash: 437055ee9e1d33d4b551faf1ca999d432a99d17919dcd67f6a701bc4f9780543
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428920"
---
# <a name="cimagepalettecimagepalette-constructor"></a>CImagePalette.CImagePalette-Konstruktor

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

*pBaseFilter* 
</dt> <dd>

Zeiger auf den besitzenden Filter.

</dd> <dt>

*pBaseWindow* 
</dt> <dd>

Zeiger auf ein **CBaseWindow-Objekt,** das das Fenster verwaltet, in dem die Palette realisiert wird. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pDrawImage* 
</dt> <dd>

Zeiger auf ein **CDrawImage-Objekt,** das das Videobild zeichnet. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CImagePalette-Klasse**](cimagepalette.md)
</dt> </dl>

 

 




