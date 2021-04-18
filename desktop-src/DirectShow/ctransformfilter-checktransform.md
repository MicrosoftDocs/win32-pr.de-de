---
description: Die checktransform-Methode überprüft, ob ein Eingabe Medientyp mit einem Ausgabe Medientyp kompatibel ist.
ms.assetid: 349145e5-c12d-41df-ae37-7846f8aaa423
title: Ctransformfilter. checktransform-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b3302304e6a0f9df41005f7ed63d9316a3cd410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368475"
---
# <a name="ctransformfilterchecktransform-method"></a>Ctransformfilter. checktransform-Methode

Die- `CheckTransform` Methode überprüft, ob ein Eingabe Medientyp mit einem Ausgabe Medientyp kompatibel ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MTiN* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Eingabetyp angibt.

</dd> <dt>

*mtout* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Ausgabetyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                                | Beschreibung                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Die Medientypen sind kompatibel.<br/>     |
| <dl> <dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt> </dl> | Die Medientypen sind nicht kompatibel.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode muss von der abgeleiteten Klasse implementiert werden. Gibt \_ OK zurück, wenn der Filter beide angegebenen Medientypen akzeptieren kann, andernfalls einen Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




