---
description: Legt die HDCP-Schutzebene für die DVD-Wiedergabe gemäß den REGELN des DVD Content Scramble System (CSS) fest.
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2290f8d0dd17e01d482c197a54448a3317b11f80840579c2ddd05f01b6103840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101904"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a>OPM \_ LEGT \_ \_ SCHUTZEBENE GEMÄß \_ \_ \_ \_ CSS-DVD FEST

Legt die HDCP-Schutzebene für die DVD-Wiedergabe gemäß den REGELN des DVD Content Scramble System (CSS) fest.



| Anforderung | Wert |
|--------------|-----------------------------------------------------------------------------------------------------|
| Befehls-GUID | OPM \_ LEGT \_ \_ SCHUTZEBENE GEMÄß \_ \_ \_ \_ CSS-DVD FEST                                                |
| Eingabedaten   | Eine [**OPM \_ SET PROTECTION LEVEL \_ \_ \_ PARAMETERS-Struktur**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) |



 

## <a name="remarks"></a>Hinweise

Dieser Befehl wird verwendet, um High-Bandwidth Digital Content Protection (HDCP) festzulegen, wenn Standard-DVDs wiedergegeben werden. Im Gegensatz zum [**BEFEHL OPM \_ SET PROTECTION \_ \_ LEVEL**](opm-set-protection-level.md) beendet dieser Befehl die Wiedergabe nicht, wenn HDCP aus irgendeinem Grund nicht festgelegt werden kann. (DVD-CSS-Regeln enthalten eine "bestmögliche" Bereitstellung für Player.) Andernfalls ist dieser Befehl mit dem **BEFEHL OPM \_ SET PROTECTION \_ \_ LEVEL** identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[OPM-Befehle](opm-commands.md)
</dt> </dl>

 

 




