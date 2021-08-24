---
description: Die Eigenschaft PKEY AudioEndpoint Supports EventDriven Mode gibt an, ob der Endpunkt \_ \_ den \_ \_ ereignisgesteuerten Modus unterstützt.
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: PKEY_AudioEndpoint_Supports_EventDriven_Mode (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 280be65d4ae8e0b557bd96320ea31f67ba75657ecb5b685608bd2c314e10836d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758920"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a>PKEY \_ AudioEndpoint \_ unterstützt den \_ EventDriven-Modus. \_

Die **Eigenschaft PKEY \_ AudioEndpoint \_ Supports \_ EventDriven \_ Mode** gibt an, ob der Endpunkt den ereignisgesteuerten Modus unterstützt.

Der **vt-Member** der **PROPVARIANT-Struktur** ist auf VT \_ UI4 festgelegt.

Der **uintVal-Member** der **PROPVARIANT-Struktur** ist ein **DWORD,** das angibt, ob der Endpunkt den ereignisgesteuerten Modus unterstützt.

## <a name="remarks"></a>Hinweise

Dieser Eigenschaftswert wird von einem Audio-OEM in einer INF-Datei aufgefüllt, um anzugeben, dass die HDAudio-Hardware den ereignisgesteuerten Modus nach WHQL-Anforderung unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Audioendpunkteigenschaften**](audio-endpoint-properties.md)
</dt> <dt>

[Kernaudioeigenschaften](core-audio-properties.md)
</dt> </dl>

 

 




