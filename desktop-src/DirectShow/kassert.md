---
description: Wertet einen Ausdruck aus und löst eine Breakpointausnahme aus, wenn der Ausdruck FALSE ist. Der Text des Ausdrucks, der Name der Quelldatei und die Zeilennummer werden mit dem DbgLog-Makro protokolliert. Wird in Einzelhandelsbuilds ignoriert.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: KASSERT-Makro (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: a1eb6738ea3e9d4535bf9f8291dc71349d67bb51d143b6bc73e83290f36657cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817057"
---
# <a name="kassert-macro"></a>KASSERT-Makro

Wertet einen Ausdruck aus und löst eine Breakpointausnahme aus, wenn der Ausdruck **FALSE** ist. Der Text des Ausdrucks, der Name der Quelldatei und die Zeilennummer werden mit dem [**DbgLog-Makro**](dbglog.md) protokolliert. Wird in Einzelhandelsbuilds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void KASSERT(
    cond
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cond* 
</dt> <dd>

Der auszuwertende Ausdruck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Im Gegensatz zu den [**Assert-**](assert.md) und [**EXECUTE \_ ASSERT-Makros**](execute-assert.md) zeigt dieses Makro kein Meldungsfeld an, in dem der Benutzer dazu aufgefordert wird. Wenn der Ausdruck in Debugbuilds **FALSE** ist, löst das Makro automatisch eine Breakpointausnahme aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Assert- und Breakpoint-Makros](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




