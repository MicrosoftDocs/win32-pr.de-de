---
description: 'Weitere Informationen zu: OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c06da78ea9ae1a4f0ea58f0fb8770dffadff6a34d577fd2328816ffc100e4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102064"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a>OPM \_ GET ACP AND CGMSA SIGNALING (OPM GET \_ \_ ACP- UND \_ CGMSA-SIGNALISIERUNG) \_

Gibt die folgenden Informationen zu einer Videoausgabe zurück:

-   Eine Liste der vom Fahrer unterstützten Tv-Schutzstandards.
-   Der Standard, der derzeit aktiv ist.
-   Das aktuelle Seitenverhältnis oder andere Signaldaten.



| Anforderung | Wert |
|--------------|-------------------------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ GET ACP AND CGMSA SIGNALING (OPM GET \_ \_ ACP- UND \_ CGMSA-SIGNALISIERUNG) \_                                                |
| Eingabedaten   | Keine                                                                                |
| Daten zurückgeben  | EINE [**OPM \_ \_ ACP- UND \_ CGMSA \_ SIGNALING-Struktur**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) |



 

## <a name="remarks"></a>Hinweise

Diese Abfrage entspricht der DXVA \_ COPPQuerySignaling-Abfrage, die im Certified Output Protection Protocol (COPP) verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[OPM-Statusanforderungen](opm-status-requests.md)
</dt> </dl>

 

 




