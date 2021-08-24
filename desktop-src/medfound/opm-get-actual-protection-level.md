---
description: Gibt die globale Schutzebene für einen angegebenen Schutzmechanismus zurück.
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: OPM_GET_ACTUAL_PROTECTION_LEVEL (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ed5d895c037fedfa97bbafab8331d685af9a7f1ce81489b8d600bd903aa2a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101919"
---
# <a name="opm_get_actual_protection_level"></a>OPM \_ GET \_ ACTUAL \_ PROTECTION \_ LEVEL

Gibt die globale Schutzebene für einen angegebenen Schutzmechanismus zurück.



| Anforderung | Wert |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ GET \_ ACTUAL \_ PROTECTION \_ LEVEL                                                                                                                                       |
| Eingabedaten   | Der abzufragende Schutzmechanismus, der als 32-Bit-Ganzzahl angegeben wird. Der Wert wird als Member der [OPM-Schutztypflags](opm-protection-type-flags.md)interpretiert. |
| Daten zurückgeben  | Eine [**OPM \_ STANDARD \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                               |



 

## <a name="remarks"></a>Hinweise

Die globale Schutzebene ist die Schutzebene, die derzeit auf den Connector angewendet wird, unabhängig davon, wie der Grafiktreiber angewiesen wurde, den Schutz anzuwenden. Beispielsweise kann eine Anwendung die ACP-Schutzebene festlegen, indem sie die **ChangeDisplaySettingsEx-Funktion aufruft.** In diesem Fall würde die globale Schutzebene diese Einstellung widerspiegeln, obwohl sie nicht über den Ausgabeschutz-Manager (Output Protection Manager, OPM) angefordert wurde.

Die Schutzebene wird im **ulInformation-Member** der [**OPM \_ STANDARD \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) zurückgegeben. Die Bedeutung dieses Werts hängt vom abgefragten Schutzmechanismus ab. Für jeden Schutzmechanismus ist der Wert von **ulInformation** ein Flag aus einer anderen Enumeration, wie in der folgenden Tabelle dargestellt.



| Schutzmechanismus | Enumeration                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**OPM \_ ACP \_ PROTECTION \_ LEVEL**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [CGMS-A-Schutzflags](cgms-a-protection-flags.md)            |
| DPCP                 | [**OPM \_ DPCP \_ PROTECTION \_ LEVEL**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| Hdcp                 | [**OPM \_ HDCP \_ PROTECTION \_ LEVEL**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Diese Abfrage entspricht der \_ DXVA-Abfrage COPPQueryGlobalProtectionLevel, die im Certified Output Protection Protocol (COPP) verwendet wird.

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

 

 




