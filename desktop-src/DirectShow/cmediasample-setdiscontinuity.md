---
description: Die SetDiscontinuity-Methode gibt an, ob dieses Beispiel eine Unterbrechung im Datenstrom darstellt. Diese Methode implementiert die IMediaSample::SetDiscontinuity-Methode.
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: CMediaSample.SetDiscontinuity-Methode (Amfilter.h)
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
ms.openlocfilehash: 4189498c60a52692c057a867dba8bc48c43d2b1c32fbd6091738a3711102f4b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832180"
---
# <a name="cmediasamplesetdiscontinuity-method"></a>CMediaSample.SetDiscontinuity-Methode

Die `SetDiscontinuity` -Methode gibt an, ob dieses Beispiel eine Unterbrechung im Datenstrom darstellt. Diese Methode implementiert die [**IMediaSample::SetDiscontinuity-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bDiscont* 
</dt> <dd>

Boolescher Wert, der angibt, ob dieses Beispiel eine Diskontinuität ist. True **gibt an,** dass das Medienbeispiel im vorherigen Beispiel nicht mehr verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode aktualisiert die [**CMediaSample::m \_ dwFlags-Membervariable,**](cmediasample-m-dwflags.md) die die Diskontinuitätseigenschaft angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




