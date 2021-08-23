---
description: Die Unregister-Methode entfernt den Filter aus der Registrierung.
ms.assetid: 2eb70e9f-1acf-433e-972f-24fb32eaeb13
title: CBaseFilter.Unregister-Methode (Amfilter.h)
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
ms.openlocfilehash: c57d08c77c9c420cdc45b158a19fa610231f53f6b409d8b650953de0de8381a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317900"
---
# <a name="cbasefilterunregister-method"></a>CBaseFilter.Unregister-Methode

Die `Unregister` -Methode entfernt den Filter aus der Registrierung.

> [!Note]  
> Diese Methode ist veraltet. Die Registrierung neuer Filter sollte mithilfe der [**Funktion AMovieDllRegisterServer2**](amoviedllregisterserver2.md) aufgehoben werden. Weitere Informationen finden Sie unter [Registrieren von DirectShow-Filtern.](how-to-register-directshow-filters.md)

 

## <a name="syntax"></a>Syntax


```C++
HRESULT Unregister();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK oder einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




