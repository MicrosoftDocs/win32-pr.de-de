---
description: Gibt eine Beschreibung des Videosignals zurück, das über den Connector übertragen wird.
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: OPM_GET_ACTUAL_OUTPUT_FORMAT (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37f35e9f3d64bd1a72bb6800011978ea1cf2f4c60f523a344594f949beb4f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102074"
---
# <a name="opm_get_actual_output_format"></a>OPM \_ GET \_ ACTUAL \_ OUTPUT \_ FORMAT

Gibt eine Beschreibung des Videosignals zurück, das über den Connector übertragen wird.



| Anforderung | Wert |
|--------------|------------------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ GET \_ ACTUAL \_ OUTPUT \_ FORMAT                                             |
| Eingabedaten   | Keine                                                                         |
| Daten zurückgeben  | Eine [**OPM \_ ACTUAL OUTPUT \_ \_ FORMAT-Struktur**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) |



 

## <a name="remarks"></a>Hinweise

Das Videosignal, das über den Connector übertragen wird, hat nicht unbedingt das gleiche Format wie der Desktopanzeigemodus. Der Desktopanzeigemodus kann beispielsweise 1.024 x 768 Pixel bei 85 Hz betragen, während der Connector ein S-Video-Connector sein kann, der ein Videosignal mit 720 x 480 Pixeln und 60/1,01 Hz-Interlacing überträgt. In diesem Fall gibt der Treiber die Auflösung des S-Video-Signals zurück, nicht die Desktopauflösung.

Diese Abfrage entspricht der \_ DXVA-Abfrage COPPQueryDisplayData, die im Certified Output Protection Protocol (COPP) verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                      |
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

 

 




