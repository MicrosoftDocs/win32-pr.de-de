---
description: Die Help-Methode ruft die Hilfe zur Eigenschaftenseite auf. Diese Methode implementiert die IPropertyPage::Help-Methode.
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: CBasePropertyPage.Help-Methode (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Help
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e2f97f7edd1e719eb44ff1d41929d7cb3864d8117eabb383b4318688adfa537f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955089"
---
# <a name="cbasepropertypagehelp-method"></a>CBasePropertyPage.Help-Methode

Die `Help` -Methode ruft die Hilfe zur Eigenschaftenseite auf. Diese Methode implementiert die **IPropertyPage::Help-Methode.**

## <a name="syntax"></a>Syntax


```C++
HRESULT Help(
   LPCWSTR lpszHelpDir
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszHelpDir* 
</dt> <dd>

Zeiger auf die Zeichenfolge unter dem **HelpDir-Schlüssel** in den CLSID-Informationen der Eigenschaftenseite in der Registrierung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ NOTIMPL zurück.

## <a name="remarks"></a>Hinweise

In der Basisklasse gibt die Methode immer E \_ NOTIMPL zurück. Wenn die Methode fehlschlägt, ruft der Frame **IPropertyPage::GetPageInfo** auf, um den Namen der Hilfedatei und den Kontextbezeichner abzurufen. Standardmäßig sind dies **NULL.** Um Hilfe bereitzustellen, kann die abgeleitete Klasse daher entweder die `Help` -Methode oder die [**CBasePropertyPage::GetPageInfo-Methode**](cbasepropertypage-getpageinfo.md) überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePropertyPage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




