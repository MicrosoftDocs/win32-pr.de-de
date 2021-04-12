---
description: Gibt Informationen über das Videosignal außer der Schutz Ebene an.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02247c48b89e61d49afe7f8f6f3821da68ff050b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527875"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a>OPM \_ Set \_ ACP \_ und \_ cgmsa \_ Signalisierung

Gibt Informationen über das Videosignal außer der Schutz Ebene an.



| Anforderung | Wert |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| Befehls-GUID | OPM \_ Set \_ ACP \_ und \_ cgmsa \_ Signalisierung                                                                                |
| Eingabedaten   | Eine [**OPM \_ \_ -Set ACP- \_ und \_ cgmsa- \_ Signalisierungs \_ Parameter-**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) Struktur |



 

## <a name="remarks"></a>Bemerkungen

Dieser Befehl entspricht dem DXVA-Befehl "", der \_ im Certified Output Protection Protocol (COPP) verwendet wird.

Für CGMS-a erfordern bestimmte Schutzstandards, dass das Fernsehsignal Informationen in denselben VBI-Wellenform-Paketen wie die CGMS-a-Bits enthält. Unter anderem umfasst diese Informationen das Seitenverhältnis des Bilds. Fernsehgeräte können schlecht angezeigt werden, wenn die Seitenverhältnis Informationen nicht mit dem Videostream konsistent sind. Die Anwendung kann diesen Befehl verwenden, um das Seitenverhältnis anzugeben, damit der Grafiktreiber die richtigen VBI-Pakete generieren kann.

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

 

 




