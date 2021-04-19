---
description: Die checkpaletteheader-Methode überprüft die Paletteneinträge in einer videoinfo-Struktur.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: Cimagedisplay. checkpaletteheader-Methode (winutil. h)
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
ms.openlocfilehash: 54c4f401d2e75aeb35ffc19d26690fa04a769c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361650"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a>Cimagedisplay. checkpaletteheader-Methode

Die- `CheckPaletteHeader` Methode überprüft die Paletteneinträge in einer [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur.

## <a name="syntax"></a>Syntax


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinput* 
</dt> <dd>

Zeiger auf eine **videoinfo** -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Paletteneinträge gültig sind, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Wenn das Bildformat nicht palettisiert ist, überprüft die Methode, ob **biclrused** gleich 0 (null) ist. Andernfalls überprüft die Methode, ob das **bicompression** -Flag BI \_ RGB ist. **biclrimportant** ist nicht größer als **biclrused**. und die Anzahl der Paletteneinträge unter Berücksichtigung der Farbtiefe den maximalen Wert nicht überschreitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagedisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




