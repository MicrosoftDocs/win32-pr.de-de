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
ms.openlocfilehash: fee207d7a17f12cc81036fbd4f82ec49a99f4a31
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096038"
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

## <a name="remarks"></a>Bemerkungen

Diese Methode wird an beiden Pins am Ende des Verbindungsprozesses aufgerufen. Der Verbindungspin ruft ihn innerhalb der [**CBasePin::Connect-Methode**](cbasepin-connect.md) auf, und der empfangende Pin ruft ihn innerhalb der [**CBasePin::ReceiveConnection-Methode**](cbasepin-receiveconnection.md) auf.

In der Basisklasse gibt diese Methode einfach S \_ OK zurück. Wenn eine abgeleitete Klasse Anforderungen zum Abschließen einer Verbindung hat, sollte sie diese Methode überschreiben. Beispielsweise verwendet die [**CBaseOutputPin-Klasse**](cbaseoutputpin.md) diese Methode, um die Speicherzuweisung zu bestimmen.

Wenn bei dieser Methode ein Fehler auftritt, schlägt auch der gesamte Verbindungsversuch fehl, und der Pin wird vom empfangenden Pin getrennt.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




