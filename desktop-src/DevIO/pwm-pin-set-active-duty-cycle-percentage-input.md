---
description: Enthält einen gewünschten Prozentsatz für einen Arbeitszyklus für eine Stecknadel oder einen Kanal in einem PWM-Controller (Pulse Width PwM).
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT -Struktur (Pwm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: ca6b2ee6aa4d4d2da3f94aa7cc471de12c1f8040b597edf568bf061c8e392aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758850"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a>PWM PIN SET ACTIVE DUTY CYCLE PERCENTAGE INPUT structure (PWM \_ PIN SET ACTIVE DUTY CYCLE PERCENTAGE \_ \_ \_ \_ \_ \_ INPUT-Struktur)

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Enthält einen gewünschten Prozentsatz für einen Arbeitszyklus für eine Stecknadel oder einen Kanal in einem PWM-Controller (Pulse Width PwM).

## <a name="syntax"></a>Syntax


```C++
typedef struct _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**Percentage**
</dt> <dd>

Der gewünschte PWM-Signal-Pflichtzyklus als PWM PERCENTAGE, bei dem es \_ sich um einen ULONGLONG-Wert handelt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                             |
| KMDF-Mindestversion<br/>     | 1.19<br/>                                                                                  |
| UMDF-Mindestversion<br/>     | 2.19<br/>                                                                                  |
| Header<br/>                   | <dl> <dt>Pwm.h (einschließlich Pwm.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IOCTL \_ PWM \_ PIN \_ SET \_ ACTIVE \_ DUTY \_ CYCLE \_ PERCENTAGE**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




