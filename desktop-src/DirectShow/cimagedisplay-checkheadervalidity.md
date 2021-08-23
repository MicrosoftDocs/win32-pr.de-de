---
description: Die CheckHeaderValidity-Methode überprüft eine BITMAPINFOHEADER-Struktur. Diese Methode ist nur für nicht komprimierte RGB-Typen nützlich, nicht für komprimierte Typen oder YUV-Typen.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: CImageDisplay.CheckHeaderValidity-Methode (Winutil.h)
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
ms.openlocfilehash: 25c8ce12f7e383e04942184e3897d0ddc52700a1a621844719d94f54f60203ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652360"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a>CImageDisplay.CheckHeaderValidity-Methode

Die `CheckHeaderValidity` -Methode überprüft eine [**BITMAPINFOHEADER-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) Diese Methode ist nur für nicht komprimierte RGB-Typen nützlich, nicht für komprimierte Typen oder YUV-Typen.

## <a name="syntax"></a>Syntax


```C++
BOOL CheckHeaderValidity(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInput* 
</dt> <dd>

Zeiger auf eine [**VIDEOINFO-Struktur,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) die die **BITMAPINFOHEADER-Struktur** enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** **wenn BITMAPINFOHEADER** gültig ist, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Diese Methode überprüft, ob die Bilddimensionen nicht negativ sind. Der Komprimierungstyp ist BI RGB oder BI BITFIELDS. Die Farbtiefe und farbmasken sind gültig, das BiPlanes-Member ist gleich 1, und die \_ \_ Elemente **biSize** und **biSizeImage**  sind korrekt. Außerdem werden häufige Fehler in den Paletteneinträgen überprüft, sofern diese auftreten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImageDisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




