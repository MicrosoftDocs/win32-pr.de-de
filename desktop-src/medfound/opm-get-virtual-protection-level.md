---
description: Gibt die virtuelle Schutzebene für einen angegebenen Schutzmechanismus zurück.
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: OPM_GET_VIRTUAL_PROTECTION_LEVEL (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fb4130b4ad700de2328114dbf900ff7d122045b277c8a5ae812332c730a5d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972919"
---
# <a name="opm_get_virtual_protection_level"></a>OPM \_ GET \_ VIRTUAL \_ PROTECTION \_ LEVEL

Gibt die virtuelle Schutzebene für einen angegebenen Schutzmechanismus zurück.

Die *virtuelle* Schutzebene ist die Ebene, die von der Anwendung während der aktuellen OPM-Sitzung (Output Protection Manager) angefordert wird. Der Treiber kann aufgrund von Ereignissen außerhalb dieser OPM-Sitzung eine höhere Ebene anwenden. Um die tatsächliche Schutzebene zu ermitteln, die wirksam ist, senden Sie die [**OPM \_ GET ACTUAL \_ PROTECTION \_ \_ LEVEL-Abfrage.**](opm-get-actual-protection-level.md)



| Anforderung | Wert |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ GET \_ VIRTUAL \_ PROTECTION \_ LEVEL                                                                                                                                          |
| Eingabedaten   | Der abzufragende Schutzmechanismus, der als 32-Bit-Ganzzahl angegeben wird. Der Wert wird als Member der [**OPM-Schutztypflags**](opm-protection-type-flags.md)interpretiert. |
| Daten zurückgeben  | Eine [**OPM \_ STANDARD \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                                   |



 

## <a name="remarks"></a>Hinweise

Die Schutzebene wird im **ulInformation-Member** der [**OPM \_ STANDARD \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) zurückgegeben. Die Bedeutung dieses Werts hängt vom abgefragten Schutzmechanismus ab. Für jeden Schutzmechanismus ist der Wert von **ulInformation** ein Flag aus einer anderen Enumeration, wie in der folgenden Tabelle dargestellt.



| Schutzmechanismus | Enumeration                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**OPM \_ ACP \_ PROTECTION \_ LEVEL**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [**CGMS-A-Schutzflags**](cgms-a-protection-flags.md)        |
| DPCP                 | [**OPM \_ DPCP \_ PROTECTION \_ LEVEL**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| Hdcp                 | [**OPM \_ HDCP \_ PROTECTION \_ LEVEL**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Diese Abfrage entspricht der \_ DXVA-Abfrage COPPQueryLocalProtectionLevel, die im Certified Output Protection Protocol (COPP) verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[OPM-Statusanforderungen](opm-status-requests.md)
</dt> </dl>

 

 




