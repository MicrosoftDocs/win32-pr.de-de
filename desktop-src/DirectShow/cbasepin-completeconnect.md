---
description: Die completeconnect-Methode schließt eine Verbindung mit einer anderen Pin ab.
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Cbasepin. completeconnect-Methode (amfilter. h)
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
ms.openlocfilehash: 9068bf63d3168a8c6d9e1bca2ef709f63e80a3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354784"
---
# <a name="cbasepincompleteconnect-method"></a>Cbasepin. completeconnect-Methode

Die- `CompleteConnect` Methode schließt eine Verbindung mit einer anderen Pin ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*preceivepin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen Pin.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird auf beiden Pins am Ende des Verbindungsprozesses aufgerufen. Die Verbindungs-Pin ruft Sie aus der [**cbasepin:: Connect**](cbasepin-connect.md) -Methode ab, und die empfangende Pin ruft Sie innerhalb der [**cbasepin:: receiveconnection**](cbasepin-receiveconnection.md) -Methode auf.

In der Basisklasse gibt diese Methode einfach S \_ OK zurück. Wenn eine abgeleitete Klasse über Anforderungen zum Abschließen einer Verbindung verfügt, sollte diese Methode überschrieben werden. Beispielsweise verwendet die [**cbaseoutputpin**](cbaseoutputpin.md) -Klasse diese Methode, um die Speicherzuweisung zu entscheiden.

Wenn diese Methode fehlschlägt, schlägt der allgemeine Verbindungsversuch ebenfalls fehl, und die PIN trennt die Verbindung mit der empfangenden PIN.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




