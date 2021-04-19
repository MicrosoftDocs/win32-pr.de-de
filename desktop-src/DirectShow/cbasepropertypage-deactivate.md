---
description: Die Methode zum Deaktivieren zerstört das Dialogfenster. Diese Methode implementiert die IPropertyPage::D eaktivierungs-Methode.
ms.assetid: f2d2f15f-15f6-4902-bafc-f58a684ff193
title: Cbasepropertypage. deaktiviert-Methode (cprop. h)
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
ms.openlocfilehash: 63a843502fc735cc41ff3656e83ef3d6cb839a19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369116"
---
# <a name="cbasepropertypagedeactivate-method"></a>Cbasepropertypage. deaktivieren-Methode

Mit der- `Deactivate` Methode wird das Dialogfeld zerstört. Diese Methode implementiert die **IPropertyPage::D eaktivierungs** -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Deactivate();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>            |
| <dl> <dt>**E \_ unerwartet**</dt> </dl> | Unerwarteter Fehler.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> <dt>

[**Cbasepropertypage:: ondeaktivieren**](cbasepropertypage-ondeactivate.md)
</dt> </dl>

 

 




