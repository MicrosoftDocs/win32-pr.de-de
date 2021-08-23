---
description: Die AlignDown-Methode schneidet einen Wert auf eine angegebene Ausrichtungsgrenze ab.
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: CPullPin.AlignDown-Methode (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignDown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cdf16f3759bb7637fa243ce98bc4886b65e31d25bf62f5e9f581064d3741ea1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585350"
---
# <a name="cpullpinaligndown-method"></a>CPullPin.AlignDown-Methode

Die `AlignDown` -Methode schneidet einen Wert auf eine angegebene Ausrichtungsgrenze ab.

## <a name="syntax"></a>Syntax


```C++
LONGLONG AlignDown(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ll* 
</dt> <dd>

Gibt die Zahl an, die ausgerichtet werden soll.

</dd> <dt>

*lAlign* 
</dt> <dd>

Gibt die Ausrichtungsgrenze an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das ausgerichtete Ergebnis zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPullPin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




