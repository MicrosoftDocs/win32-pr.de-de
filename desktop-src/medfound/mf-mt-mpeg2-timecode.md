---
description: Gibt für einen Medientyp an, der einen MPEG-2-Transportdaten Strom (TS) beschreibt, gibt an, dass die Transport Pakete einen 4-Byte-Zeit Code enthalten.
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: MF_MT_MPEG2_TIMECODE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc9db5d7b3c6e94f7845bec2bd98c569d1b1f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216883"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a>MF \_ MT-Attribut "- \_ \_ Zeit Leitzahl"

Gibt für einen Medientyp an, der einen MPEG-2-Transportdaten Strom (TS) beschreibt, gibt an, dass die Transport Pakete einen 4-Byte-Zeit Code enthalten.

## <a name="data-type"></a>Datentyp

**UINT32**



| Wert                                                                                                | Bedeutung                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Es wurde kein Zeit Code hinzugefügt.<br/>                                                                                                              |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Ein 4-Byte-Zeit Code wird zu Beginn jedes Transport Pakets hinzugefügt. Dieser Zeitaufwand wird für einige Digital TV-Standards benötigt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




