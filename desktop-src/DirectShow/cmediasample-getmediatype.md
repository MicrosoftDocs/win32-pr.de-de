---
description: 'Die getmediatype-Methode ruft den Medientyp ab, wenn der Medientyp vom vorherigen Beispiel abweicht. Diese Methode implementiert die imediasample:: getmediatype-Methode.'
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: Cmediasample. getmediatype-Methode (amfilter. h)
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
ms.openlocfilehash: 9a067494d6236b824ef8fbbcb583ad50503297b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352910"
---
# <a name="cmediasamplegetmediatype-method"></a>Cmediasample. getmediatype-Methode

Die- `GetMediaType` Methode ruft den Medientyp ab, wenn der Medientyp vom vorherigen Beispiel abweicht. Diese Methode implementiert die [**imediasample:: getmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMediaType(
   AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PpMediaType* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur von am erhält. Wenn sich der Medientyp nicht im vorherigen Beispiel geändert hat, wird *\* PpMediaType* auf **null** festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                   | Beschreibung                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | Der Medientyp wurde im vorherigen Beispiel nicht geändert.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                                 |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                                     |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Medientyp abgeschlossen haben, geben Sie den Speicherblock frei, indem Sie die Dienstprogramm Funktion [**deletemediatype**](deletemediatype.md) aufrufen.

Die Member-Variable [**cmediasample:: m \_ pmediatype**](cmediasample-m-pmediatype.md) gibt den Medientyp an. Die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) gibt an, ob sich der Medientyp geändert hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




