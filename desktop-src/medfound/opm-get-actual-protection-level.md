---
description: Gibt die globale Schutz Ebene für einen angegebenen Schutzmechanismus zurück.
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: OPM_GET_ACTUAL_PROTECTION_LEVEL (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 960d704fd44ca779f128795b26603698bb0ad622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041903"
---
# <a name="opm_get_actual_protection_level"></a>OPM \_ get \_ Actual \_ Protection \_ Level

Gibt die globale Schutz Ebene für einen angegebenen Schutzmechanismus zurück.



| Anforderung | Wert |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ get \_ Actual \_ Protection \_ Level                                                                                                                                       |
| Eingabedaten   | Der abzufragende Schutzmechanismus, der als 32-Bit-Ganzzahl angegeben wird. Der Wert wird als Member der [OPM-Schutztyp Flags](opm-protection-type-flags.md)interpretiert. |
| Daten zurückgeben  | Eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur                                                                                               |



 

## <a name="remarks"></a>Bemerkungen

Die globale Schutz Ebene ist die Schutz Ebene, die zurzeit auf den Connector angewendet wird, unabhängig davon, wie der Grafiktreiber angewiesen wurde, den Schutz anzuwenden. Beispielsweise kann eine Anwendung die ACP-Schutz Ebene durch Aufrufen der **changedisplaysettingsex** -Funktion festlegen. In diesem Fall würde die globale Schutz Ebene diese Einstellung widerspiegeln, auch wenn Sie nicht durch Output Protection Manager (OPM) angefordert wurde.

Die Schutz Ebene wird im **ulinformation** -Member der [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur zurückgegeben. Die Bedeutung dieses Werts hängt von dem abgefragten Schutzmechanismus ab. Für jeden Schutzmechanismus ist der Wert von **ulinformation** ein Flag aus einer anderen Enumeration, wie in der folgenden Tabelle dargestellt.



| Schutzmechanismus | Enumeration                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**OPM \_ -ACP- \_ Schutz \_ Ebene**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [CGMS-A-Schutzflags](cgms-a-protection-flags.md)            |
| Dpcp                 | [**OPM \_ dpcp- \_ Schutz \_ Ebene**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| HDCP                 | [**OPM- \_ HDCP- \_ Schutz \_ Ebene**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Diese Abfrage entspricht der DXVA- \_ Abfrage "coppqueryglobalschutzlevel", die im Certified Output Protection Protocol (COPP) verwendet wird.

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

 

 




