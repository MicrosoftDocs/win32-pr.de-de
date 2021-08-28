---
description: Die BIT-Flagkonstierten PHONEHOOKSWITCHDEV beschreiben verschiedene Audio-E/A-Geräte, die jeweils über einen eigenen Hookschalter vom \_ Computer aus steuerbar sind.
ms.assetid: b3272a75-87b0-4afc-b2e2-2d65e4b49300
title: PHONEHOOKSWITCHDEV_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77e6b776b89adf6224d6feaef8deeef1f9f71b9888929f3aea08b5342adc1dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796750"
---
# <a name="phonehookswitchdev_-constants"></a>PHONEHOOKSWITCHDEV-Konstanten \_

Die **BIT-Flagkonst constants PHONEHOOKSWITCHDEV \_** beschreiben verschiedene Audio-E/A-Geräte, die jeweils über einen eigenen Hookschalter vom Computer aus steuerbar sind.

<dl> <dt>

<span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**PHONEHOOKSWITCHDEV-HANDSET \_**
</dt> <dd> <dl> <dt>



Dies ist ein Standardtelefon für Hör- und Hörnchen.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**PHONEHOOKSWITCHDEV-HEADSET \_**
</dt> <dd> <dl> <dt>



Dies ist ein Headset, das mit dem Telefonsatz verbunden ist.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV-LAUTSPRECHER \_**
</dt> <dd> <dl> <dt>



Dies ist ein integrierter Fon und mikrofon. Dabei kann es sich auch um einen extern verbundenen Lautsprecher mit dem Telefonsatz geben.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Diese Konstanten werden in der [**PHONECAPS-Datenstruktur**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) verwendet, um die Hookswitch-Gerätefunktionen eines Telefongeräts anzugeben. Die [**PHONESTATUS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) meldet den Zustand der Hookswitchgeräte des Telefons. Die Funktion [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) und [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) verwenden sie als Parameter, um das E/A-Gerät des Telefons auszuwählen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




