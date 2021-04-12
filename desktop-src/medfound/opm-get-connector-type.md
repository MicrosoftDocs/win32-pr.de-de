---
description: Gibt den physischen Verbindungstyp der Videoausgabe zurück.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a95ca88b079aa93b4c2665fe7aa954eb58cfc1a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215027"
---
# <a name="opm_get_connector_type"></a>OPM \_ get \_ Connector- \_ Typ

Gibt den physischen Verbindungstyp der Videoausgabe zurück.



| Anforderung | Wert |
|--------------|-----------------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ get \_ Connector- \_ Typ                                                   |
| Eingabedaten   | Keine                                                                        |
| Daten zurückgeben  | Eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur |



 

## <a name="remarks"></a>Bemerkungen

Der Verbindungstyp wird im **ulinformation** -Member der [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur zurückgegeben. Der Wert von **ulinformation** ist gleich einem der Connector-Typen, die in [**OPM-Connector-Typflags**](opm-connector-type-flags.md)aufgeführt sind.

Im COPP-Emulations Modus kann der Verbindungstyp mit dem **internen OPM- \_ \_ \_ \_ Kopiertyp \_** -Flag kombiniert werden. Verwenden Sie ein bitweises **and-** Element, um den Verbindungstyp zu extrahieren:

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

Anwendungen sollten das interne Flag " **OPM \_ COPP \_ Compatible \_ Connector \_ Type \_** " ignorieren. Weitere Informationen finden Sie im Abschnitt "Hinweise" der [**OPM-Connector-Typflags**](opm-connector-type-flags.md).

Diese Abfrage entspricht der DXVA- \_ Abfrage "coppqueryconnector Type", die im Certified Output Protection Protocol (COPP) verwendet wird.

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

 

 




