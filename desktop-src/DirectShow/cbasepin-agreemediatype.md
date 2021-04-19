---
description: Die agreemediatype-Methode sucht nach einem Medientyp, um eine PIN-Verbindung herzustellen.
ms.assetid: 545186d2-b5e8-4833-b0ff-11160c1dd53b
title: Cbasepin. agreemediatype-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AgreeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e5cdea12cb8bca3319f908fe697251a3d4699d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370329"
---
# <a name="cbasepinagreemediatype-method"></a>Cbasepin. agreemediatype-Methode

Die- `AgreeMediaType` Methode sucht nach einem Medientyp, um eine PIN-Verbindung herzustellen.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT AgreeMediaType(
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

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das einen Medientyp angibt, oder **null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                                  | Beschreibung                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>                            |
| <dl> <dt>**VFW \_ E \_ keine \_ akzeptablen \_ Typen**</dt> </dl> | Es wurde kein zulässiger Medientyp gefunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn der *PMT* -Parameter nicht **null** ist und einen Medientyp vollständig angibt, versucht diese Methode, mithilfe dieses Medientyps eine Verbindung herzustellen. Wenn der Versuch fehlschlägt, gibt die Methode einen Fehler zurück.

Wenn der *PMT* -Parameter **null** ist oder einen partiellen Medientyp angibt, versucht diese Methode Medientypen in der folgenden Reihenfolge:

1.  Die bevorzugten Medientypen der empfangenden PIN.
2.  Die bevorzugten Medientypen dieser Pin.

Bevorzugte Medientypen werden mit der [**cbasepin:: enummediatypes**](cbasepin-enummediatypes.md) -Methode aufgezählt, und der resultierende Enumerator wird an die [**cbasepin:: trymediatypes**](cbasepin-trymediatypes.md) -Methode übergeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




