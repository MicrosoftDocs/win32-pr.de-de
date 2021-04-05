---
title: Patcharray (MMSYSTEM. h)
description: Patcharray ist ein Typ, der verwendet wird, um ein Array von MIDI-Patches zu definieren.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- patcharray midipatchsize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e07af0e878fc0d2fc79d6d17aafd48fbd991fb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859306"
---
# <a name="patcharray"></a>Patcharray

Patcharray ist ein Typ, der verwendet wird, um ein Array von MIDI-Patches zu definieren.


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**patcharray \[ midipatchsize\]**
</dt> <dd>

Jedes Element im Array entspricht einem Patch, wobei jedes der 16 Bits einen der 16-MIDI-Kanäle darstellt. Bits werden für jeden der Kanäle festgelegt, die diesen bestimmten Patch verwenden. Wenn beispielsweise die Patchnummer 0 von den physischen MIDI-Kanälen 0 und 8 verwendet wird, sollte Element 0 des Arrays auf 0x0101 festgelegt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Version<br/>                  | Digital Instrumentation Digital Interface (MIDI), MIDI-Typen<br/>                                        |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MIDI-Typen](midi-event-types.md)
</dt> </dl>

 

 





