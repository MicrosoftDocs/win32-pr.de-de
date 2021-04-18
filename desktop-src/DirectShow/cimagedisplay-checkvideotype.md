---
description: Die checkvideotype-Methode überprüft, ob ein bestimmtes videoinfo-Format mit dem Anzeige Format kompatibel ist.
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: Cimagedisplay. checkvideotype-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckVideoType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7db198270804053993352c4969b924fa7edc891f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372680"
---
# <a name="cimagedisplaycheckvideotype-method"></a>Cimagedisplay. checkvideotype-Methode

Die- `CheckVideoType` Methode überprüft, ob ein angegebenes [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Format mit dem Anzeige Format kompatibel ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckVideoType(
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

Gibt S \_ OK zurück, wenn das Format kompatibel ist, \_ andernfalls E invalidArg.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt S \_ OK zurück, wenn der vorgeschlagene Typ unter den aktuellen Anzeigeeinstellungen problemlos angezeigt werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagedisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




