---
description: Die addpin-Methode fügt dem Filter eine neue Ausgabe-PIN hinzu.
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: CSource. addpin-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.AddPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 224550756f5935ce26c106ba01c9ef64f0767140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352833"
---
# <a name="csourceaddpin-method"></a>CSource. addpin-Methode

Die- `AddPin` Methode fügt dem Filter eine neue Ausgabe-PIN hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddPin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStream* 
</dt> <dd>

Zeiger auf das [**csourcestream**](csourcestream.md) -Objekt, das die PIN implementiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                   | Beschreibung                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg<br/>             |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine neue PIN erstellen, die von **csourcestream** abgeleitet ist, ruft der **csourcestream** -Konstruktor diese Methode automatisch auf, um dem Filter die Ausgabe-PIN hinzuzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSource-Klasse**](csource.md)
</dt> </dl>

 

 




