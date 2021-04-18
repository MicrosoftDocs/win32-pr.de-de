---
description: Die checkmediatype-Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: Ctransformoutputpin. checkmediatype-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3c2bc617a5ff56a8b82184700af85e2634960ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365399"
---
# <a name="ctransformoutputpincheckmediatype-method"></a>Ctransformoutputpin. checkmediatype-Methode

Die- `CheckMediaType` Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MTiN* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den vorgeschlagenen Medientyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                                 |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Die Eingabe-PIN des Filters ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode implementiert die rein virtuelle [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode. Die Methode schlägt fehl, wenn die Eingabe-PIN des Filters nicht verbunden ist. Andernfalls wird die [**ctransformfilter:: checktransform**](ctransformfilter-checktransform.md) -Methode des Filters aufgerufen, die ebenfalls rein virtuell ist. Die abgeleitete Klasse des Filters muss **checktransform** implementieren, das bestimmt, ob der vorgeschlagene Ausgabe Medientyp mit dem Eingabe Medientyp kompatibel ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




