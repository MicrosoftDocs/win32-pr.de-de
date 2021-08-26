---
description: Gibt den physischen Connectortyp der Videoausgabe zurück.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3099da66193048b52011e58eb5ce3f925d451fc1ad26b193f2955f6012f0e607
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887500"
---
# <a name="opm_get_connector_type"></a>OPM \_ GET \_ CONNECTOR \_ TYPE

Gibt den physischen Connectortyp der Videoausgabe zurück.



| Anforderung | Wert |
|--------------|-----------------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ GET \_ CONNECTOR \_ TYPE                                                   |
| Eingabedaten   | Keine                                                                        |
| Daten zurückgeben  | Eine [**OPM \_ STANDARD \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Hinweise

Der Connectortyp wird im **ulInformation-Member** der [**OPM \_ STANDARD \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) zurückgegeben. Der Wert von **ulInformation** entspricht einem der Connectortypen, die unter [**OPM-Connectortypflags aufgeführt sind.**](opm-connector-type-flags.md)

Im COPP-Emulationsmodus kann der Connectortyp mit dem **OPM \_ COPP \_ COMPATIBLE CONNECTOR \_ TYPE \_ \_ INTERNAL-Flag kombiniert** werden. Verwenden Sie ein **bitweises AND,** um den Connectortyp zu extrahieren:

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

Anwendungen sollten das **FLAG OPM \_ COPP \_ COMPATIBLE CONNECTOR \_ \_ TYPE \_ INTERNAL** ignorieren. Weitere Informationen finden Sie im Abschnitt "Hinweise" von [**OPM-Connectortypflags.**](opm-connector-type-flags.md)

Diese Abfrage entspricht der \_ DXVA-Abfrage COPPQueryConnectorType, die im Certified Output Protection Protocol (COPP) verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                      |
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

 

 




