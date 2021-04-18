---
description: Die cancelnotification-Methode bricht das Timer-Ereignis ab, das das Rendering plant.
ms.assetid: 56ddf692-a2e3-40f2-848f-2d592601ec00
title: Cbaserderderer. cancelnotification-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CancelNotification
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3330f369c5fcc45fe051a1964a504d5d40fcd091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361313"
---
# <a name="cbaserenderercancelnotification-method"></a>Cbaserderderer. cancelnotification-Methode

Die- `CancelNotification` Methode bricht das Timer-Ereignis ab, das das Rendering plant.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CancelNotification();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                             | Beschreibung                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Es war kein ausstehendes Timer-Ereignis vorhanden.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

Der Filter ruft diese Methode auf, wenn das Streaming beendet wird. Die-Methode bricht alle geplanten Renderingvorgänge ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




