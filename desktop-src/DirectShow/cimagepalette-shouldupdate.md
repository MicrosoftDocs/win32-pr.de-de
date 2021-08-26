---
description: Die ShouldUpdate-Methode bestimmt, ob eine neue Palette erstellt werden muss.
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: CImagePalette.ShouldUpdate-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.ShouldUpdate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c7897e14aec690ec67451fe868b5352e99c9bd513c8c182a47556fe075cffb2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916030"
---
# <a name="cimagepaletteshouldupdate-method"></a>CImagePalette.ShouldUpdate-Methode

Die `ShouldUpdate` -Methode bestimmt, ob eine neue Palette erstellt werden muss.

## <a name="syntax"></a>Syntax


```C++
BOOL ShouldUpdate(
   const VIDEOINFOHEADER *pNewInfo,
   const VIDEOINFOHEADER *pOldInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNewInfo* 
</dt> <dd>

Zeiger auf eine [**VIDEOINFOHEADER-Struktur,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) die die neue Farbtabelle enthält.

</dd> <dt>

*pOldInfo* 
</dt> <dd>

Zeiger auf eine **VIDEOINFOHEADER-Struktur,** die die alte Farbtabelle enthält. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die Palette aktualisiert werden muss, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

-   Wenn keine **der VIDEOINFOHEADER-Strukturen** eine Farbtabelle enthält, gibt die Methode **FALSE zurück.**
-   Wenn nur eine Struktur eine Farbtabelle enthält oder *wenn pOldInfo* **NULL** ist, gibt die Methode **TRUE zurück.**
-   Wenn beide Strukturen Farbtabellen enthalten und die Farbeinträge übereinstimmen, gibt die Methode **FALSE zurück.**
-   Wenn beide Strukturen Farbtabellen enthalten, die Farbeinträge jedoch nicht übereinstimmen, gibt die Methode **TRUE zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImagePalette-Klasse**](cimagepalette.md)
</dt> </dl>

 

 




