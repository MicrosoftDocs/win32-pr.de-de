---
description: 'CTransformOutputPin.CheckConnect-Methode: Die CheckConnect-Methode bestimmt, ob eine Stecknadelverbindung geeignet ist.'
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: CTransformOutputPin.CheckConnect-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b85c2197cf65465441387ecc661af71e0ddfa7ca912c3296ddee543d11c4784
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086990"
---
# <a name="ctransformoutputpincheckconnect-method"></a>CTransformOutputPin.CheckConnect-Methode

Die `CheckConnect` -Methode bestimmt, ob eine Stecknadelverbindung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPin* 
</dt> <dd>

Zeiger auf die IPin-Schnittstelle des [**Ausgabepins.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                                 |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Der Eingabepin des Filters ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBaseOutputPin::CheckConnect-Methode.**](cbaseoutputpin-checkconnect.md) Sie ruft die [**CTransformFilter::CheckConnect-Methode**](ctransformfilter-checkconnect.md) des Filters auf, die S \_ OK in der Basisklasse zurückgibt. Die abgeleitete Klasse kann die **CTransformFilter::CheckConnect-Methode** überschreiben, um zusätzliche Überprüfungen durchzuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




