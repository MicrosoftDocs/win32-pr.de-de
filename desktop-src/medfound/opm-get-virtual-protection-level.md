---
description: Gibt die virtuelle Schutz Ebene für einen angegebenen Schutzmechanismus zurück.
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: OPM_GET_VIRTUAL_PROTECTION_LEVEL (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7ac36abd0a043a74a18401205bbb5e661ac17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347860"
---
# <a name="opm_get_virtual_protection_level"></a>OPM \_ - \_ Ebene zum virtuellen \_ Schutz \_

Gibt die virtuelle Schutz Ebene für einen angegebenen Schutzmechanismus zurück.

Die *virtuelle* Schutz Ebene ist die Ebene, die von der Anwendung während der aktuellen Output Protection Manager-Sitzung (OPM) angefordert wird. Der Treiber kann aufgrund von Ereignissen außerhalb dieser OPM-Sitzung eine höhere Ebene anwenden. Um die tatsächliche Sicherheitsstufe zu ermitteln, die wirksam ist, senden Sie die OPM-Abfrage zum Abrufen der [**\_ \_ tatsächlichen \_ Schutz \_ Ebene**](opm-get-actual-protection-level.md) .



| Anforderung | Wert |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ - \_ Ebene zum virtuellen \_ Schutz \_                                                                                                                                          |
| Eingabedaten   | Der abzufragende Schutzmechanismus, der als 32-Bit-Ganzzahl angegeben wird. Der Wert wird als Member der [**OPM-Schutztyp Flags**](opm-protection-type-flags.md)interpretiert. |
| Daten zurückgeben  | Eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Die Schutz Ebene wird im **ulinformation** -Member der [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur zurückgegeben. Die Bedeutung dieses Werts hängt von dem abgefragten Schutzmechanismus ab. Für jeden Schutzmechanismus ist der Wert von **ulinformation** ein Flag aus einer anderen Enumeration, wie in der folgenden Tabelle dargestellt.



| Schutzmechanismus | Enumeration                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**OPM \_ -ACP- \_ Schutz \_ Ebene**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [**CGMS-A-Schutzflags**](cgms-a-protection-flags.md)        |
| Dpcp                 | [**OPM \_ dpcp- \_ Schutz \_ Ebene**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| HDCP                 | [**OPM- \_ HDCP- \_ Schutz \_ Ebene**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Diese Abfrage entspricht der DXVA- \_ Abfrage "coppquerylocalschutzlevel", die im Certified Output Protection Protocol (COPP) verwendet wird.

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

 

 




