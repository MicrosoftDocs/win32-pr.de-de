---
description: Fragt ab, ob ein DVI-Connector (Digital Video Interface) die DVI-Version 1,1 oder höher unterstützt.
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: OPM_GET_DVI_CHARACTERISTICS (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6f996b0397db509a45af6e243359c581df333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041901"
---
# <a name="opm_get_dvi_characteristics"></a>OPM- \_ get- \_ DVI- \_ Merkmale

Fragt ab, ob ein DVI-Connector (Digital Video Interface) die DVI-Version 1,1 oder höher unterstützt.



| Anforderung | Wert |
|--------------|-----------------------------------------------------------------------------|
| Anforderungs-GUID | OPM- \_ get- \_ DVI- \_ Merkmale                                              |
| Eingabedaten   | Keine                                                                        |
| Daten zurückgeben  | Eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur |



 

## <a name="remarks"></a>Bemerkungen

Wenn diese Abfrage erfolgreich ist, enthält der **ulinformation** -Member der [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur einen der folgenden Werte.



| Wert                                     | BESCHREIBUNG               |
|-------------------------------------------|---------------------------|
| OPM- \_ DVI- \_ Merkmal \_ 1 \_ 0            | DVI-Version 1,0.          |
| OPM- \_ DVI- \_ Merkmal \_ 1 \_ 1 \_ oder \_ höher | DVI-Version 1,1 oder höher. |



 

Diese Abfrage wird nur unterstützt, wenn der Typ des physischen Connector der OPM- \_ Connector ist \_ \_ . Um den Verbindungstyp zu erhalten, senden Sie die Abfrage " [**OPM \_ get \_ Connector \_ Type**](opm-get-connector-type.md) ".

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

 

 




