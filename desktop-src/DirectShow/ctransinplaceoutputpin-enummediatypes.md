---
description: 'Die enummediatypes-Methode listet die bevorzugten Medientypen der PIN auf. Diese Methode implementiert die IPin:: enummediatypes-Methode.'
ms.assetid: 942c6594-3053-484a-a0f7-286dcd3f7550
title: Ctransinplaceoutputpin. enummediatypes-Methode (transip. h)
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
ms.openlocfilehash: 4d214004412264272c64d0efaf20a5da7e1ca3cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367610"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a>Ctransinplaceoutputpin. enummediatypes-Methode

Die `EnumMediaTypes` -Methode listet die bevorzugten Medientypen der PIN auf. Diese Methode implementiert die [**IPin:: enummediatypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) -Methode.

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

Empfängt einen Zeiger auf die [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                           | Beschreibung                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                                 |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>         | Nicht genügend Arbeitsspeicher.<br/>                     |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>             | **Null** -Zeiger.<br/>                        |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Die Eingabe-PIN des Filters ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt die **ienummediatypes** -Schnittstelle aus der upstreamausgabepin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplaceoutputpin-Klasse**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




