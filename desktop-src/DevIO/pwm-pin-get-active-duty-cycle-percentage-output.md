---
description: Enthält den aktuellen Duty-Cycle-Prozentsatz für eine PIN oder einen Kanal in einem PWM-Controller (Pulse Width Modulation).
ms.assetid: 09C0232A-DF5C-4A1C-8138-D3D65E45731B
title: PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT Struktur (PWM. h)
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
ms.openlocfilehash: 607fcb1ab429e7cbe9aee593f75d48f0f9d308bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126770"
---
# <a name="pwm_pin_get_active_duty_cycle_percentage_output-structure"></a>PWM- \_ Pin \_ get \_ Active \_ Duty \_ Cycle Prozent der \_ \_ Ausgabestruktur

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Enthält den aktuellen Duty-Cycle-Prozentsatz für eine PIN oder einen Kanal in einem PWM-Controller (Pulse Width Modulation).

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

Der aktuelle PWM-Signal-Duty-Cycle als PWM- \_ Prozentsatz, bei dem es sich um einen ULONGLONG-Wert handelt.

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

[**IOCTL \_ PWM- \_ Pin \_ get \_ Active \_ Duty \_ Cycle \_ Prozent**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




