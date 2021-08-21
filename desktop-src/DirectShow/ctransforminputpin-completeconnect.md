---
description: 'CTransformInputPin.CompleteConnect-Methode: Die CompleteConnect-Methode schließt eine Verbindung mit einem anderen Pin ab.'
ms.assetid: 568cee55-b9ea-4fc2-ac9d-0080b7de9790
title: CTransformInputPin.CompleteConnect-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8b92ae9830bc7083f5e7a091b1ffbed273d9b62068ca47c5ad85682347706653
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812820"
---
# <a name="ctransforminputpincompleteconnect-method"></a>CTransformInputPin.CompleteConnect-Methode

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

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBasePin::CompleteConnect-Methode.**](cbasepin-completeconnect.md) Sie ruft die [**CTransformFilter::CompleteConnect-Methode**](ctransformfilter-completeconnect.md) des Filters auf, die \_ S OK in der Basisklasse zurückgibt. Die abgeleitete Klasse kann die **CTransformFilter::CompleteConnect-Methode** überschreiben, um zusätzliche Überprüfungen durchzuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




