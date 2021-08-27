---
description: Die CheckPaletteHeader-Methode überprüft die Paletteneinträge in einer VIDEOINFO-Struktur.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: CImageDisplay.CheckPaletteHeader-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckPaletteHeader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6378a93ffced86546b8e95071e7f9bdc1398cdd1831aa18d41d62c6ea97caff0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087290"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a>CImageDisplay.CheckPaletteHeader-Methode

Die `CheckPaletteHeader` -Methode überprüft die Paletteneinträge in einer [**VIDEOINFO-Struktur.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)

## <a name="syntax"></a>Syntax


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInput* 
</dt> <dd>

Zeiger auf eine **VIDEOINFO-Struktur.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die Paletteneinträge gültig sind, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Wenn das Bildformat nicht palettiert ist, überprüft die Methode, ob **biClrUsed** gleich 0 (null) ist. Andernfalls überprüft die -Methode, ob **das biCompression-Flag** BI \_ RGB ist. **biClrImportant** ist nicht größer als **biClrUsed;** und die Anzahl der Paletteneinträge überschreitet den Maximalwert nicht, wenn die Farbtiefe angegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImageDisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




