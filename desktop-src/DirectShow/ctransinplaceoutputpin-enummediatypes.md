---
description: 'CTransInPlaceOutputPin.EnumMediaTypes-Methode: Die EnumMediaTypes-Methode listet die bevorzugten Medientypen des Pins auf. Diese Methode implementiert die IPin::EnumMediaTypes-Methode.'
ms.assetid: 942c6594-3053-484a-a0f7-286dcd3f7550
title: CTransInPlaceOutputPin.EnumMediaTypes-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7a351f947b0526b8daf77b0b15ea0d2a2894ef6ff90390be484b5d0ce4b7fa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076170"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a>CTransInPlaceOutputPin.EnumMediaTypes-Methode

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



| Rückgabecode                                                                                           | Beschreibung                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Nicht genügend Arbeitsspeicher.<br/>                     |
| <dl> <dt>**E \_ POINTER**</dt> </dl>             | **NULL-Zeiger.**<br/>                        |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der Eingabepin des Filters ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode gibt die **IEnumMediaTypes-Schnittstelle** vom Upstreamausgabepin zurück.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransInPlaceOutputPin-Klasse**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




