---
description: 'CTransInPlaceInputPin.EnumMediaTypes-Methode: Die EnumMediaTypes-Methode listet die bevorzugten Medientypen des Pins auf. Diese Methode implementiert die IPin::EnumMediaTypes-Methode.'
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: CTransInPlaceInputPin.EnumMediaTypes-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f0c60a3fd20887975011ba54fba374d0af880cb2711bb501a40d64c6a66f206
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076220"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a>CTransInPlaceInputPin.EnumMediaTypes-Methode

Die `EnumMediaTypes` -Methode listet die bevorzugten Medientypen des Pins auf. Diese Methode implementiert die [**IPin::EnumMediaTypes-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppEnum* 
</dt> <dd>

Empfängt einen Zeiger auf die [**IEnumMediaTypes-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                           | Beschreibung                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Nicht genügend Arbeitsspeicher.<br/>             |
| <dl> <dt>**E \_ POINTER**</dt> </dl>             | **NULL-Zeiger.**<br/>                |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der Ausgabepin ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode gibt die **IEnumMediaTypes-Schnittstelle** aus dem Downstreameingabepin zurück.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransInPlaceInputPin-Klasse**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




