---
description: 'CTransInPlaceOutputPin.EnumMediaTypes-Methode: Die EnumMediaTypes-Methode aufzählt die bevorzugten Medientypen des Pins. Diese Methode implementiert die IPin::EnumMediaTypes-Methode.'
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
ms.openlocfilehash: 26dd58f23dc18a086c6c59f6f8a6a098e3449fea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084634"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a>CTransInPlaceOutputPin.EnumMediaTypes-Methode

Die `EnumMediaTypes` -Methode aufzählt die bevorzugten Medientypen des Pins. Diese Methode implementiert die [**IPin::EnumMediaTypes-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)

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

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                                           | Beschreibung                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Nicht genügend Arbeitsspeicher.<br/>                     |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>             | **NULL-Zeiger.**<br/>                        |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der Eingabepin des Filters ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt die **IEnumMediaTypes-Schnittstelle** vom Upstreamausgabepin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceOutputPin-Klasse**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




