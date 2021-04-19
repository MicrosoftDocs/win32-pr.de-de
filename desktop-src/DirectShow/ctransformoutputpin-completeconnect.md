---
description: Die completeconnect-Methode schließt eine Verbindung mit einer anderen Pin ab.
ms.assetid: 14bc48bc-ddfb-4491-8d5b-9e5ac601ba04
title: Ctransformoutputpin. completeconnect-Methode (Transfrm. h)
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
ms.openlocfilehash: 8d0c9c9fc7096191d7cdedffa21e2639fa0750ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362150"
---
# <a name="ctransformoutputpincompleteconnect-method"></a>Ctransformoutputpin. completeconnect-Methode

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

Diese Methode überschreibt die [**cbaseoutputpin:: completeconnect**](cbaseoutputpin-completeconnect.md) -Methode. Er ruft die [**ctransformfilter:: completeconnect**](ctransformfilter-completeconnect.md) -Methode des Filters auf, die \_ in der Basisklasse "s OK" zurückgibt. Die abgeleitete Klasse kann die **ctransformfilter:: completeconnect** -Methode überschreiben, um zusätzliche Überprüfungen auszuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




