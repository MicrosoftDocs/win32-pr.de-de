---
description: Die SetPreroll-Methode gibt an, ob es sich bei diesem Beispiel um ein Preroll-Beispiel handelt. Ein Vorabrollbeispiel sollte nicht angezeigt werden. Diese Methode implementiert die IMediaSample::SetPreroll-Methode.
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: CMediaSample.SetPreroll-Methode (Amfilter.h)
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
ms.openlocfilehash: 410031ccf60e830c51615d267d3324167169c5de7960f79dc05b8c9e267463bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832100"
---
# <a name="cmediasamplesetpreroll-method"></a>CMediaSample.SetPreroll-Methode

Die `SetPreroll` -Methode gibt an, ob es sich bei diesem Beispiel um ein Prerollbeispiel handelt. Ein Vorabrollbeispiel sollte nicht angezeigt werden. Diese Methode implementiert die [**IMediaSample::SetPreroll-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bIsPreroll* 
</dt> <dd>

Boolescher Wert, der angibt, ob es sich um ein Prerollbeispiel handelt. True gibt an, dass dies ein Vorabrollbeispiel ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode aktualisiert die [**CMediaSample::m \_ dwFlags-Membervariable,**](cmediasample-m-dwflags.md) die die Preroll-Eigenschaft angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




