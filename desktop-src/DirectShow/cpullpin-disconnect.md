---
description: Die Disconnect-Methode unterbricht die Verbindung mit der Ausgabepin.
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: Cpullpin. Disconnect-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec13a7f29a06bab4f79ddb58932796f8363adadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362046"
---
# <a name="cpullpindisconnect-method"></a>Cpullpin. Disconnect-Methode

Die- `Disconnect` Methode unterbricht die Verbindung mit der Ausgabepin.

## <a name="syntax"></a>Syntax


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode unterbricht jede in der [**cpullpin:: Connect**](cpullpin-connect.md) -Methode hergestellte Verbindung. Nennen Sie diese Methode in Ihrer [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) -Methode. (Wenn Ihre PIN von [**cbasepin**](cbasepin.md)abgeleitet ist, überschreiben Sie [**cbasepin:: breakconnect**](cbasepin-breakconnect.md) , um diese Methode aufzurufen.)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpullpin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




