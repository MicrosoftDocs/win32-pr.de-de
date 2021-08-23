---
description: 'CTransformOutputPin.QueryId-Methode: Die QueryId-Methode ruft einen Bezeichner für den Pin ab. Diese Methode implementiert die IPin::QueryId-Methode.'
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: CTransformOutputPin.QueryId-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56da848f3829f56d93d7d0383dc7fdc1ec6d5bfd995c2c74507d05eb13801fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584810"
---
# <a name="ctransformoutputpinqueryid-method"></a>CTransformOutputPin.QueryId-Methode

Die `QueryId` -Methode ruft einen Bezeichner für den Pin ab. Diese Methode implementiert die [**IPin::QueryId-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Id* 
</dt> <dd>

Empfängt eine Zeichenfolge, die den Stecknadelbezeichner enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                   | Beschreibung                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher<br/>       |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | **NULL-Zeigerargument**<br/> |



 

## <a name="remarks"></a>Hinweise

Der Stecknadelbezeichner wird für die Graphpersistenz verwendet. Der Stecknadelbezeichner für diese Klasse ist Out. Diese Klasse überschreibt das Verhalten der [**CBasePin-Klasse.**](cbasepin.md) In der **CBasePin-Klasse** entspricht der Pinbezeichner dem Pinnamen, der im Klassenkonstruktor angegeben ist. In der **CTransformInputPin-Klasse** sind der Pinbezeichner und der Pinname nicht identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




