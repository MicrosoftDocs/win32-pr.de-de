---
description: Die CheckMediaType-Methode bestimmt, ob der Filter einen bestimmten Medientyp akzeptiert.
ms.assetid: 90d26cf6-443c-4a06-98c6-ffa14e27ee41
title: CBaseRenderer.CheckMediaType-Methode (Renbase.h)
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
ms.openlocfilehash: 8de57346138b4683f59cfa612f01fff1ef3d8fd9aceec9b34daee49bfa74ebbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157980"
---
# <a name="cbaserenderercheckmediatype-method"></a>CBaseRenderer.CheckMediaType-Methode

Die `CheckMediaType` -Methode bestimmt, ob der Filter einen bestimmten Medientyp akzeptiert.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den vorgeschlagenen Medientyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn der vorgeschlagene Medientyp akzeptabel ist. Andernfalls wird S \_ FALSE oder ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Hinweise

Der Eingabepin ruft diese Methode aus ihrer eigenen [**CBasePin::CheckMediaType-Methode**](cbasepin-checkmediatype.md) auf. Die abgeleitete Klasse muss diese Methode implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




