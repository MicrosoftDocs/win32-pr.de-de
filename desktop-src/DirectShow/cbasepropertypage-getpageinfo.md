---
description: Die GetPageInfo-Methode ruft Informationen zur Eigenschaftenseite ab. Diese Methode implementiert die IPropertyPage::GetPageInfo-Methode.
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: CBasePropertyPage.GetPageInfo-Methode (Cprop.h)
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
ms.openlocfilehash: badb0678faa85b70dfa848bba7538319b905feea440339e24285f3d64b59d61c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823160"
---
# <a name="cbasepropertypagegetpageinfo-method"></a>CBasePropertyPage.GetPageInfo-Methode

Die `GetPageInfo` -Methode ruft Informationen über die Eigenschaftenseite ab. Diese Methode implementiert die **IPropertyPage::GetPageInfo-Methode.**

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

Zeiger auf eine vom Aufrufer zugeordnete **PROPPAGEINFO-Struktur.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                   | Beschreibung                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePropertyPage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




