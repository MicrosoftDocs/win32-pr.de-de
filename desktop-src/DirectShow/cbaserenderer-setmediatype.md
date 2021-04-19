---
description: Die setmediatype-Methode wird aufgerufen, wenn der Medientyp der PIN festgelegt ist.
ms.assetid: 91d88523-006e-49fe-92f3-92825fbb323b
title: Cbaserderderer. setmediatype-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ccb364545df514e098811ff6135e0c8cf72a329
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370909"
---
# <a name="cbaserenderersetmediatype-method"></a>Cbaserderderer. setmediatype-Methode

Die `SetMediaType` -Methode wird aufgerufen, wenn der Medientyp der PIN festgelegt ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die Eingabe-PIN ruft diese Methode von ihrer eigenen [**crendererinputpin:: setmediatype**](crendererinputpin-setmediatype.md) -Methode auf. Diese Methode führt in der Basisklasse keine Aktion aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




