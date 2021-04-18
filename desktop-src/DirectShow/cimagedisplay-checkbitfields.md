---
description: Die checkbitfields-Methode überprüft die Farb Masken in einer videoinfo-Struktur.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: Cimagedisplay. checkbitfields-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckBitFields
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade581dad5e53c2454df52e387653e44d6d4ad2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358257"
---
# <a name="cimagedisplaycheckbitfields-method"></a>Cimagedisplay. checkbitfields-Methode

Die- `CheckBitFields` Methode überprüft die Farb Masken in einer [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur.

## <a name="syntax"></a>Syntax


```C++
BOOL CheckBitFields(
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

Gibt **true** zurück, wenn die Farb Masken gültig sind, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Diese Methode überprüft, ob die Farb Maske für jede Farbkomponente zwischen 1 und 8 Bits lang ist, und dass jede Farb Maske eine zusammenhängende Sequenz von Bits ist. Diese Methode wird nur aufgerufen, wenn der **bicompression** -Member auf BI Bitfields festgelegt ist \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagedisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




