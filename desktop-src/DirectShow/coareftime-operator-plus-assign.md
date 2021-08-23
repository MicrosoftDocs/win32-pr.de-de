---
description: Dieser Operator fügt zwei Verweiszeiten hinzu und legt dieses Objekt auf das Ergebnis fest.
ms.assetid: 6d29014b-0e31-497e-8326-e3fefc022227
title: COARefTime.operator+=-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dcb635e3026cec18aa5bea199b6712c15c6472d81e9b6707267d15d7afcfa6ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585560"
---
# <a name="coareftimeoperator-method"></a>COARefTime.operator+=-Methode

Dieser Operator fügt zwei Verweiszeiten hinzu und legt dieses Objekt auf das Ergebnis fest.

## <a name="syntax"></a>Syntax


```C++
COARefTime& operator+=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Verweis auf das **hinzuzufügende COARefTime-Objekt.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Verweis auf das -Objekt zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COARefTime-Klasse**](coareftime.md)
</dt> </dl>

 

 




