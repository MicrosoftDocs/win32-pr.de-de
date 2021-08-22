---
description: Gibt andere Informationen zum Videosignal als die Schutzebene an.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 265d2986c624e30d342a4b3bc5e957e04c56bd01d51e146536de5731db42ace8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343510"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a>OPM \_ SET \_ ACP \_ AND \_ CGMSA \_ SIGNALING

Gibt andere Informationen zum Videosignal als die Schutzebene an.



| Anforderung | Wert |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| Befehls-GUID | OPM \_ SET \_ ACP \_ AND \_ CGMSA \_ SIGNALING                                                                                |
| Eingabedaten   | EINE [**OPM \_ SET \_ \_ ACP- UND \_ CGMSA \_ SIGNALING \_ PARAMETERS-Struktur**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) |



 

## <a name="remarks"></a>Hinweise

Dieser Befehl entspricht dem DXVA \_ COPPSetSignaling-Befehl, der im Certified Output Protection Protocol (COPP) verwendet wird.

Für CGMS-A erfordern bestimmte Schutzstandards, dass das Fernsehsignal Informationen in denselben VBI-Wellenformpaketen wie die CGMS-A-Bits enthält. Zu diesen Informationen gehört unter anderem das Bildseitenverhältnis. Fernsehgeräte werden möglicherweise schlecht angezeigt, wenn die Informationen zum Seitenverhältnis nicht mit dem Videostream konsistent sind. Die Anwendung kann diesen Befehl verwenden, um das Seitenverhältnis anzugeben, sodass der Grafiktreiber die richtigen VBI-Pakete generieren kann.

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

 

 




