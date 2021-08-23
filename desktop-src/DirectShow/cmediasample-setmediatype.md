---
description: Die SetMediaType-Methode legt den Medientyp für das Beispiel fest. Diese Methode implementiert die IMediaSample::SetMediaType-Methode.
ms.assetid: 4423cc1e-d6e1-49e7-9cc1-1a1d71a3497b
title: CMediaSample.SetMediaType-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e7059e0d9b2d91b6a938c67445f185a2c9be0daf5831c30b235918ab7820b1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832170"
---
# <a name="cmediasamplesetmediatype-method"></a>CMediaSample.SetMediaType-Methode

Die `SetMediaType` -Methode legt den Medientyp für das Beispiel fest. Diese Methode implementiert die [**IMediaSample::SetMediaType-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMediaType(
   AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaType* 
</dt> <dd>

Zeiger auf eine [**AM \_ MEDIA \_ TYPE-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                   | Beschreibung                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode legt die [**Membervariable CMediaSample::m \_ pMediaType**](cmediasample-m-pmediatype.md) fest, die den Medientyp angibt, und die [**CMediaSample::m \_ dwFlags-Membervariable,**](cmediasample-m-dwflags.md) die angibt, ob sich der Medientyp geändert hat.

Diese Methode macht eine Kopie der AM \_ MEDIA \_ TYPE-Struktur.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




