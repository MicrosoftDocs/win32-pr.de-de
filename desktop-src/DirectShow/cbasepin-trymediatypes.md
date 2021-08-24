---
description: Bei einer Liste von Medientypen versucht die TryMediaTypes-Methode, eine Verbindung mit einem dieser Typen herzustellen.
ms.assetid: cc437e44-bc59-494e-8669-7f539353a794
title: CBasePin.TryMediaTypes-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.TryMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a4d4e33ca339c1ade344bb2ca9531bea381d14b4381773673b07e522437e90a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108620"
---
# <a name="cbasepintrymediatypes-method"></a>CBasePin.TryMediaTypes-Methode

Bei einer Liste von Medientypen versucht die `TryMediaTypes` -Methode, eine Verbindung mit einem dieser Typen herzustellen.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT TryMediaTypes(
         IPin            *pReceivePin,
   const CMediaType      *pmt,
         IEnumMediaTypes *pEnum
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

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das die möglichen Medientypen einschränkt, oder **NULL**.

</dd> <dt>

*pEnum* 
</dt> <dd>

Zeiger auf eine [**IEnumMediaTypes-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) die zum Auflisten der Liste der Medientypen verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die werte in der folgenden Tabelle.



| Rückgabecode                                                                                                  | Beschreibung                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>                               |
| <dl> <dt>**VFW \_ E \_ KEINE \_ \_ AKZEPTABLEN TYPEN**</dt> </dl> | Es wurde kein zulässiger Medientyp gefunden.<br/> |



 

## <a name="remarks"></a>Hinweise

Für jeden Medientyp, der von der **IEnumMediaTypes-Schnittstelle** zurückgegeben wird, versucht diese Methode eine Verbindung, indem sie die [**CBasePin::AttemptConnection-Methode**](cbasepin-attemptconnection.md) aufruft.

Wenn der *pmt-Parameter* ungleich **NULL** ist, überspringt der Pin Medientypen, die nicht mit diesem Typ übereinstimmen. Der *pmt-Parameter* kann einen partiellen Medientyp angeben. Ein partieller Medientyp hat den Wert GUID \_ NULL für den Haupttyp, den Untertyp oder das Format. Der GUID \_ NULL-Wert entspricht einem beliebigen Typ, ähnlich einem Platzhalterwert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




