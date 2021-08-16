---
description: Wertet einen Ausdruck aus und zeigt eine Diagnosemeldung an, wenn der Ausdruck FALSE ist. Wird in Einzelhandelsbuilds ignoriert.
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: ASSERT-Makro (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1c64ae2256ae132fccdca6e483fae3f79d28b0cda66d7701acbe95abb1222d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824429"
---
# <a name="assert-macro"></a>ASSERT-Makro

Wertet einen Ausdruck aus und zeigt eine Diagnosemeldung an, wenn der Ausdruck **FALSE** ist. Wird in Einzelhandelsbuilds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void ASSERT(
   BOOL cond
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

Wenn der Ausdruck in Debugbuilds **FALSE** ist, zeigt dieses Makro ein Meldungsfeld mit dem Text des Ausdrucks, dem Namen der Quelldatei und der Zeilennummer an. Der Benutzer kann die Assertion ignorieren, den Debugger eingeben oder die Anwendung beenden.

## <a name="examples"></a>Beispiele


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Assert- und Breakpoint-Makros](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




