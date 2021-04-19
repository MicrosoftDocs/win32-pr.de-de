---
description: Die "phonehuokswitchdev" \_ -Bitflag-Konstanten beschreiben verschiedene e/a-Audiogeräte, die jeweils über einen eigenen, von einem computergesteuerten Port verfügen.
ms.assetid: b3272a75-87b0-4afc-b2e2-2d65e4b49300
title: PHONEHOOKSWITCHDEV_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a6727bf8103c35402bebc048de4ed9286650be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374041"
---
# <a name="phonehookswitchdev_-constants"></a>Phonehuokswitchdev- \_ Konstanten

Die " **phonehuokswitchdev \_** "-Bitflag-Konstanten beschreiben verschiedene e/a-Audiogeräte, die jeweils über einen eigenen, von einem computergesteuerten Port verfügen.

<dl> <dt>

<span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**phonehuokswitchdev- \_ Mobiltelefon**
</dt> <dd> <dl> <dt>



Dabei handelt es sich um ein Standardmäßiges Ohr-und-Telefon Telefon.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**phonehuokswitchdev- \_ Headset**
</dt> <dd> <dl> <dt>



Dabei handelt es sich um ein mit dem Telefon Satz verbundenes Headset.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**phonehuokswitchdev- \_ Sprecher**
</dt> <dd> <dl> <dt>



Dabei handelt es sich um einen integrierten Lautsprecher und ein Mikrofon. Dabei kann es sich auch um einen extern verbundenen Ergänzung-Sprecher mit dem Telefon Satz handeln.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Diese Konstanten werden in der [**phonecaps**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) -Datenstruktur verwendet, um die Gerätefunktionen von "hostingswitch" auf einem Telefongerät anzugeben. In der [**phonestatus**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) -Struktur wird der Status der Geräte des Telefons für den Gerätewechsel gemeldet. Die Funktion " [**phonesethookswitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) " und " [**phonegethookswitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) " verwenden Sie als Parameter, um das e/a-Gerät des Telefons auszuwählen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




