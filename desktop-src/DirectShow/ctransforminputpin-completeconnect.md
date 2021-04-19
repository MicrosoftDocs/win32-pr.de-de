---
description: Die completeconnect-Methode schließt eine Verbindung mit einer anderen Pin ab.
ms.assetid: 568cee55-b9ea-4fc2-ac9d-0080b7de9790
title: Ctransforminputpin. completeconnect-Methode (Transfrm. h)
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
ms.openlocfilehash: 455517968481b9333fbeba590aca644b34b2f5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366715"
---
# <a name="ctransforminputpincompleteconnect-method"></a>Ctransforminputpin. completeconnect-Methode

Die- `CompleteConnect` Methode schließt eine Verbindung mit einer anderen Pin ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*preceivepin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen Pin.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasepin:: completeconnect**](cbasepin-completeconnect.md) -Methode. Er ruft die [**ctransformfilter:: completeconnect**](ctransformfilter-completeconnect.md) -Methode des Filters auf, die \_ in der Basisklasse "s OK" zurückgibt. Die abgeleitete Klasse kann die **ctransformfilter:: completeconnect** -Methode überschreiben, um zusätzliche Überprüfungen auszuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




