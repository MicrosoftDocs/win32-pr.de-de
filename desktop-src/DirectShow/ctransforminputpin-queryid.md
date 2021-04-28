---
description: 'CTransformInputPin.QueryId-Methode: Die QueryId-Methode ruft einen Bezeichner für den Pin ab. Diese Methode implementiert die IPin::QueryId-Methode.'
ms.assetid: 91fde383-0288-4307-9ca8-e117b6111769
title: CTransformInputPin.QueryId-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8407e649814fcb12f699c2362f0f89137e941d19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095008"
---
# <a name="ctransforminputpinqueryid-method"></a>CTransformInputPin.QueryId-Methode

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



 

## <a name="remarks"></a>Bemerkungen

Der Stecknadelbezeichner wird für die Graphpersistenz verwendet. Der Stecknadelbezeichner für diese Klasse ist In. Diese Klasse überschreibt das Verhalten der [**CBasePin-Klasse.**](cbasepin.md) In der **CBasePin-Klasse** entspricht der Pinbezeichner dem Pinnamen, der im Klassenkonstruktor angegeben ist. In der **CTransformInputPin-Klasse** sind der Pinbezeichner und der Pinname nicht identisch.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




