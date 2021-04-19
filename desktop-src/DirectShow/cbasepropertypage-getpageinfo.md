---
description: 'Die GetPageInfo-Methode ruft Informationen zur Eigenschaften Seite ab. Diese Methode implementiert die IPropertyPage:: getpagumfo-Methode.'
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: Cbasepropertypage. getpagumfo-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.GetPageInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27faecf50381b098dfcbee34d1494e37c77a36ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369173"
---
# <a name="cbasepropertypagegetpageinfo-method"></a>Cbasepropertypage. getpagumfo-Methode

Die- `GetPageInfo` Methode ruft Informationen zur Eigenschaften Seite ab. Diese Methode implementiert die **IPropertyPage:: getpagumfo** -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPageInfo(
   LPPROPPAGEINFO pPageInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPageInfo* 
</dt> <dd>

Zeiger auf eine vom Aufrufer zugewiesene **PROPPAGEINFO** -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                   | Beschreibung                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>             |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




