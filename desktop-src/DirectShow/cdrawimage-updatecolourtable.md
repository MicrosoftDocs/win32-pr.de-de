---
description: Die UpdateColourTable-Methode aktualisiert die Farbtabelle mit einer neuen Palette.
ms.assetid: 61ad98c6-a526-4aac-ad68-d44fadc668de
title: CDrawImage.UpdateColourTable-Methode (Winutil.h)
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
ms.openlocfilehash: 5a53413cd1aaf60c17031f126f0a158629f5c41f8ca94981d293f003afadda8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384030"
---
# <a name="cdrawimageupdatecolourtable-method"></a>CDrawImage.UpdateColourTable-Methode

Die `UpdateColourTable` -Methode aktualisiert die Farbtabelle mit einer neuen Palette.

## <a name="syntax"></a>Syntax


```C++
void UpdateColourTable(
   HDC              hdc,
   BITMAPINFOHEADER *pbmi
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hdc* 
</dt> <dd>

Gerätekontext, der das Bild enthält.

</dd> <dt>

*pbmi* 
</dt> <dd>

Zeiger auf eine [**BITMAPINFOHEADER-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) die die neue Palette enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDrawImage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




