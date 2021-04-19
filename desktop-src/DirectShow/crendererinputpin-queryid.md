---
description: 'Die QueryId-Methode ruft den PIN-Bezeichner ab. Diese Methode überschreibt die cbasepin:: QueryId-Methode.'
ms.assetid: 9543234c-5349-49d0-b410-1c461ee4eabe
title: Crendererinputpin. QueryId-Methode (renbase. h)
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
ms.openlocfilehash: b56ae2a846b4d89da4c6a9d4c8f88bd3094c5cff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362143"
---
# <a name="crendererinputpinqueryid-method"></a>Crendererinputpin. QueryId-Methode

Die- `QueryId` Methode ruft den PIN-Bezeichner ab. Diese Methode überschreibt die [**cbasepin:: QueryId**](cbasepin-queryid.md) -Methode.

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

Empfängt eine Zeichenfolge mit dem PIN-Bezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                   | Beschreibung                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg<br/>                   |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher<br/>       |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | **Null** -Zeigerargument<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ordnet die breit Zeichen-Zeichenfolge "in" zu und weist Sie dem *ID* -Parameter zu. Der Aufrufer muss den zugewiesenen Speicher mithilfe der **CoTaskMemFree** -Funktion freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Crendererinputpin-Klasse**](crendererinputpin.md)
</dt> </dl>

 

 




