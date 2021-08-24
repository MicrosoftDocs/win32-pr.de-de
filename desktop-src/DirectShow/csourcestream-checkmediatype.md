---
description: Die CheckMediaType-Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert. Diese Methode implementiert die rein virtuelle CBasePin::CheckMediaType-Methode.
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: CSourceStream.CheckMediaType-Methode (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cb900d4de448b59eadb4cfd4de28aebf3ac07845fff6a2769c003d37cac846a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633930"
---
# <a name="csourcestreamcheckmediatype-method"></a>CSourceStream.CheckMediaType-Methode

Die `CheckMediaType` -Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert. Diese Methode implementiert die rein virtuelle [**CBasePin::CheckMediaType-Methode.**](cbasepin-checkmediatype.md)

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaType* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den vorgeschlagenen Medientyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                            | Beschreibung                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Dieser Pin unterstützt diesen Medientyp.<br/>        |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Der Pin unterstützt diesen Medientyp nicht.<br/> |



 

## <a name="remarks"></a>Hinweise

Standardmäßig unterstützt der Pin einen einzelnen Medientyp. Diese Methode ruft den unterstützten Typ ab, indem die Einzelparameterversion der [**CSourceStream::GetMediaType-Methode**](csourcestream-getmediatype.md) aufgerufen und mit dem vorgeschlagenen Typ verglichen wird. Wenn Ihr Pin mehrere Medientypen unterstützt, überschreiben Sie diese Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




