---
description: Die Disconnect-Methode unterbricht die Verbindung mit dem Ausgabepin.
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: CPullPin.Disconnect-Methode (Pullpin.h)
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
ms.openlocfilehash: 0491bfba7e5b739a2b46674cc2f6506017810d4f1e51693d4478720c67a4a4da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055070"
---
# <a name="cpullpindisconnect-method"></a>CPullPin.Disconnect-Methode

Die `Disconnect` -Methode unterbricht die Verbindung mit dem Ausgabepin.

## <a name="syntax"></a>Syntax


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode unterbricht alle Verbindungen, die in der [**CPullPin::Verbinden-Methode**](cpullpin-connect.md) hergestellt wurden. Rufen Sie diese Methode in Ihrer [**IPin::D isconnect-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) auf. (Wenn Ihre Stecknadel von [**CBasePin**](cbasepin.md)abgeleitet ist, überschreiben Sie [**CBasePin::BreakConnect,**](cbasepin-breakconnect.md) um diese Methode aufzurufen.)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPullPin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




