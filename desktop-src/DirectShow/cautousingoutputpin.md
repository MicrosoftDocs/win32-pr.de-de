---
description: Die cautousingoutputpin-Klasse erhält Zugriff auf ein cdynamicoutputpin-Objekt und gibt Sie frei.
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: Cautousingoutputpin-Klasse (amfilter. h)
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
ms.openlocfilehash: b664267ce2ff0dbbeeba8bc74708c9c67e185ae4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371716"
---
# <a name="cautousingoutputpin-class"></a>Cautousingoutputpin-Klasse

Die **cautousingoutputpin** -Klasse erhält Zugriff auf ein [**cdynamicoutputpin**](cdynamicoutputpin.md) -Objekt und gibt Sie frei.

**Cautousingoutputpin** verfügt über folgende Typen von Membern:



| Öffentliche Methoden                                                           | BESCHREIBUNG                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**Cautousingoutputpin**](cautousingoutputpin-cautousingoutputpin.md)   | Konstruktormethode. Erhält Zugriff auf die angegebene PIN. |
| [**~ Cautousingoutputpin**](cautousingoutputpin--cautousingoutputpin.md) | Dekonstruktormethode. Erhält Zugriff auf die angegebene PIN.  |



 

## <a name="remarks"></a>Bemerkungen

Wenn bestimmte Methoden für [**cdynamicoutputpin**](cdynamicoutputpin.md)aufgerufen werden, muss der Aufrufer Zugriff auf die PIN erhalten und diesen Zugriff freigeben. Der Aufrufer verwendet die [**cdynamicoutputpin:: startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md) -Methode, um Zugriff zu erhalten. Zum Freigeben des Zugriffs wird die [**cdynamicoutputpin:: stopusingoutputpin**](cdynamicoutputpin-stopusingoutputpin.md) -Methode aufgerufen. Bei der **cautousingoutputpin** -Klasse handelt es sich um eine Hilfsklasse, die diese Aufgaben in den Konstruktor-und dekonstruktormethoden verarbeitet. Im folgenden Codebeispiel wird gezeigt, wie diese Klasse verwendet wird:


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
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Basisklassen Referenz](base-class-reference.md)
</dt> </dl>

 

 




