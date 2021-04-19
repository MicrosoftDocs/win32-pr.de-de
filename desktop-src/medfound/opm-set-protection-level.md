---
description: Legt die Schutz Ebene für einen ausgabeschutzmechanismus fest.
ms.assetid: f4e63bf5-0749-4054-9f86-7fd88f2881ad
title: OPM_SET_PROTECTION_LEVEL (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a80fb674c9347dafc3bcf1a62dc4bc909f0471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348259"
---
# <a name="opm_set_protection_level"></a>OPM \_ - \_ Schutz \_ Ebene festlegen

Legt die Schutz Ebene für einen ausgabeschutzmechanismus fest.



| Anforderung | Wert |
|--------------|-----------------------------------------------------------------------------------------------------|
| Befehls-GUID | OPM \_ - \_ Schutz \_ Ebene festlegen                                                                         |
| Eingabedaten   | Eine [**OPM-Parameter Struktur zum \_ Festlegen der \_ Schutz \_ Ebenen \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) |



 

## <a name="remarks"></a>Bemerkungen

Einige Connectors können mehrere Schutzmechanismen unterstützen. Mit diesem Verbindungstyp können Sie mehrere Schutzmechanismen auf denselben Connector anwenden, wobei jeweils jeweils jeweils eine Einstellung unterschiedlich ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[OPM-Befehle](opm-commands.md)
</dt> </dl>

 

 




