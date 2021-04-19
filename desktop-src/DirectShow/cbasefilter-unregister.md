---
description: Mit der Unregister-Methode wird der Filter aus der Registrierung entfernt.
ms.assetid: 2eb70e9f-1acf-433e-972f-24fb32eaeb13
title: Cbasefilter. Unregister-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Unregister
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8b46e74e4009f6767788fa120984eca0e89fb551
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370042"
---
# <a name="cbasefilterunregister-method"></a>Cbasefilter. Unregister-Methode

Die- `Unregister` Methode entfernt den Filter aus der Registrierung.

> [!Note]  
> Diese Methode ist veraltet. Die Registrierung neuer Filter sollte mithilfe der [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) -Funktion aufgehoben werden. Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md).

 

## <a name="syntax"></a>Syntax


```C++
HRESULT Unregister();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




