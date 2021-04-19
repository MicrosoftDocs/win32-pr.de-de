---
description: Die checkmediatype-Methode bestimmt, ob der Filter einen bestimmten Medientyp akzeptiert.
ms.assetid: 90d26cf6-443c-4a06-98c6-ffa14e27ee41
title: Cbaserderderer. checkmediatype-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc0d4fc70e9ed64f9481d827cb678eb3ff9721d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351373"
---
# <a name="cbaserenderercheckmediatype-method"></a>Cbaserderderer. checkmediatype-Methode

Die- `CheckMediaType` Methode bestimmt, ob der Filter einen bestimmten Medientyp akzeptiert.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den vorgeschlagenen Medientyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn der vorgeschlagene Medientyp zulässig ist. Andernfalls gibt S \_ false oder einen Fehlercode zurück.

## <a name="remarks"></a>Bemerkungen

Die Eingabe-PIN ruft diese Methode aus ihrer eigenen [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode auf. Diese Methode muss von der abgeleiteten Klasse implementiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




