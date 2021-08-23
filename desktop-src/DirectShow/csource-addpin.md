---
description: Die AddPin-Methode fügt dem Filter einen neuen Ausgabepin hinzu.
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: CSource.AddPin-Methode (Source.h)
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
ms.openlocfilehash: a1c221d2fd032445587b52b0d0ae7f7744889254983fab82c7b282d06fee195e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953779"
---
# <a name="csourceaddpin-method"></a>CSource.AddPin-Methode

Die `AddPin` -Methode fügt dem Filter einen neuen Ausgabepin hinzu.

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

Zeiger auf das [**CSourceStream-Objekt,**](csourcestream.md) das den Pin implementiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                   | Beschreibung                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn Sie einen neuen, von **CSourceStream** abgeleiteten Pin erstellen, ruft der **CSourceStream-Konstruktor** diese Methode automatisch auf, um dem Filter den Ausgabepin hinzuzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSource-Klasse**](csource.md)
</dt> </dl>

 

 




