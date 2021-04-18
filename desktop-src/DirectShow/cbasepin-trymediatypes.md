---
description: Bei einer Liste von Medientypen wird von der trymediatypes-Methode versucht, eine Verbindung mit einem dieser Typen abzuschließen.
ms.assetid: cc437e44-bc59-494e-8669-7f539353a794
title: Cbasepin. trymediatypes-Methode (amfilter. h)
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
ms.openlocfilehash: 19b8da39d07b8aae9401bdc6ccf2eecb5d3a1e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351294"
---
# <a name="cbasepintrymediatypes-method"></a>Cbasepin. trymediatypes-Methode

Bei einer Liste von Medientypen versucht die- `TryMediaTypes` Methode, eine Verbindung mit einem dieser Typen abzuschließen.

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

*preceivepin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der empfangenden PIN.

</dd> <dt>

*PMT* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das die möglichen Medientypen einschränkt, oder **null**.

</dd> <dt>

*"-ID"* 
</dt> <dd>

Zeiger auf eine [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle, die verwendet wird, um die Liste der Medientypen aufzuzählen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                                  | Beschreibung                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>                               |
| <dl> <dt>**VFW \_ E \_ keine \_ akzeptablen \_ Typen**</dt> </dl> | Es wurde kein akzeptabler Medientyp gefunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Für jeden Medientyp, der von der **ienummediatypes** -Schnittstelle zurückgegeben wird, versucht diese Methode, eine Verbindung durch Aufrufen der [**cbasepin::-Verbindungs**](cbasepin-attemptconnection.md) Methode herzustellen.

Wenn der *PMT* -Parameter nicht **null** ist, überspringt die PIN Medientypen, die nicht diesem Typ entsprechen. Der *PMT* -Parameter kann einen partiellen Medientyp angeben. Ein partieller Medientyp weist den Wert GUID \_ NULL für den Haupttyp, den Untertyp oder das Format auf. Der GUID- \_ NULL-Wert stimmt mit einem beliebigen Typ überein, ähnlich dem Wert "Platzhalter".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




