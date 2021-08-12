---
description: Legt den Debugtime out-Wert fest. Wird in Einzelhandelsbuilds ignoriert.
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: DbgSetWaitTimeout-Funktion (Wxdebug.h)
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
ms.openlocfilehash: 67a5522184b9e88cd4b8ac9f23246f96c13ffad2175d625334de32d34c750e12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654022"
---
# <a name="dbgsetwaittimeout-function"></a>DbgSetWaitTimeout-Funktion

Legt den Debugtime out-Wert fest. Wird in Einzelhandelsbuilds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DbgSetWaitTimeout(
   DWORD dwTimeout
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwTimeout* 
</dt> <dd>

Time out-Wert in Millisekunden oder INFINITE, um unbegrenzt zu warten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

In Debugbuilds verwenden die Funktionen [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) und [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) diesen Wert als Time out-Intervall.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Wartedebuggen von Funktionen](wait-debugging-functions.md)
</dt> </dl>

 

 




