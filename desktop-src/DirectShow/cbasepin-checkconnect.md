---
description: 'CBasePin.CheckConnect-Methode: Die CheckConnect-Methode bestimmt, ob eine Pinverbindung geeignet ist.'
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
ms.openlocfilehash: 314d3e1ce0e73e60ea07bb4f7270fa04f69750c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096048"
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
| <dl> <dt>**VFW \_ E \_ INVALID \_ DIRECTION**</dt> </dl> | Stecknadelrichtungen sind nicht kompatibel.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird zu Beginn des Verbindungsprozesses für beide Pins aufgerufen. Der Verbindende Pin ruft ihn aus der [**CBasePin::Connect-Methode**](cbasepin-connect.md) auf, und der empfangende Pin ruft ihn aus der [**CBasePin::ReceiveConnection-Methode**](cbasepin-receiveconnection.md) auf.

Verwenden Sie diese Methode, um zu bestimmen, ob der durch den *pPin-Parameter* angegebene Pin für eine Verbindung geeignet ist. Die Basisklasse gibt einen Fehler zurück, wenn beide Pins die gleiche Richtung aufweisen (eingabe oder beide Ausgabe). Abgeleitete Klassen können diese Methode überschreiben, um andere Features im Pin zu überprüfen. Beispielsweise fragt die [**CBaseOutputPin-Klasse**](cbaseoutputpin.md) den Eingabepin für die [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ab.

Wenn bei dieser Methode ein Fehler auftritt, schlägt die Verbindung fehl, und der Pin ruft die [**CBasePin::BreakConnect-Methode**](cbasepin-breakconnect.md) auf. Verwenden Sie **BreakConnect,** um alle in abgerufenen Ressourcen frei zu `CheckConnect` machen. Wenn beispielsweise `CheckConnect` die **QueryInterface-Methode** aufruft, muss **BreakConnect** die -Schnittstelle freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




