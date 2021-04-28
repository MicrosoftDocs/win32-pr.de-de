---
description: 'CImagePalette.CImagePalette-Konstruktor: Konstruktormethode.'
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
ms.openlocfilehash: 5021b165a8fa47bedc7961657d7cdbfa07af301d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085678"
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



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CImagePalette-Klasse**](cimagepalette.md)
</dt> </dl>

 

 




