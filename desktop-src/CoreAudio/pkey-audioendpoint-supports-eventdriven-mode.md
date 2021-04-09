---
description: "\"Pkey \\_ audioendpoint\" \\_ unterstützt die \\_ Eigenschaft \"Eventgesteuerte \\_ Modus\". gibt an, ob der Endpunkt den ereignisgesteuerten Modus unterstützt."
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: PKEY_AudioEndpoint_Supports_EventDriven_Mode (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2707de83721d546040ac878b337faea12f533bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958536"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a>Pkey \_ audioendpoint \_ unterstützt den \_ ereignisbasierten \_ Modus

" **Pkey \_ audioendpoint" unterstützt die Eigenschaft " \_ \_ Eventgesteuerte \_ Modus** ". gibt an, ob der Endpunkt den ereignisgesteuerten Modus unterstützt.

Der **VT** -Member der **PROPVARIANT** -Struktur ist auf VT \_ UI4 festgelegt.

Der **uintval** -Member der **PROPVARIANT** -Struktur ist ein **DWORD** , das angibt, ob der Endpunkt den ereignisgesteuerten Modus unterstützt.

## <a name="remarks"></a>Bemerkungen

Dieser Eigenschafts Wert wird von einem audiooem in einer INF-Datei aufgefüllt, um anzugeben, dass die Hdaudio-Hardware den ereignisbasierten Modus gemäß der WHQL-Anforderung unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften des audioendpunkts**](audio-endpoint-properties.md)
</dt> <dt>

[Kernaudioeigenschaften](core-audio-properties.md)
</dt> </dl>

 

 




