---
description: Die Deactivate-Methode zerstört das Dialogfeldfenster. Diese Methode implementiert die IPropertyPage::D eactivate-Methode.
ms.assetid: f2d2f15f-15f6-4902-bafc-f58a684ff193
title: CBasePropertyPage.Deactivate-Methode (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Deactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5acb906a28087464f349aff3fdcdf367d7e3bceaa5a29cfa1cad4143b80e10c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526770"
---
# <a name="cbasepropertypagedeactivate-method"></a>CBasePropertyPage.Deactivate-Methode

Die `Deactivate` -Methode zerstört das Dialogfeldfenster. Diese Methode implementiert die **IPropertyPage::D eactivate-Methode.**

## <a name="syntax"></a>Syntax


```C++
HRESULT Deactivate();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>            |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Unerwarteter Fehler.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePropertyPage-Klasse**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage::OnDeactivate**](cbasepropertypage-ondeactivate.md)
</dt> </dl>

 

 




