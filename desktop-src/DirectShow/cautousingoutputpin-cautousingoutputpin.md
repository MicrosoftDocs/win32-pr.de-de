---
description: Konstruktormethode. Der Konstruktor erhält Zugriff auf den angegebenen Pin.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: CAutoUsingOutputPin.CAutoUsingOutputPin-Konstruktor (Amfilter.h)
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
ms.openlocfilehash: c0594eed7f253f7e540f843dfc3c3de6481d7dbede3f25d1534e52181ef0585b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057520"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a>CAutoUsingOutputPin.CAutoUsingOutputPin-Konstruktor

Konstruktormethode. Der Konstruktor erhält Zugriff auf den angegebenen Pin.

## <a name="syntax"></a>Syntax


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOutputPin* 
</dt> <dd>

Zeiger auf ein [**CDynamicOutputPin-Objekt.**](cdynamicoutputpin.md)

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf eine Variable, die einen **HRESULT-Wert** enthält. Der Wert muss S \_ OK sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn die Methode zurückgegeben wird, gibt der Wert *\* von phr* den Erfolg oder Fehler der Methode an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CAutoUsingOutputPin-Klasse**](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




