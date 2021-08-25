---
description: Die AttemptConnection-Methode stellt mithilfe eines angegebenen Medientyps eine Verbindung mit einem anderen Pin her.
ms.assetid: b80cf2c0-7266-4dac-8633-d30a871c57d9
title: CBasePin.AttemptConnection-Methode (Amfilter.h)
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
ms.openlocfilehash: e70683d5307b81db14d23fec2c163b085cccaf64b7926eb41efdb5dfe9ac7611
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872395"
---
# <a name="cbasepinattemptconnection-method"></a>CBasePin.AttemptConnection-Methode

Die `AttemptConnection` -Methode stellt mithilfe eines angegebenen Medientyps eine Verbindung mit einem anderen Pin her.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT AttemptConnection(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des empfangenden Pins.

</dd> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die werte in der folgenden Tabelle.



| Rückgabecode                                                                                                | Beschreibung                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                          |
| <dl> <dt>**VFW \_ \_ E-TYP \_ NICHT \_ AKZEPTIERT**</dt> </dl> | Der Medientyp ist nicht akzeptabel.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode versucht, die beiden Pins mit einem bestimmten Medientyp zu verbinden. Wenn der Typ nicht akzeptabel ist, schlägt die Methode fehl, ohne andere Medientypen auszuprobieren.

Wenn der Medientyp akzeptabel ist, ruft diese Methode die [**IPin::ReceiveConnection-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) des empfangenden Pins auf. Anschließend wird die [**CBasePin::CompleteConnect-Methode**](cbasepin-completeconnect.md) zum Abschließen der Verbindung aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




