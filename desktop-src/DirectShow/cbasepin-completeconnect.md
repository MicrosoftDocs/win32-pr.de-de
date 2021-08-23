---
description: 'CBasePin.CompleteConnect-Methode: Die CompleteConnect-Methode schließt eine Verbindung mit einem anderen Pin ab.'
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: CBasePin.CompleteConnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e31829829a99dc613cfeeeda7ad8a9871c1a3ec4fee99220b804b171bbdcdc29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074784"
---
# <a name="cbasepincompleteconnect-method"></a>CBasePin.CompleteConnect-Methode

Die `CompleteConnect` -Methode schließt eine Verbindung mit einem anderen Pin ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des anderen Pins.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode wird an beiden Pins am Ende des Verbindungsprozesses aufgerufen. Der Verbindungspin ruft ihn innerhalb der [**CBasePin::Verbinden-Methode**](cbasepin-connect.md) auf, und der empfangende Pin ruft ihn innerhalb der [**CBasePin::ReceiveConnection-Methode**](cbasepin-receiveconnection.md) auf.

In der Basisklasse gibt diese Methode einfach S \_ OK zurück. Wenn eine abgeleitete Klasse Anforderungen zum Abschließen einer Verbindung hat, sollte sie diese Methode überschreiben. Beispielsweise verwendet die [**CBaseOutputPin-Klasse**](cbaseoutputpin.md) diese Methode, um die Speicherzuweisung zu bestimmen.

Wenn bei dieser Methode ein Fehler auftritt, schlägt auch der gesamte Verbindungsversuch fehl, und der Pin wird vom empfangenden Pin getrennt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




