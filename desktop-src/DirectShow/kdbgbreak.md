---
description: Verursacht eine Breakpointausnahme und protokolliert die angegebene Zeichenfolge mithilfe des DbgLog-Makros. Wird in Einzelhandels-Builds ignoriert.
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: KDbgBreak-Makro (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KDbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 3339e69bb10876fe326f5960e6012849664fdbfcb4fe06fffd4029e6170af8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952359"
---
# <a name="kdbgbreak-macro"></a>KDbgBreak-Makro

Verursacht eine Breakpointausnahme und protokolliert die angegebene Zeichenfolge mithilfe des [**DbgLog-Makros.**](dbglog.md) Wird in Einzelhandels-Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void KDbgBreak(
    strLiteral
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strLiteral* 
</dt> <dd>

Textzeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Im Gegensatz [**zum DbgBreak-Makro**](dbgbreak.md) zeigt dieses Makro kein Meldungsfeld an, in dem der Benutzer dazu aufgefordert wird. In Debugbuilds wird automatisch eine Breakpointausnahme ausgelöst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Assert- und Breakpoint-Makros](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




