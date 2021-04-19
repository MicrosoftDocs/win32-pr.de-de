---
description: Verursacht eine breakpointausnahme und protokolliert die angegebene Zeichenfolge mit dem dbglog-Makro. Wird in Einzelhandels Builds ignoriert.
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: Kdbgbreak-Makro (wxdebug. h)
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
ms.openlocfilehash: 9631dc8d956652137810b25ae5923cc1c6927bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357531"
---
# <a name="kdbgbreak-macro"></a>Kdbgbreak-Makro

Verursacht eine breakpointausnahme und protokolliert die angegebene Zeichenfolge mit dem [**dbglog**](dbglog.md) -Makro. Wird in Einzelhandels Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void KDbgBreak(
    strLiteral
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*"Straume"* 
</dt> <dd>

Text Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Im Gegensatz zum [**dbgbreak**](dbgbreak.md) -Makro zeigt dieses Makro kein Meldungs Feld an, in dem der Benutzer dazu aufgefordert wird. In Debugbuilds bewirkt dies automatisch, dass eine breakpointausnahme auftritt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Assert-und breakpointmakros](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




