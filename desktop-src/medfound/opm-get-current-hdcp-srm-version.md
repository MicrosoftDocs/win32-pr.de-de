---
description: Gibt die Versionsnummer der von der Videoausgabe verwendeten SRM (System erneuerbarkeits Meldung) zurück.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05ad53ae58e2141c63179c84a90f90cea86fb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372917"
---
# <a name="opm_get_current_hdcp_srm_version"></a>OPM \_ get \_ Current \_ HDCP \_ SRM- \_ Version

Gibt die Versionsnummer der von der Videoausgabe verwendeten SRM (System erneuerbarkeits Meldung) zurück.



| Anforderung | Wert |
|--------------|-----------------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ get \_ Current \_ HDCP \_ SRM- \_ Version                                       |
| Eingabedaten   | Keine                                                                        |
| Daten zurückgeben  | Eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur |



 

## <a name="remarks"></a>Bemerkungen

Wenn diese Abfrage erfolgreich ist, enthält der **ulinformation** -Member der [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur die SRM-Versionsnummer im Little-Endian-Format.

Mithilfe von SRMs wird die Liste der gesperrten HDCP-Geräte (High-Bandwidth Digital Content Protection) aktualisiert. SRMs werden mit dem Videoinhalt geliefert. Um den SRM festzulegen, senden Sie den Befehl [**OPM \_ Set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .

Diese Abfrage kann bewirken, dass die [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) -Methode einen der folgenden Fehlercodes zurückgibt.



| Rückgabecode                                            | Beschreibung                             |
|--------------------------------------------------------|-----------------------------------------|
| Fehler \_ Grafik \_ OPM \_ HDCP \_ SRM \_ nie \_ festgelegt            | Die Anwendung hat keinen SRM festgelegt.     |
| Fehler \_ Grafik- \_ OPM- \_ Ausgabe \_ \_ \_ unterstützt \_ HDCP nicht | HDCP wird von der Videoausgabe nicht unterstützt. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[OPM-Status Anforderungen](opm-status-requests.md)
</dt> </dl>

 

 




