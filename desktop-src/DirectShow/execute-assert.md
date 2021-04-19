---
description: Wertet einen Ausdruck in Debug-und Retail-Builds aus. In Debugbuilds zeigt eine Diagnose Meldung an, wenn der Ausdruck false ist.
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: EXECUTE_ASSERT-Makro (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXECUTE_ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 5db5e78d198cc9f66aa5de6fdb0160e325b82591
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365833"
---
# <a name="execute_assert-macro"></a>\_ASSERT-Makro ausführen

Wertet einen Ausdruck in Debug-und Retail-Builds aus. In Debugbuilds zeigt eine Diagnose Meldung an, wenn der Ausdruck **false** ist.

## <a name="syntax"></a>Syntax


```C++
void EXECUTE_ASSERT(
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

Im Gegensatz zum [**Assert**](assert.md) -Makro wertet dieses Makro den Ausdruck in Einzelhandels Builds aus. Wenn in Debugbuilds der Ausdruck **false** ist, zeigt das Makro ein Meldungs Feld mit dem Text des Ausdrucks, dem Namen der Quelldatei und der Zeilennummer an. Der Benutzer kann die-Übersetzung ignorieren, den Debugger eingeben oder die Anwendung beenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Assert-und breakpointmakros](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




