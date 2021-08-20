---
description: Für einen Medientyp, der einen MPEG-2-Transportstream (TS) beschreibt, gibt an, dass die Transportpakete einen 4-Byte-Zeitcode enthalten.
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: MF_MT_MPEG2_TIMECODE -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7a4ce6868f783ed33c50acd5a8648297648481a58c74198b0dcadd1bd237bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741764"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a>MF \_ MT \_ MPEG2 \_ TIMECODE-Attribut

Für einen Medientyp, der einen MPEG-2-Transportstream (TS) beschreibt, gibt an, dass die Transportpakete einen 4-Byte-Zeitcode enthalten.

## <a name="data-type"></a>Datentyp

**UINT32**



| Wert                                                                                                | Bedeutung                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Es wird kein Zeitcode hinzugefügt.<br/>                                                                                                              |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Am Anfang jedes Transportpakets wird ein 4-Byte-Zeitcode hinzugefügt. Dieser Zeitcode ist für einige Standards für digitale Fernsehsendungen erforderlich.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




