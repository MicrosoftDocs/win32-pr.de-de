---
description: Die completeconnect-Methode schließt eine PIN-Verbindung ab.
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: Ctransinplacefilter. completeconnect-Methode (transip. h)
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
ms.openlocfilehash: 4fdc9d1d5567cda2e4b0fd4a351136405493ef61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372734"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a>Ctransinplacefilter. completeconnect-Methode

Die- `CompleteConnect` Methode schließt eine PIN-Verbindung ab.

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

Member des enumerierten Typs der [**Pin- \_ Richtung**](/windows/win32/api/strmif/ne-strmif-pin_direction) , der angibt, welche PIN im Filter die Verbindung herstellen soll.

</dd> <dt>

*preceivepin* 
</dt> <dd>

Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen PIN bei diesem Verbindungsversuch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein **HRESULT** zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                           | Beschreibung                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                             |
| <dl> <dt>**VFW \_ E \_ nicht \_ im \_ Diagramm**</dt> </dl> | Der Filter befindet sich nicht in einem Filter Diagramm.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**ctransformfilter:: completeconnect**](ctransformfilter-completeconnect.md) -Methode.

Das Verhalten des Filters hängt von der Reihenfolge der PIN-Verbindungen ab:

-   Wenn die Eingabe-PIN zuerst verbunden ist, verwendet die Verbindung eine temporäre Zuweisung. Wenn die Ausgabe-PIN verbunden ist, verbindet der Filter die eingabepin erneut. Das erneute Verbinden der Eingabe-PIN bewirkt, dass der upstreamfilter die Zuweisung erneut ausgehandelt. An diesem Punkt schlägt die Eingabe-PIN eine Zuweisung vom downstreamfilter vor. Weitere Informationen finden Sie unter [**ctransinplaceinputpin:: getallocator**](ctransinplaceinputpin-getallocator.md).
-   Wenn die Ausgabe-PIN zuerst verbunden ist, wählt die Ausgabepin keinen Zuweiser aus. Wenn die eingabepin verbunden ist, aushandelte Sie eine Zuweisung für beide Verbindungen. Wenn die Eingabe-und Ausgabemedien Typen nicht identisch sind, verbindet der Filter die Ausgabe-PIN mit dem Eingabetyp erneut.

Der Filter führt alle Pin-Neuverbindungen durch Aufrufen der [**cbasefilter:: reconnectpin**](cbasefilter-reconnectpin.md) -Methode aus. Die **reconnectpin** -Methode wiederum ruft die [**IFilterGraph2:: reconnectex**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) -Methode für den Filter Graph-Manager auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplacefilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




