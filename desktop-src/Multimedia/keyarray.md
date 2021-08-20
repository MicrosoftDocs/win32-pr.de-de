---
title: KEYARRAY (Mmsystem.h)
description: KEYARRAY gibt einen Typ an, mit dem ein Array von Schlüsseln definiert wird.
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- KEYARRAYPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c5f578b912a7b184f9f455bc4a730132b2316472d061532c48847c312302d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140040"
---
# <a name="keyarray"></a>KEYARRAY

KEYARRAY gibt einen Typ an, mit dem ein Array von Schlüsseln definiert wird.


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**\[KEYARRAYPATCHSIZE\]**
</dt> <dd>

Jedes Element im Array entspricht einem schlüsselbasierten Patch, bei dem jedes der 16 Bits einen der 16 BITS-Kanäle darstellt. Bits werden für jeden Kanal festgelegt, der diesen bestimmten Patch verwendet. Wenn z. B. der Patch für Schlüsselnummer 60 von den physischen SENDER-Kanälen 9 und 15 verwendet wird, sollte Element 60 des Arrays auf 0x8200.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Version<br/>                  | Instruments Instrument Digital Interface (KEYBOARD), KEYBOARD-Typen<br/>                                        |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DATEITYP-Typen](midi-event-types.md)
</dt> </dl>

 

 





