---
description: Die OnDeactivate-Methode wird aufgerufen, wenn das Dialogfeldfenster zerstört wird.
ms.assetid: 47320e61-324f-4f64-abe1-38fe70e82787
title: CBasePropertyPage.OnDeactivate-Methode (Cprop.h)
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
ms.openlocfilehash: a2091cc1c4708f82ae6923499e1ecc0f0e9aaf28c181d7164ff73720cd7f4d45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000832"
---
# <a name="cbasepropertypageondeactivate-method"></a>CBasePropertyPage.OnDeactivate-Methode

Die `OnDeactivate` -Methode wird aufgerufen, wenn das Dialogfeldfenster zerstört wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnDeactivate();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Basisklassenimplementierung gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Die [**CBasePropertyPage::D eactivate-Methode**](cbasepropertypage-deactivate.md) ruft die `OnDeactivate` -Methode auf. Überschreiben Sie , um alle Ressourcen frei zu geben, die die abgeleitete Klasse in der `OnDeactivate` [**CBasePropertyPage::OnActivate-Methode**](cbasepropertypage-onactivate.md) erhalten hat, oder um bei Bedarf andere Aufgaben auszuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePropertyPage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




