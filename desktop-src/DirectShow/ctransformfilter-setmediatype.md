---
description: Die setmediatype-Methode wird aufgerufen, wenn der Medientyp für einen der Pins des Filters festgelegt wird.
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: Ctransformfilter. setmediatype-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86e9eac76ccc178659935511d75b1676a136a1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361623"
---
# <a name="ctransformfiltersetmediatype-method"></a>Ctransformfilter. setmediatype-Methode

Die `SetMediaType` -Methode wird aufgerufen, wenn der Medientyp für einen der Pins des Filters festgelegt wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*direction* 
</dt> <dd>

Member der [**Pin- \_ Richtung**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerierten Typs, der eine PIN für den Filter angibt (Eingabe oder Ausgabe).

</dd> <dt>

*PMT* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die [**ctransforminputpin:: setmediatype**](ctransforminputpin-setmediatype.md) -Methode und die [**ctransformoutputpin:: setmediatype**](ctransformoutputpin-setmediatype.md) -Methode aufrufen diese Methode, wenn der Medientyp einer PIN festgelegt ist. Diese Methode führt keine Aktion in der Basisklasse durch, aber die abgeleitete Klasse kann Sie überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




