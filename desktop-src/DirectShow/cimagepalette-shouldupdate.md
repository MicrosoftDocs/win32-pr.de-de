---
description: Die Methode "schuldupdate" bestimmt, ob eine neue Palette erstellt werden muss.
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: Cimagepalette. Schulter Dupdate-Methode (winutil. h)
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
ms.openlocfilehash: f8cf27548487ad0338f0c4773c66df8f7d03c2f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373621"
---
# <a name="cimagepaletteshouldupdate-method"></a>Cimagepalette. schuldupdate-Methode

Die- `ShouldUpdate` Methode bestimmt, ob eine neue Palette erstellt werden muss.

## <a name="syntax"></a>Syntax


```C++
BOOL ShouldUpdate(
   const VIDEOINFOHEADER *pNewInfo,
   const VIDEOINFOHEADER *pOldInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnetwinfo* 
</dt> <dd>

Ein Zeiger auf eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur, die die neue Farbtabelle enthält.

</dd> <dt>

*poldinfo* 
</dt> <dd>

Zeiger auf eine **videoinfoheader** -Struktur, die die alte Farbtabelle enthält. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Palette aktualisiert werden muss, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

-   Wenn keine **videoinfoheader** -Struktur eine Farbtabelle enthält, gibt die Methode **false** zurück.
-   Wenn nur eine Struktur eine Farbtabelle enthält oder *poldinfo* **null** ist, gibt die Methode **true** zurück.
-   Wenn beide Strukturen Farbtabellen enthalten und die Farbeinträge Stimmen, gibt die Methode **false** zurück.
-   Wenn beide Strukturen Farbtabellen enthalten, die Farbeinträge jedoch nicht stimmen, gibt die Methode **true** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagepalette-Klasse**](cimagepalette.md)
</dt> </dl>

 

 




