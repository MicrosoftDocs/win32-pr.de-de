---
description: Die GetMediaType-Methode ruft den Medientyp ab, wenn sich der Medientyp vom vorherigen Beispiel unterscheidet. Diese Methode implementiert die IMediaSample::GetMediaType-Methode.
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: CMediaSample.GetMediaType-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee7b5464ff2620dbc0247b006dc323232131de3936d2c5e56f2232b67c00ba5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832300"
---
# <a name="cmediasamplegetmediatype-method"></a>CMediaSample.GetMediaType-Methode

Die `GetMediaType` -Methode ruft den Medientyp ab, wenn sich der Medientyp vom vorherigen Beispiel unterscheidet. Diese Methode implementiert die [**IMediaSample::GetMediaType-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMediaType(
   AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppMediaType* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf eine [**AM \_ MEDIA \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) empfängt. Wenn sich der Medientyp nicht im vorherigen Beispiel geändert hat, wird *\* ppMediaType* auf **NULL** festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                   | Beschreibung                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | Der Medientyp hat sich gegenüber dem vorherigen Beispiel nicht geändert.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                                     |



 

## <a name="remarks"></a>Hinweise

Wenn Sie mit dem Medientyp fertig sind, geben Sie den Speicherblock frei, indem Sie die [**DeleteMediaType-Hilfsprogrammfunktion**](deletemediatype.md) aufrufen.

Die [**CMediaSample::m \_ pMediaType-Membervariable**](cmediasample-m-pmediatype.md) gibt den Medientyp an. Die [**Membervariable CMediaSample::m \_ dwFlags**](cmediasample-m-dwflags.md) gibt an, ob sich der Medientyp geändert hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




