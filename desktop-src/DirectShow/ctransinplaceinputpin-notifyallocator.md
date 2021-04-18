---
description: 'Die notifyzucator-Methode gibt eine Zuweisung für die Verbindung an. Mit dieser Methode wird die IMemInputPin:: notifyzucator-Methode implementiert.'
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: Ctransinplaceinputpin. notifyzucator-Methode (transip. h)
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
ms.openlocfilehash: 74578243ce780e09d7435f9dd4b70bd9497e1e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357596"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a>Ctransinplaceinputpin. notifyzucator-Methode

Die- `NotifyAllocator` Methode gibt eine Zuweisung für die Verbindung an. Mit dieser Methode wird die [**IMemInputPin:: notifyzucator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) -Methode implementiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pallocator* 
</dt> <dd>

Ein Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners.

</dd> <dt>

*nur Bread* 
</dt> <dd>

Flag, das angibt, ob Beispiele aus dieser Zuweisung schreibgeschützt sind. **True** gibt an, dass die Beispiele schreibgeschützt sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                               | Beschreibung                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                   |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>    | Fehler<br/>                   |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeigerargument<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Filter versucht, die gleiche Zuweisung für beide Pin-Verbindungen zu verwenden.

-   Wenn die Ausgabe-PIN nicht verbunden ist, akzeptiert die Eingabe-PIN automatisch die Zuweisung. Wenn die Ausgabe-PIN verbunden ist, stellt der Filter erneut eine Verbindung mit der eingabepin her. An diesem Punkt versucht der Filter erneut, eine einzelne Zuweisung zu verwenden.
-   Wenn die Ausgabe-PIN verbunden ist, akzeptiert die Eingabe-PIN die Zuweisung. Die Ausgabe-PIN verwendet auch die gleiche Zuweisung. Er ruft `NotifyAllocator` für die downstreameingabepin auf.

Der vorherige Fall hat die folgende Ausnahme:

-   Wenn die vorgeschlagene Zuweisung schreibgeschützt ist (d. h., der *bReadOnly* -Parameter ist **true**) und der Filter die Beispiele ändern muss, muss der Filter zwei verschiedene Zuweisungen verwenden. Wenn der upstreamfilter in diesem Fall vorschlägt, die Zuweisung des downstreamfilters zu verwenden, gibt die Methode E \_ Fail zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplaceinputpin-Klasse**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




