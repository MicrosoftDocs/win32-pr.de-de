---
description: 'Die ispagedirty-Methode gibt an, ob die Eigenschaften Seite seit der Aktivierung oder seit dem letzten Aufrufen von IPropertyPage:: apply geändert wurde. Diese Methode implementiert die IPropertyPage:: ispagedirty-Methode.'
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: Cbasepropertypage. ispagedirty-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.IsPageDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c69c2e7d480f63542e146c73e56b9e692693f665
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371443"
---
# <a name="cbasepropertypageispagedirty-method"></a>Cbasepropertypage. ispagedirty-Methode

Die- `IsPageDirty` Methode gibt an, ob die Eigenschaften Seite seit der Aktivierung oder seit dem letzten Aufrufen von **IPropertyPage:: apply** geändert wurde. Diese Methode implementiert die **IPropertyPage:: ispagedirty** -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt "s OK" zurück \_ , wenn " [**cbasepropertypage:: m \_ bdirty**](cbasepropertypage-m-bdirty.md) " den Wert **true** hat, \_ andernfalls "false".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




