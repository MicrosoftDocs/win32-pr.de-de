---
description: Gibt den eindeutigen Bezeichner des Monitors zurück, der mit dieser Videoausgabe verknüpft ist.
ms.assetid: d34d68ff-c513-483e-8619-4a9baa2a40ba
title: OPM_GET_OUTPUT_ID (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6146c07be3467e513b33f636bde78e699f3e0d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347031"
---
# <a name="opm_get_output_id"></a>OPM \_ - \_ Ausgabe- \_ ID erhalten

Gibt den eindeutigen Bezeichner des Monitors zurück, der mit dieser Videoausgabe verknüpft ist.



| Anforderung | Wert |
|--------------|------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ - \_ Ausgabe- \_ ID erhalten                                             |
| Eingabedaten   | Keine                                                             |
| Daten zurückgeben  | Eine [**OPM- \_ Ausgabe- \_ ID- \_ Daten**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data) Struktur |



 

## <a name="remarks"></a>Bemerkungen

Der Videotreiber weist jedem Monitor einen eindeutigen Bezeichner zu. Diese Abfrage gibt den Bezeichner für den Monitor zurück, der dem aktuellen [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Zeiger zugeordnet ist.

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

 

 




