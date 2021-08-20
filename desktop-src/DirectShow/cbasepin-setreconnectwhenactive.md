---
description: Die SetReconnectWhenActive-Methode gibt an, ob der Pin dynamische Erneute Verbindungen unterstützt.
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: CBasePin.SetReconnectWhenActive-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf90c32af8371d9f2dd61369e21dfeb0726c7fa044758a3d8fb9beee7fd5743e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000842"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a>CBasePin.SetReconnectWhenActive-Methode

Die `SetReconnectWhenActive` -Methode gibt an, ob der Pin dynamische Verbindungswiederherstellungen unterstützt.

## <a name="syntax"></a>Syntax


```C++
void SetReconnectWhenActive(
   bool bCanReconnect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bCanReconnect* 
</dt> <dd>

Ein boolescher Wert, der angibt, ob die Pin dynamisch erneut eine Verbindung herstellen kann. True gibt an, dass die Stecknadel die Verbindung dynamisch wiederherstellen kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Standardmäßig müssen Sie einen Filter beenden, bevor Sie die Verbindung mit einem seiner Pins wiederherstellen. Wenn die Stecknadel die Verbindung wiederherstellen kann, während der Filter aktiv ist, rufen Sie diese Methode mit dem Wert **TRUE** auf. Weitere Informationen finden Sie unter [Dynamic Graph Building](dynamic-graph-building.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




