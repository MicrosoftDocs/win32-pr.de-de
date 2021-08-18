---
description: Gibt die Liste der Schutzmechanismen zurück, die vom Connector unterstützt werden.
ms.assetid: dd4cdd3c-6bb5-4427-827d-f3e909e752e5
title: OPM_GET_SUPPORTED_PROTECTION_TYPES (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eddc6f4006f9692ec6152875cda412191b87d247e907d33b615aa6d4fb89748e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012540"
---
# <a name="opm_get_supported_protection_types"></a>OPM \_ GET \_ SUPPORTED \_ PROTECTION \_ TYPES

Gibt die Liste der Schutzmechanismen zurück, die vom Connector unterstützt werden.



| Anforderung | Wert |
|--------------|-----------------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ GET \_ SUPPORTED \_ PROTECTION \_ TYPES                                      |
| Eingabedaten   | Keine                                                                        |
| Daten zurückgeben  | Eine [**OPM \_ STANDARD \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Hinweise

Die Schutzmechanismen werden im **ulInformation-Member** der [**OPM \_ STANDARD \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) zurückgegeben. Der Wert ist ein bitweises **OR** von [OPM-Schutztypflags.](opm-protection-type-flags.md)

Diese Abfrage entspricht der \_ DXVA-Abfrage COPPQueryProtectionType, die im Certified Output Protection Protocol (COPP) verwendet wird.

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

 

 




