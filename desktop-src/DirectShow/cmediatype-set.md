---
description: Die CMediaType.Set-Methode (Mtype.h) legt den Medientyp von einem anderen Medientyp fest. Die -Methode verwendet den Parameter "cmtype".
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: CMediaType.Set-Methode (Mtype.h) – cmtype [ref]-Parameter
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
ms.openlocfilehash: 0a317b23b4870ad6e68032ed23f846a81019be358974ebbe75e2a5859db71303
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585880"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a>CMediaType.Set-Methode (Mtype.h) – cmtype [ref]-Parameter

Die `Set` -Methode legt den Medientyp von einem anderen Medientyp fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cmtype* \[ Ref\]
</dt> <dd>

Verweis auf ein [**CMediaType-Objekt.**](cmediatype.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder E \_ OUTOFMEMORY zurück.

## <a name="remarks"></a>Hinweise

Diese Methode kopiert den gesamten Medientyp aus *cmtype.*

## <a name="requirements"></a>Anforderungen

| Anforderung                   | Wert                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header  | Mtype.h (include Streams.h)                                                                                     |
| Bibliothek | Strmbase.lib (Einzelhandels-Builds); Strmbasd.lib (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




