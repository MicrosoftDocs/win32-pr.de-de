---
description: Enthält den aktuellen Prozentsatz des Arbeitszyklus für eine Stecknadel oder einen Kanal in einem PWM-Controller (Pulse Width PwM).
ms.assetid: 09C0232A-DF5C-4A1C-8138-D3D65E45731B
title: PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT -Struktur (Pwm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: dda05c06ee8c53968647bc29da2febee14abf758d4ad228c16178703c2d1da08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053320"
---
# <a name="pwm_pin_get_active_duty_cycle_percentage_output-structure"></a>PWM \_ PIN GET ACTIVE DUTY CYCLE PERCENTAGE OUTPUT \_ \_ \_ \_ \_ \_ structure

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Enthält den aktuellen Prozentsatz des Arbeitszyklus für eine Stecknadel oder einen Kanal in einem PWM-Controller (Pulse Width PwM).

## <a name="syntax"></a>Syntax


```C++
typedef struct _PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**Percentage**
</dt> <dd>

Der aktuelle PWM-Signal-Pflichtzyklus als \_ PWM-PROZENTSATZ, bei dem es sich um einen ULONGLONG-Wert handelt.

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

[**IOCTL \_ PWM \_ PIN \_ GET \_ ACTIVE \_ DUTY \_ CYCLE \_ PERCENTAGE**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




