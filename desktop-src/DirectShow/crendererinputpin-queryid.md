---
description: Die QueryId-Methode ruft den Pinbezeichner ab. Diese Methode überschreibt die CBasePin::QueryId-Methode.
ms.assetid: 9543234c-5349-49d0-b410-1c461ee4eabe
title: CRendererInputPin.QueryId-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 732bf7aa6d0d247c93c0334db48b86bccd2ac15715dd2da9a4d60a0d315966bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054572"
---
# <a name="crendererinputpinqueryid-method"></a>CRendererInputPin.QueryId-Methode

Die `QueryId` -Methode ruft den Pinbezeichner ab. Diese Methode überschreibt die [**CBasePin::QueryId-Methode.**](cbasepin-queryid.md)

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

Empfängt eine Zeichenfolge, die den Pinbezeichner enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                   | Beschreibung                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher<br/>       |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | **NULL-Zeigerargument**<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode weist die Breitzeichenzeichenfolge "In" zu und weist sie dem *Id-Parameter* zu. Der Aufrufer muss den zugeordneten Arbeitsspeicher mithilfe der **CoTaskMemFree-Funktion frei** geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CRendererInputPin-Klasse**](crendererinputpin.md)
</dt> </dl>

 

 




