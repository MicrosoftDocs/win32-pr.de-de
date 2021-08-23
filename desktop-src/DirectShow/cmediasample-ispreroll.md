---
description: Die IsPreroll-Methode bestimmt, ob es sich bei diesem Beispiel um ein Preroll-Beispiel handelt. Ein Vorabrollbeispiel sollte nicht angezeigt werden. Diese Methode implementiert die IMediaSample::IsPreroll-Methode.
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: CMediaSample.IsPreroll-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f4c4b192d72c5edcfdb9c318f7420ca6ae5797446ec4f99cb6871aad2abd241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634640"
---
# <a name="cmediasampleispreroll-method"></a>CMediaSample.IsPreroll-Methode

Die `IsPreroll` -Methode bestimmt, ob es sich bei diesem Beispiel um ein Preroll-Beispiel handelt. Ein Vorabrollbeispiel sollte nicht angezeigt werden. Diese Methode implementiert die [**IMediaSample::IsPreroll-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll)

## <a name="syntax"></a>Syntax


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn es sich bei dem Beispiel um ein Prerollbeispiel handelt, \_ andernfalls S FALSE.

## <a name="remarks"></a>Hinweise

Die [**Membervariable cMediaSample::m \_ dwFlags**](cmediasample-m-dwflags.md) gibt diese Eigenschaft an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




