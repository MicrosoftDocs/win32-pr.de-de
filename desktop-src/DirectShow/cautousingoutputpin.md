---
description: Die CAutoUsingOutputPin-Klasse erhält und gibt den Zugriff auf ein CDynamicOutputPin-Objekt frei.
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: CAutoUsingOutputPin-Klasse (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 141c65507a0d983a2b4531b93617ed741e7403b8b2a5ead9c196f78dcf61acdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955379"
---
# <a name="cautousingoutputpin-class"></a>CAutoUsingOutputPin-Klasse

Die **CAutoUsingOutputPin-Klasse** erhält und gibt den Zugriff auf ein [**CDynamicOutputPin-Objekt**](cdynamicoutputpin.md) frei.

**CAutoUsingOutputPin** verfügt über die folgenden Membertypen:



| Öffentliche Methoden                                                           | Beschreibung                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md)   | Konstruktormethode. Erhält Zugriff auf den angegebenen Pin. |
| [**~CAutoUsingOutputPin**](cautousingoutputpin--cautousingoutputpin.md) | Destruktormethode. Erhält Zugriff auf den angegebenen Pin.  |



 

## <a name="remarks"></a>Hinweise

Wenn bestimmte Methoden für [**CDynamicOutputPin**](cdynamicoutputpin.md)aufgerufen werden, muss der Aufrufer Zugriff auf den Pin erhalten und diesen Zugriff dann wieder frei geben. Um Zugriff zu erhalten, verwendet der Aufrufer die [**CDynamicOutputPin::StartUsingOutputPin-Methode.**](cdynamicoutputpin-startusingoutputpin.md) Um den Zugriff frei zu geben, ruft er die [**CDynamicOutputPin::StopUsingOutputPin-Methode**](cdynamicoutputpin-stopusingoutputpin.md) auf. Die **CAutoUsingOutputPin-Klasse** ist eine Hilfsklasse, die diese Aufgaben in ihren Konstruktor- und Destruktormethoden behandelt. Im folgenden Codebeispiel wird die Verwendung dieser Klasse veranschaulicht:


```
CDynamicOutputPin *pPin;
HRESULT hr = S_OK;  // Important! Initialize to S_OK.

// TODO: Obtain a pointer to the pin (not shown).

// Scope for lock.
{
    // Hold lock on pin.
    CAutoUsingOutputPin UsingPin(pPin, &hr)

    if (SUCCEEDED(hr)) 
    {

        // Safe to use the pin.
        hr = pPin->Deliver(pSample);

    }

} // Object goes out of scope here.

// No longer safe to use the pin.
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Basisklassenreferenz](base-class-reference.md)
</dt> </dl>

 

 




