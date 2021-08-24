---
title: PATCHARRAY (Mmsystem.h)
description: PATCHARRAY ist ein Typ, der zum Definieren eines Arrays von PATCH-Patches verwendet wird.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- PATCHARRAY– PATCHPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d1d14696d7bb76827f902609cb1411f7890adeac53092e1b66b7eda16604320
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806070"
---
# <a name="patcharray"></a>PATCHARRAY

PATCHARRAY ist ein Typ, der zum Definieren eines Arrays von PATCH-Patches verwendet wird.


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**PATCHARRAY– \[ PATCHPATCHSIZE\]**
</dt> <dd>

Jedes Element im Array entspricht einem Patch mit jedem der 16 Bits, die einen der 16 CAB-Kanäle darstellen. Bits werden für jeden Kanal festgelegt, der diesen bestimmten Patch verwendet. Wenn z. B. patch number 0 von den physischen CHANNELS 0 und 8 verwendet wird, sollte Element 0 des Arrays auf 0x0101 festgelegt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Version<br/>                  | Kombinnische Instrument-Digitalschnittstelle (INSTRUMENT Digital Interface, MUSIC), TYPEN VON TYPEN<br/>                                        |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DATENTYPEN](midi-event-types.md)
</dt> </dl>

 

 





