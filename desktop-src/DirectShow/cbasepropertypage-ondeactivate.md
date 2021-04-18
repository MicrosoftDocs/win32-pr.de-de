---
description: Die ondeaktivieren-Methode wird aufgerufen, wenn das Dialogfeld Fenster zerstört wird.
ms.assetid: 47320e61-324f-4f64-abe1-38fe70e82787
title: Cbasepropertypage. ondeaktiviert-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDeactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27191e4895c911d3d13a795306eee2b0ad6989ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354811"
---
# <a name="cbasepropertypageondeactivate-method"></a>Cbasepropertypage. ondeaktivieren-Methode

Die- `OnDeactivate` Methode wird aufgerufen, wenn das Dialogfeld Fenster zerstört wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnDeactivate();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Basisklassen Implementierung gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die [**cbasepropertypage::D eaktivierungs**](cbasepropertypage-deactivate.md) -Methode ruft die- `OnDeactivate` Methode auf. `OnDeactivate`Überschreiben Sie, um alle Ressourcen freizugeben, die von der abgeleiteten Klasse in der [**cbasepropertypage:: onaktivierungs**](cbasepropertypage-onactivate.md) -Methode abgerufen wurden, oder, um andere Aufgaben nach Bedarf auszuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




