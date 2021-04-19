---
description: Wertet einen Ausdruck aus und verursacht eine breakpointausnahme, wenn der Ausdruck false ist. Der Text des Ausdrucks, der Name der Quelldatei und die Zeilennummer werden mithilfe des dbglog-Makros protokolliert. Wird in Einzelhandels Builds ignoriert.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: Kassert-Makro (wxdebug. h)
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
ms.openlocfilehash: f797e60a6175a86f2c1c9d675e9607a48a58c14a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362159"
---
# <a name="kassert-macro"></a>Kassert-Makro

Wertet einen Ausdruck aus und verursacht eine breakpointausnahme, wenn der Ausdruck **false** ist. Der Text des Ausdrucks, der Name der Quelldatei und die Zeilennummer werden mithilfe des [**dbglog**](dbglog.md) -Makros protokolliert. Wird in Einzelhandels Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void KASSERT(
    cond
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cond* 
</dt> <dd>

Der auszuwertende Ausdruck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Im Gegensatz zu den Makros [**Assert**](assert.md) und [**Execute \_ Assert**](execute-assert.md) zeigt dieses Makro kein Meldungs Feld an, in dem der Benutzer dazu aufgefordert wird. Wenn in Debugbuilds der Ausdruck **false** lautet, bewirkt das Makro automatisch, dass eine breakpointausnahme auftritt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Assert-und breakpointmakros](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




