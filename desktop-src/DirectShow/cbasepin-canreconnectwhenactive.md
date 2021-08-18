---
description: Die CanReconnectWhenActive-Methode fragt ab, ob der Pin dynamische wiederhergestellte Verbindungen unterstützt.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: CBasePin.CanReconnectWhenActive-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CanReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffe4cc09efa53ac4d3ab8089a1061d860206f9734c214d250b5c3cdc907eaf84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916920"
---
# <a name="cbasepincanreconnectwhenactive-method"></a>CBasePin.CanReconnectWhenActive-Methode

Die `CanReconnectWhenActive` -Methode fragt ab, ob der Pin dynamische wiederhergestellte Verbindung unterstützt.

## <a name="syntax"></a>Syntax


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob die Verbindung mit dem Pin dynamisch wiederhergestellt werden kann. True **gibt an,** dass der Pin die Verbindung dynamisch wiederherstellen kann.

## <a name="remarks"></a>Hinweise

Standardmäßig müssen Sie einen Filter beenden, bevor Sie einen seiner Stecknadeln erneut verbinden. Wenn ein Pin die dynamische wiederhergestellte Verbindung unterstützt, kann die Verbindung jedoch wiederhergestellt werden, während der Filter aktiv ist. Weitere Informationen finden Sie unter [Dynamic Graph Building](dynamic-graph-building.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




