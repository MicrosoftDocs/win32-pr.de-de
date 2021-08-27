---
description: Die CheckVideoType-Methode überprüft, ob ein angegebenes VIDEOINFO-Format mit dem Anzeigeformat kompatibel ist.
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: CImageDisplay.CheckVideoType-Methode (Winutil.h)
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
ms.openlocfilehash: de6389e22868fe529b5038fe6be1403748dd5a01d22a242c41f9e6c6b8f86808
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108490"
---
# <a name="cimagedisplaycheckvideotype-method"></a>CImageDisplay.CheckVideoType-Methode

Die `CheckVideoType` -Methode überprüft, ob ein angegebenes [**VIDEOINFO-Format**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) mit dem Anzeigeformat kompatibel ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckVideoType(
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

Gibt S \_ OK zurück, wenn das Format kompatibel ist, \_ andernfalls E INVALIDARG.

## <a name="remarks"></a>Hinweise

Diese Methode gibt S OK zurück, wenn der vorgeschlagene Typ problemlos unter \_ den aktuellen Anzeigeeinstellungen angezeigt werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImageDisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




