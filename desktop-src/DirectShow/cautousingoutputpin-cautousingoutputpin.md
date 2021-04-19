---
description: Konstruktormethode. Der Konstruktor erhält Zugriff auf die angegebene PIN.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: Cautousingoutputpin. cautousingoutputpin-Konstruktor (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94bafcdcb6e44a07afdccea382d783c20a9ad2ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370289"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a>Cautousingoutputpin. cautousingoutputpin-Konstruktor

Konstruktormethode. Der Konstruktor erhält Zugriff auf die angegebene PIN.

## <a name="syntax"></a>Syntax


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*poutputpin* 
</dt> <dd>

Zeiger auf ein [**cdynamicoutputpin**](cdynamicoutputpin.md) -Objekt.

</dd> <dt>

*PHR* 
</dt> <dd>

Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert enthält. Der Wert muss S \_ OK lauten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn die-Methode zurückgegeben wird, gibt der Wert von *\* PHR* den Erfolg oder Misserfolg der Methode an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cautousingoutputpin-Klasse**](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




