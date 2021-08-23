---
description: Gibt die Versionsnummer der systemerneuerbarkeitsmeldung (System Renewability Message, SRM) zurück, die derzeit von der Videoausgabe verwendet wird.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee36516510d04fec067bbc692387e2e36b9da083db1a6daae0f51948a992cc83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887490"
---
# <a name="opm_get_current_hdcp_srm_version"></a>OPM GET CURRENT HDCP SRM VERSION (ABRUFEN \_ DER \_ AKTUELLEN \_ \_ HDCP-SRM-VERSION) \_

Gibt die Versionsnummer der systemerneuerbarkeitsmeldung (System Renewability Message, SRM) zurück, die derzeit von der Videoausgabe verwendet wird.



| Anforderung | Wert |
|--------------|-----------------------------------------------------------------------------|
| Anforderungs-GUID | OPM GET CURRENT HDCP SRM VERSION (ABRUFEN \_ DER \_ AKTUELLEN \_ \_ HDCP-SRM-VERSION) \_                                       |
| Eingabedaten   | Keine                                                                        |
| Daten zurückgeben  | Eine [**OPM \_ STANDARD \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Hinweise

Wenn diese Abfrage erfolgreich ist, enthält das **ulInformation-Element** der [**OPM \_ STANDARD \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) die SRM-Versionsnummer im Little-Endian-Format.

SRMs werden verwendet, um die Liste der gesperrten HDCP-Geräte (Digital Content Protection) High-Bandwidth zu aktualisieren. SRMs werden mit dem Videoinhalt bereitgestellt. Um den SRM festzulegen, senden Sie den [**BEFEHL OPM \_ SET \_ HDCP \_ SRM.**](opm-set-hdcp-srm.md)

Diese Abfrage kann dazu führen, dass die [**IOPMVideoOutput::GetInformation-Methode**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) einen der folgenden Fehlercodes zurückgibt.



| Rückgabecode                                            | Beschreibung                             |
|--------------------------------------------------------|-----------------------------------------|
| FEHLERGRAFIK \_ \_ OPM \_ HDCP \_ SRM \_ NEVER \_ SET            | Die Anwendung hat keinen SRM festgelegt.     |
| FEHLERGRAFIK \_ \_ \_ OPM-AUSGABE \_ \_ UNTERSTÜTZT \_ \_ HDCP NICHT | Die Videoausgabe unterstützt HDCP nicht. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[OPM-Statusanforderungen](opm-status-requests.md)
</dt> </dl>

 

 




