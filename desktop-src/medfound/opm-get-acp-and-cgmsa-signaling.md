---
description: 'Weitere Informationen finden Sie hier: OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf6294c3f1d90ac8a2292c65b3c1b8558e69220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355566"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a>OPM \_ get \_ ACP \_ und \_ cgmsa- \_ Signalisierung

Gibt die folgenden Informationen zu einer Videoausgabe zurück:

-   Eine Liste der vom Treiber unterstützten TV-Schutzstandards.
-   Der Standard, der derzeit aktiv ist.
-   Das aktuelle Seitenverhältnis oder andere Signalisierungs Daten.



| Anforderung | Wert |
|--------------|-------------------------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ get \_ ACP \_ und \_ cgmsa- \_ Signalisierung                                                |
| Eingabedaten   | Keine                                                                                |
| Daten zurückgeben  | Eine [**OPM \_ -ACP- \_ und \_ cgmsa- \_ Signal**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) Struktur |



 

## <a name="remarks"></a>Bemerkungen

Diese Abfrage entspricht der DXVA-Option " \_ coppquerysigna", die im Certified Output Protection Protocol (COPP) verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[OPM-Status Anforderungen](opm-status-requests.md)
</dt> </dl>

 

 




