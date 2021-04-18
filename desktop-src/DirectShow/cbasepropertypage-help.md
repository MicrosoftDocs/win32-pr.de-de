---
description: 'Die Hilfe Methode ruft die Hilfe der Eigenschaften Seite auf. Diese Methode implementiert die IPropertyPage:: Help-Methode.'
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: Cbasepropertypage. Help-Methode (cprop. h)
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
ms.openlocfilehash: b87c8ba76928fbf0e465a8b6a3a0aaf4730759f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360944"
---
# <a name="cbasepropertypagehelp-method"></a>Cbasepropertypage. Help-Methode

Die- `Help` Methode ruft die Hilfe der Eigenschaften Seite auf. Diese Methode implementiert die **IPropertyPage:: Help** -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Help(
   LPCWSTR lpszHelpDir
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszhelpdir* 
</dt> <dd>

Zeiger auf die Zeichenfolge unter dem **helpDir** -Schlüssel in den CLSID-Informationen der Eigenschaften Seite in der Registrierung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "E \_ notimpl" zurück.

## <a name="remarks"></a>Bemerkungen

In der-Basisklasse gibt die-Methode immer E \_ notimpl zurück. Wenn die Methode fehlschlägt, ruft der Frame **IPropertyPage:: GetPageInfo** auf, um den Namen der Hilfedatei und des Kontext Bezeichners zu erhalten. Standardmäßig sind diese **null**-Werte. Um Hilfe bereitzustellen, kann die abgeleitete Klasse entweder die- `Help` Methode oder die [**cbasepropertypage:: getpagumfo**](cbasepropertypage-getpageinfo.md) -Methode überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




