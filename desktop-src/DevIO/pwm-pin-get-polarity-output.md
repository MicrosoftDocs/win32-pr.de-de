---
description: Enthält einen Wert, der zurückgegeben werden soll.
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: PWM_PIN_GET_POLARITY_OUTPUT Struktur (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_POLARITY_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 81cf7b658a0024c3280db1523af34aaf2ef17262
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958333"
---
# <a name="pwm_pin_get_polarity_output-structure"></a>PWM- \_ Pin \_ Get Polarität- \_ \_ Ausgabestruktur

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Enthält einen Wert, der zurückgegeben werden soll.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PWM_PIN_GET_POLARITY_OUTPUT {
  PWM_POLARITY Polarity;
} PWM_PIN_GET_POLARITY_OUTPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**Gan**
</dt> <dd>

Die Polarität der PIN oder des Kanals als [**PWM- \_ polationswert**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) . Die Polarität ist entweder "hoch" oder "aktiv".

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

[**IOCTL \_ PWM- \_ Pin \_ get \_ Polarität**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[**PWM- \_ Polarität**](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

