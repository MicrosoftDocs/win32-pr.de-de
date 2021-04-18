---
description: Legt den Timeout Wert für das Debuggen fest. Wird in Einzelhandels Builds ignoriert.
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: Dbgsetwaittimeout-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetWaitTimeout
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5805112b19132045e0245ef7baf29cb5c844e290
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359307"
---
# <a name="dbgsetwaittimeout-function"></a>Dbgsetwaittimeout-Funktion

Legt den Timeout Wert für das Debuggen fest. Wird in Einzelhandels Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DbgSetWaitTimeout(
   DWORD dwTimeout
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwtimeout* 
</dt> <dd>

Timeout Wert in Millisekunden oder unendlich, wenn unbegrenzt gewartet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

In Debugbuilds verwenden die Funktionen [**dbgwaitformultipleobjects**](dbgwaitformultipleobjects.md) und [**dbgwaitforsingleobject**](dbgwaitforsingleobject.md) diesen Wert als Timeout Intervall.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Wait-Debugging-Funktionen](wait-debugging-functions.md)
</dt> </dl>

 

 




