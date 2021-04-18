---
description: Die Methode checkheaderordinüberprüft eine BITMAPINFOHEADER-Struktur. Diese Methode ist nur für nicht komprimierte RGB-Typen, nicht für komprimierte Typen oder YUV-Typen nützlich.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: Cimagedisplay. checkheadergültigkeit-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckHeaderValidity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 803e8cd1a70c68f3e20c320978e9a350bdf23bdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364597"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a>Cimagedisplay. checkheadergültigkeit-Methode

Die- `CheckHeaderValidity` Methode überprüft eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur. Diese Methode ist nur für nicht komprimierte RGB-Typen, nicht für komprimierte Typen oder YUV-Typen nützlich.

## <a name="syntax"></a>Syntax


```C++
BOOL CheckHeaderValidity(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinput* 
</dt> <dd>

Zeiger auf eine [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur, die die **BITMAPINFOHEADER** -Struktur enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn der **BITMAPINFOHEADER** gültig ist, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Diese Methode überprüft, ob die Bild Dimensionen nicht negativ sind. der Komprimierungstyp ist BI \_ RGB-oder BI- \_ Bitfields; die Farbtiefe und die Farb Masken sind gültig. der **Biplane** -Member ist gleich 1, und die **bisize** -und **bisizeimage** -Member sind richtig. Er prüft außerdem ggf., ob häufige Fehler in den paletteneinträgen vorhanden sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagedisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




