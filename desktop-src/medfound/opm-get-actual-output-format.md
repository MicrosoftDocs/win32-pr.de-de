---
description: Gibt eine Beschreibung des Videosignals zurück, das über den Connector übertragen wird.
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: OPM_GET_ACTUAL_OUTPUT_FORMAT (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eeca9bcf8fde670447afe4268a86ffa31b6a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344419"
---
# <a name="opm_get_actual_output_format"></a>OPM \_ get \_ tatsächliches \_ Ausgabe \_ Format

Gibt eine Beschreibung des Videosignals zurück, das über den Connector übertragen wird.



| Anforderung | Wert |
|--------------|------------------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ get \_ tatsächliches \_ Ausgabe \_ Format                                             |
| Eingabedaten   | Keine                                                                         |
| Daten zurückgeben  | Eine [**tatsächliche OPM- \_ \_ Ausgabe \_ Format**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) Struktur |



 

## <a name="remarks"></a>Bemerkungen

Das über den Connector übertragene Videosignal weist nicht notwendigerweise dasselbe Format wie der Desktop Anzeigemodus auf. Beispielsweise kann der Desktop Anzeigemodus 1024 x 768 Pixel bei 85 Hz sein, während der Connector ein S-Video-Connector sein kann, der ein Videosignal mit 720 x 480 Pixel, 60/1.01 Hz-Zeilen Sprung überträgt. In diesem Fall würde der Treiber die Auflösung des S-Video Signals und nicht die Desktop Auflösung zurückgeben.

Diese Abfrage entspricht der DXVA- \_ Abfrage "coppquerydisplaydata", die im Certified Output Protection Protocol (COPP) verwendet wird.

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

 

 




