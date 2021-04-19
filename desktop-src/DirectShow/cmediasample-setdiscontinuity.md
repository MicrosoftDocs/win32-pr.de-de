---
description: 'Die setdiscontinuity-Methode gibt an, ob dieses Beispiel eine Unterbrechung im Datenstrom darstellt. Diese Methode implementiert die imediasample:: setdiscontinuity-Methode.'
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: Cmediasample. setdiscontinuity-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35565b2cee0284d0e5b9f85d7335a630b5f54e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352865"
---
# <a name="cmediasamplesetdiscontinuity-method"></a>Cmediasample. setdiscontinuity-Methode

Die- `SetDiscontinuity` Methode gibt an, ob dieses Beispiel eine Unterbrechung im Datenstrom darstellt. Diese Methode implementiert die [**imediasample:: setdiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bdis-Datei* 
</dt> <dd>

Boolescher Wert, der angibt, ob es sich bei diesem Beispiel um eine Diskontinuität handelt. Wenn der Wert **true** ist, wird das Medien Beispiel mit dem vorherigen Beispiel diskontinuierlich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode aktualisiert die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , die die Diskontinuität-Eigenschaft angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




