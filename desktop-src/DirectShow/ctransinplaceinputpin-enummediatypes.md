---
description: 'Die enummediatypes-Methode listet die bevorzugten Medientypen der PIN auf. Diese Methode implementiert die IPin:: enummediatypes-Methode.'
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: Ctransinplaceinputpin. enummediatypes-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa634fa695eb0007b49fc1c36c730c7fbde361b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365984"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a>Ctransinplaceinputpin. enummediatypes-Methode

Die `EnumMediaTypes` -Methode listet die bevorzugten Medientypen der PIN auf. Diese Methode implementiert die [**IPin:: enummediatypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppEnum* 
</dt> <dd>

Empfängt einen Zeiger auf die [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                           | Beschreibung                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                         |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>         | Nicht genügend Arbeitsspeicher.<br/>             |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>             | **Null** -Zeiger.<br/>                |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Die Ausgabe-PIN ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt die **ienummediatypes** -Schnittstelle von der Downstream-Eingabe-PIN zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplaceinputpin-Klasse**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




