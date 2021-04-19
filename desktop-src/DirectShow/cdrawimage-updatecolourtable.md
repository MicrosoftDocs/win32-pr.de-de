---
description: Die updatecolourtable-Methode aktualisiert die Farbtabelle mit einer neuen Palette.
ms.assetid: 61ad98c6-a526-4aac-ad68-d44fadc668de
title: Cdrawimage. updatecolourtable-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UpdateColourTable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fcffdf9e7deaaac5a01f6559ee557c978fcda88f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360442"
---
# <a name="cdrawimageupdatecolourtable-method"></a>Cdrawimage. updatecolourtable-Methode

Die- `UpdateColourTable` Methode aktualisiert die Farbtabelle mit einer neuen Palette.

## <a name="syntax"></a>Syntax


```C++
void UpdateColourTable(
   HDC              hdc,
   BITMAPINFOHEADER *pbmi
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HDC* 
</dt> <dd>

Gerätekontext, der das Bild enthält.

</dd> <dt>

*pbmi* 
</dt> <dd>

Zeiger auf eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur, die die neue Palette enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




