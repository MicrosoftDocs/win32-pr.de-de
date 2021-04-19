---
description: 'Die checktransform-Methode überprüft, ob ein Eingabe Medientyp mit einem Ausgabe Medientyp kompatibel ist. Diese Methode überschreibt die ctransformfilter:: checktransform-Methode.'
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: Ctransinplacefilter. checktransform-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a80132723be0b70f2c4afe93306d7f581b7734c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367821"
---
# <a name="ctransinplacefilterchecktransform-method"></a>Ctransinplacefilter. checktransform-Methode

Die- `CheckTransform` Methode überprüft, ob ein Eingabe Medientyp mit einem Ausgabe Medientyp kompatibel ist. Diese Methode überschreibt die [**ctransformfilter:: checktransform**](ctransformfilter-checktransform.md) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MTiN* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Eingabetyp angibt.

</dd> <dt>

*mtout* 
</dt> <dd>

Zeiger auf ein **cmediatype** -Objekt, das den Ausgabetyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Der **ctransinplace** -Filter ruft niemals auf `CheckTransform` . Stattdessen verwenden alle Pin-Verbindungen [**ctransformfilter:: checkinputtype**](ctransformfilter-checkinputtype.md) , um den Medientyp zu überprüfen. dabei wird davon ausgegangen, dass die Eingabe-und Ausgabetypen immer Stimmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplacefilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




