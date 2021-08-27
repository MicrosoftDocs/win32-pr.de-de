---
description: Die IsPageDirty-Methode gibt an, ob sich die Eigenschaftenseite seit der Aktivierung oder seit dem letzten Aufruf von IPropertyPage::Apply geändert hat. Diese Methode implementiert die IPropertyPage::IsPageDirty-Methode.
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: CBasePropertyPage.IsPageDirty-Methode (Cprop.h)
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
ms.openlocfilehash: 72b818ce117990f6f91ee58b8605e9d8cff9734fa9114d7f6114ed11d53a9521
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108500"
---
# <a name="cbasepropertypageispagedirty-method"></a>CBasePropertyPage.IsPageDirty-Methode

Die `IsPageDirty` -Methode gibt an, ob sich die Eigenschaftenseite seit der Aktivierung oder seit dem letzten Aufruf von **IPropertyPage::Apply** geändert hat. Diese Methode implementiert die **IPropertyPage::IsPageDirty-Methode.**

## <a name="syntax"></a>Syntax


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn [**CBasePropertyPage::m \_ bDirty**](cbasepropertypage-m-bdirty.md) **TRUE** ist, \_ andernfalls S FALSE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePropertyPage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




