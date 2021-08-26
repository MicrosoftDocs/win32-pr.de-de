---
description: 'CBasePin.CheckConnect-Methode: Die CheckConnect-Methode bestimmt, ob eine Stecknadelverbindung geeignet ist.'
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: CBasePin.CheckConnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0a91e936f13c76ed4d99d7c5048820777afa47c9a52c260bb7f34acb702cb777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916850"
---
# <a name="cbasepincheckconnect-method"></a>CBasePin.CheckConnect-Methode

Die `CheckConnect` -Methode bestimmt, ob eine Stecknadelverbindung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des anderen Pins.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                               | Beschreibung                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Erfolg.<br/>                           |
| <dl> <dt>**VFW \_ E \_ UNGÜLTIGE \_ RICHTUNG**</dt> </dl> | Pin-Anweisungen sind nicht kompatibel.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode wird bei beiden Pins zu Beginn des Verbindungsprozesses aufgerufen. Der Verbindungspin ruft ihn innerhalb der [**CBasePin::Verbinden-Methode**](cbasepin-connect.md) auf, und der empfangende Pin ruft ihn innerhalb der [**CBasePin::ReceiveConnection-Methode**](cbasepin-receiveconnection.md) auf.

Verwenden Sie diese Methode, um zu bestimmen, ob der vom *pPin-Parameter* angegebene Pin für eine Verbindung geeignet ist. Die Basisklasse gibt einen Fehler zurück, wenn beide Pins die gleiche Richtung haben (beide Eingaben oder beide Ausgaben). Abgeleitete Klassen können diese Methode überschreiben, um andere Features im Pin zu überprüfen. Beispielsweise fragt die [**CBaseOutputPin-Klasse**](cbaseoutputpin.md) den Eingabepin für die [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ab.

Wenn bei dieser Methode ein Fehler auftritt, schlägt die Verbindung fehl, und die PIN ruft die [**CBasePin::BreakConnect-Methode**](cbasepin-breakconnect.md) auf. Verwenden **Sie BreakConnect,** um alle in erhaltenen Ressourcen frei zu `CheckConnect` geben. Wenn z. `CheckConnect` B. die **QueryInterface-Methode aufruft,** **muss BreakConnect** die -Schnittstelle frei geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




