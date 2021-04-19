---
description: Wertet einen Ausdruck aus und zeigt eine Diagnose Meldung an, wenn der Ausdruck false ist. Wird in Einzelhandels Builds ignoriert.
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: Assert-Makro (wxdebug. h)
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
ms.openlocfilehash: 8617d1c86f655cc9b44ea6619931f73888ae2a67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359381"
---
# <a name="assert-macro"></a>ASSERT-Makro

Wertet einen Ausdruck aus und zeigt eine Diagnose Meldung an, wenn der Ausdruck **false** ist. Wird in Einzelhandels Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void ASSERT(
   BOOL cond
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

Wenn in Debugbuilds der Ausdruck **false** ist, zeigt dieses Makro ein Meldungs Feld mit dem Text des Ausdrucks, dem Namen der Quelldatei und der Zeilennummer an. Der Benutzer kann die-Übersetzung ignorieren, den Debugger eingeben oder die Anwendung beenden.

## <a name="examples"></a>Beispiele


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Assert-und breakpointmakros](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




