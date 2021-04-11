---
description: Legt die HDCP-Schutz Ebene für die DVD-Wiedergabe fest, und zwar gemäß den DVD-Inhalts Regeln für das Scramble-System
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971d288367bdc5c59e11bdfd5b86fb233755c95e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130493"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a>OPM \_ Festlegen der \_ Schutz \_ Ebene \_ gemäß CSS- \_ \_ \_ DVD

Legt die HDCP-Schutz Ebene für die DVD-Wiedergabe fest, und zwar gemäß den DVD-Inhalts Regeln für das Scramble-System



| Anforderung | Wert |
|--------------|-----------------------------------------------------------------------------------------------------|
| Befehls-GUID | OPM \_ Festlegen der \_ Schutz \_ Ebene \_ gemäß CSS- \_ \_ \_ DVD                                                |
| Eingabedaten   | Eine [**OPM-Parameter Struktur zum \_ Festlegen der \_ Schutz \_ Ebenen \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) |



 

## <a name="remarks"></a>Bemerkungen

Dieser Befehl wird verwendet, um bei der Wiedergabe von Standard-DVDs High-Bandwidth Digital Content Protection (HDCP) festzulegen. Anders als beim OPM-Befehl zum [**\_ Festlegen der \_ Schutz \_ Ebene**](opm-set-protection-level.md) , wenn HDCP aus irgendeinem Grund nicht festgelegt werden kann, wird die Wiedergabe durch diesen Befehl nicht beendet. (DVD-CSS-Regeln enthalten eine "bestmögliche" Bereitstellung für Player.) Andernfalls ist dieser Befehl mit dem OPM-Befehl zum **\_ Festlegen der \_ Schutz \_ Ebene** identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[OPM-Befehle](opm-commands.md)
</dt> </dl>

 

 




