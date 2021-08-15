---
description: Wertet einen Ausdruck in Debug- und Verkaufsbuilds aus. Zeigt in Debugbuilds eine Diagnosemeldung an, wenn der Ausdruck FALSE ist.
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: EXECUTE_ASSERT Makro (Wxdebug.h)
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
ms.openlocfilehash: 871a8e4a04ec1dc31f3240b539a943c9c1733f083166fa4b7e6f6b52d14a466c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401792"
---
# <a name="execute_assert-macro"></a>EXECUTE \_ ASSERT-Makro

Wertet einen Ausdruck in Debug- und Verkaufsbuilds aus. Zeigt in Debugbuilds eine Diagnosemeldung an, wenn der Ausdruck **FALSE** ist.

## <a name="syntax"></a>Syntax


```C++
void EXECUTE_ASSERT(
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

Im Gegensatz zum [**ASSERT-Makro**](assert.md) wertet dieses Makro den Ausdruck in Einzelhandelsbuilds aus. Wenn der Ausdruck in Debugbuilds **FALSE** ist, zeigt das Makro ein Meldungsfeld mit dem Text des Ausdrucks, dem Namen der Quelldatei und der Zeilennummer an. Der Benutzer kann die Assertion ignorieren, den Debugger eingeben oder die Anwendung beenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Assert- und Breakpoint-Makros](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




