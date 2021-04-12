---
description: Enthält einen gewünschten Duty-Cycle-Prozentsatz für eine PIN oder einen Kanal in einem PWM-Controller (Pulse Width Modulation).
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT Struktur (PWM. h)
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
ms.openlocfilehash: 98811ace7ce8fce760e10757b8bf012cc2b9b27d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392934"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a>PWM- \_ Pin \_ Set \_ Active \_ Duty \_ Cycle \_ Prozentsatz der \_ Eingabe Struktur

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Enthält einen gewünschten Duty-Cycle-Prozentsatz für eine PIN oder einen Kanal in einem PWM-Controller (Pulse Width Modulation).

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

Der gewünschte PWM-Signal-Duty-Cycle als PWM- \_ Prozentsatz, bei dem es sich um einen ULONGLONG-Wert handelt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                             |
| KMDF-Mindestversion<br/>     | 1.19<br/>                                                                                  |
| UMDF-Mindestversion<br/>     | 2.19<br/>                                                                                  |
| Header<br/>                   | <dl> <dt>PWM. h (Include PWM. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOCTL \_ PWM \_ Pin \_ Set \_ Active \_ Duty \_ Cycle \_ Prozentsatz**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




