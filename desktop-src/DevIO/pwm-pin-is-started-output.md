---
description: Enthält den aktuellen Signalgenerierungsstatus eines Pins.
ms.assetid: 07D76F8D-C5B5-4500-BFA2-452989868027
title: PWM_PIN_IS_STARTED_OUTPUT -Struktur (Pwm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_IS_STARTED_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 448b38e66b7cfb4bf7e24c5d3b7658d0e38ccb8a5ca8c95e1155129737087c68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076184"
---
# <a name="pwm_pin_is_started_output-structure"></a>PWM \_ PIN IS STARTED \_ \_ \_ OUTPUT-Struktur

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Enthält den aktuellen Signalgenerierungsstatus eines Pins.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PWM_PIN_IS_STARTED_OUTPUT {
  BOOLEAN IsStarted;
} PWM_PIN_IS_STARTED_OUTPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**Isstarted**
</dt> <dd>

Der Aktuelle Signalgenerierungszustand anheften. Der Wert true bedeutet, dass die Stecknadel gestartet wird. Der Wert false bedeutet, dass die Stecknadel beendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                             |
| KMDF-Mindestversion<br/>     | 1.19<br/>                                                                                  |
| UMDF-Mindestversion<br/>     | 2.19<br/>                                                                                  |
| Header<br/>                   | <dl> <dt>Pwm.h (einschließlich Pwm.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOCTL \_ PWM \_ PIN WIRD \_ \_ GESTARTET**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**)
</dt> </dl>

 

 




