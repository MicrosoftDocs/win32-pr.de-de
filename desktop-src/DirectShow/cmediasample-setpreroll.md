---
description: 'Die setpreroll-Methode gibt an, ob es sich bei diesem Beispiel um ein vorab Beispiel handelt. Eine ein Vorlauf ausgeführt-Stichprobe sollte nicht angezeigt werden. Diese Methode implementiert die imediasample:: setpreroll-Methode.'
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: Cmediasample. setpreroll-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 594f26ebb738a986c85a14b88f8896b122b58f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369416"
---
# <a name="cmediasamplesetpreroll-method"></a>Cmediasample. setpreroll-Methode

Die- `SetPreroll` Methode gibt an, ob es sich bei diesem Beispiel um ein vorab Beispiel handelt. Eine ein Vorlauf ausgeführt-Stichprobe sollte nicht angezeigt werden. Diese Methode implementiert die [**imediasample:: setpreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bispreroll* 
</dt> <dd>

Boolescher Wert, der angibt, ob es sich um ein vorab Beispiel handelt. **True** gibt an, dass es sich um ein vorab Beispiel handelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode aktualisiert die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , die die ein Vorlauf ausgeführt-Eigenschaft angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




