---
description: Die Methode "Methode" stellt mithilfe eines angegebenen Medientyps eine Verbindung mit einer anderen Pin her.
ms.assetid: b80cf2c0-7266-4dac-8633-d30a871c57d9
title: Cbasepin. ditconnection-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AttemptConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f80d81b5f105f528292a23f8b58257066b425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367808"
---
# <a name="cbasepinattemptconnection-method"></a>Cbasepin.. der Connection-Methode

Die- `AttemptConnection` Methode stellt mithilfe eines angegebenen Medientyps eine Verbindung mit einer anderen Pin her.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT AttemptConnection(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*preceivepin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der empfangenden PIN.

</dd> <dt>

*PMT* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                                | Beschreibung                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                          |
| <dl> <dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt> </dl> | Der Medientyp ist nicht zulässig.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode versucht, die beiden Pins mit einem bestimmten Medientyp zu verbinden. Wenn der Typ nicht zulässig ist, schlägt die Methode fehl, ohne andere Medientypen auszuprobieren.

Wenn der Medientyp zulässig ist, ruft diese Methode die [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) -Methode der empfangenden PIN auf. Anschließend wird die [**cbasepin:: completeconnect**](cbasepin-completeconnect.md) -Methode aufgerufen, um die Verbindung abzuschließen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




