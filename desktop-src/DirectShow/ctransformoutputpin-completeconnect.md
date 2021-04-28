---
description: 'CTransformOutputPin.CompleteConnect-Methode: Die CompleteConnect-Methode schließt eine Verbindung mit einem anderen Pin ab.'
ms.assetid: 14bc48bc-ddfb-4491-8d5b-9e5ac601ba04
title: CTransformOutputPin.CompleteConnect-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ab3d7e56473094b31c0d97d0e15c083ff61a21d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094918"
---
# <a name="ctransformoutputpincompleteconnect-method"></a>CTransformOutputPin.CompleteConnect-Methode

Die `CompleteConnect` -Methode schließt eine Verbindung mit einem anderen Pin ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des anderen Pins.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CBaseOutputPin::CompleteConnect-Methode.**](cbaseoutputpin-completeconnect.md) Sie ruft die [**CTransformFilter::CompleteConnect-Methode**](ctransformfilter-completeconnect.md) des Filters auf, die S \_ OK in der Basisklasse zurückgibt. Die abgeleitete Klasse kann die **CTransformFilter::CompleteConnect-Methode** überschreiben, um zusätzliche Überprüfungen durchzuführen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




