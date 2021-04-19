---
description: Die checkConnect-Methode bestimmt, ob eine PIN-Verbindung geeignet ist.
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: Cbasepin. checkConnect-Methode (amfilter. h)
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
ms.openlocfilehash: 24d5c221da417fd1fc2b3f9f140536f825b2f9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373985"
---
# <a name="cbasepincheckconnect-method"></a>Cbasepin. checkConnect-Methode

Die- `CheckConnect` Methode bestimmt, ob eine PIN-Verbindung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen Pin.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                               | Beschreibung                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Erfolg.<br/>                           |
| <dl> <dt>**VFW \_ E \_ ungültige \_ Richtung**</dt> </dl> | PIN-Anweisungen sind nicht kompatibel.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird am Anfang des Verbindungsprozesses für beide Pins aufgerufen. Die Verbindungs-Pin ruft Sie aus der [**cbasepin:: Connect**](cbasepin-connect.md) -Methode ab, und die empfangende Pin ruft Sie innerhalb der [**cbasepin:: receiveconnection**](cbasepin-receiveconnection.md) -Methode auf.

Verwenden Sie diese Methode, um zu bestimmen, ob die vom *ppin* -Parameter angegebene PIN für eine Verbindung geeignet ist. Die-Basisklasse gibt einen Fehler zurück, wenn beide Pins die gleiche Richtung (sowohl Eingabe als auch beide Ausgaben) aufweisen. Abgeleitete Klassen können diese Methode überschreiben, um andere Funktionen in der PIN zu überprüfen. Beispielsweise fragt die [**cbaseoutputpin**](cbaseoutputpin.md) -Klasse die Eingabe-PIN für Ihre [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle ab.

Wenn diese Methode fehlschlägt, schlägt die Verbindung fehl, und die PIN Ruft die [**cbasepin:: breakconnect**](cbasepin-breakconnect.md) -Methode auf. Verwenden Sie **breakconnect** , um Ressourcen freizugeben, die in abgerufen wurden `CheckConnect` . Wenn z. b. `CheckConnect` die **QueryInterface** -Methode aufruft, muss **breakconnect** die-Schnittstelle freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




