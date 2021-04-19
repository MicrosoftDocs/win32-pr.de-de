---
description: Gibt false zurück, wenn der aktuelle Thread der Besitzer des angegebenen kritischen Abschnitts ist.
ms.assetid: 1a2cb56c-2806-4bb2-b904-985af332b290
title: Critcheckout-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckOut
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae5a888e619f6bed9cda203ccd8a197b0b25c001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352947"
---
# <a name="critcheckout-function"></a>Critcheckout-Funktion

Gibt **false** zurück, wenn der aktuelle Thread der Besitzer des angegebenen kritischen Abschnitts ist.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CritCheckOut(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pccrit* 
</dt> <dd>

Zeiger auf einen kritischen [**ccritsec**](ccritsec.md) -Abschnitt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

In Debugbuilds gibt **false** zurück, wenn der aktuelle Thread der Besitzer dieses kritischen Abschnitts ist, andernfalls **true** . In Einzelhandels Builds gibt immer **true** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist die Umkehrung der [**critcheckin**](critcheckin.md) -Funktion. Wenn **critcheckin** **true** zurückgibt, gibt **critcheckout** **false** zurück und umgekehrt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kritische Abschnitts Debuggingfunktionen](critical-section-debugging-functions.md)
</dt> </dl>

 

 




