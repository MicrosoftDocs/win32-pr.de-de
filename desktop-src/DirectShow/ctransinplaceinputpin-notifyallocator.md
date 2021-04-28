---
description: 'CTransInPlaceInputPin.NotifyAllocator-Methode: Die NotifyAllocator-Methode gibt eine Zuweisung für die Verbindung an. Diese Methode implementiert die IMemInputPin::NotifyAllocator-Methode.'
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: CTransInPlaceInputPin.NotifyAllocator-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca15be5dc1893a393e6052832cc7522f27355eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094748"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a>CTransInPlaceInputPin.NotifyAllocator-Methode

Die `NotifyAllocator` -Methode gibt eine Zuweisung für die Verbindung an. Diese Methode implementiert die [**IMemInputPin::NotifyAllocator-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAllocator* 
</dt> <dd>

Zeiger auf die [**IMemAllocator-Schnittstelle der Zuweisung.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

</dd> <dt>

*bReadOnly* 
</dt> <dd>

Flag, das angibt, ob Beispiele aus dieser Zuweisung schreibgeschützt sind. True **gibt an,** dass Beispiele schreibgeschützt sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                               | Beschreibung                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                   |
| <dl> <dt>**E \_ FAIL**</dt> </dl>    | Fehler<br/>                   |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl> | **NULL-Zeigerargument**<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Filter versucht, dieselbe Zuweisung für beide Pinverbindungen zu verwenden.

-   Wenn der Ausgabepin nicht verbunden ist, akzeptiert der Eingabepin automatisch die Zuweisung. Wenn der Ausgabepin verbunden ist, verbindet der Filter den Eingabepin erneut. An diesem Punkt versucht der Filter erneut, eine einzelne Zuweisung zu verwenden.
-   Wenn der Ausgabepin verbunden ist, akzeptiert der Eingabepin die Zuweisung. Der Ausgabepin verwendet auch die gleiche Zuweisung. Er ruft `NotifyAllocator` auf dem nachgeschalteten Eingabepin auf.

Der vorherige Fall weist die folgende Ausnahme auf:

-   Wenn die vorgeschlagene Zuweisung schreibgeschützt ist (d. h., der *bReadOnly-Parameter* ist **TRUE),** und der Filter die Stichproben ändern muss, muss der Filter zwei verschiedene Zuweisungen verwenden. Wenn der Upstreamfilter in diesem Fall die Verwendung der Zuweisung des Downstreamfilters vorschlägt, gibt die Methode E \_ FAIL zurück.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceInputPin-Klasse**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




