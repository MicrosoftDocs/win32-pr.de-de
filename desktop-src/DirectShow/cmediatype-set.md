---
description: Die cmediatype. Set-Methode (mtype. h) legt den Medientyp von einem anderen Medientyp fest. Die-Methode verwendet den cmtype-Parameter.
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: Cmediatype. Set-Methode (mtype. h)-cmtype [REF]-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bf14132660045afbd171173a38d3ea320ba1aa
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106352000"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a>Cmediatype. Set-Methode (mtype. h)-cmtype [REF]-Parameter

Die- `Set` Methode legt den Medientyp von einem anderen Medientyp fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cmtype* \[ atur\]
</dt> <dd>

Verweis auf ein [**cmediatype**](cmediatype.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " \_ OK" oder "E \_ outo" zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode kopiert den gesamten Medientyp aus *cmtype*.

## <a name="requirements"></a>Anforderungen

| Anforderung                   | Wert                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header  | Mtype. h (Include Streams. h)                                                                                     |
| Bibliothek | "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 




