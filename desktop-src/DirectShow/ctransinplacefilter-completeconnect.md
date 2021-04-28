---
description: 'CTransInPlaceFilter.CompleteConnect-Methode: Die CompleteConnect-Methode schließt eine Pinverbindung ab.'
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: CTransInPlaceFilter.CompleteConnect-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9cc0bc839a4e35c4ce896acdf50da10f0c2bb0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084788"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a>CTransInPlaceFilter.CompleteConnect-Methode

Die `CompleteConnect` -Methode schließt eine Stecknadelverbindung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*direction* 
</dt> <dd>

Member des [**aufzählten PIN \_ DIRECTION-Typs,**](/windows/win32/api/strmif/ne-strmif-pin_direction) der an gibt, welcher Pin im Filter die Verbindung hergestellt wird.

</dd> <dt>

*pReceivePin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des anderen Pins in diesem Verbindungsversuch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein **HRESULT zurück.** Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                                           | Beschreibung                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                             |
| <dl> <dt>**VFW \_ E \_ NOT \_ IN \_ GRAPH**</dt> </dl> | Der Filter befindet sich nicht in einem Filterdiagramm.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CTransformFilter::CompleteConnect-Methode.**](ctransformfilter-completeconnect.md)

Das Verhalten des Filters hängt von der Reihenfolge der Pinverbindungen ab:

-   Wenn der Eingabepin zuerst verbunden ist, verwendet die Verbindung eine temporäre Zuweisung. Wenn der Ausgabepin verbunden ist, verbindet der Filter den Eingabepin erneut. Das erneute Verbinden des Eingabepins führt dazu, dass der Upstreamfilter die Zuweisung neu aushandelt. An diesem Punkt schlägt der Eingabepin eine Zuweisung aus dem Downstreamfilter vor. Weitere Informationen finden Sie unter [**CTransInPlaceInputPin::GetAllocator**](ctransinplaceinputpin-getallocator.md).
-   Wenn der Ausgabepin zuerst verbunden wird, wählt der Ausgabepin keine Zuweisung aus. Wenn der Eingabepin verbunden ist, handelt er eine Zuweisung für beide Verbindungen aus. Wenn die Eingabe- und Ausgabemedientypen nicht identisch sind, verbindet der Filter den Ausgabepin mithilfe des Eingabetyps erneut.

Der Filter führt alle Stecknadelwiederherstellungen durch Aufrufen der [**CBaseFilter::ReconnectPin-Methode**](cbasefilter-reconnectpin.md) aus. Die **ReconnectPin-Methode** ruft wiederum die [**IFilterGraph2::ReconnectEx-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) im Filtergraph-Manager auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




