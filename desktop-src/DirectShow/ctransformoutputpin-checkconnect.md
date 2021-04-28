---
description: 'CTransformOutputPin.CheckConnect-Methode: Die CheckConnect-Methode bestimmt, ob eine Pinverbindung geeignet ist.'
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
ms.openlocfilehash: 190acd2fbab5206b114b57719d350e3ad5eac0c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094948"
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

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Ausgabepins.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                                 |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Der Eingabepin des Filters ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CBaseOutputPin::CheckConnect-Methode.**](cbaseoutputpin-checkconnect.md) Sie ruft die [**CTransformFilter::CheckConnect-Methode**](ctransformfilter-checkconnect.md) des Filters auf, die \_ S OK in der Basisklasse zurückgibt. Die abgeleitete Klasse kann die **CTransformFilter::CheckConnect-Methode** überschreiben, um zusätzliche Überprüfungen durchzuführen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




