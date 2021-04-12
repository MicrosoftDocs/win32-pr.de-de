---
description: 'Weitere Informationen finden Sie hier: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION'
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561a348588b1244a6763eb447affa2b330e9c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527884"
---
# <a name="opm_get_connected_hdcp_device_information"></a>OPM \_ get \_ Connected \_ HDCP- \_ Geräte \_ Informationen

Ruft Informationen zu einem HDCP-Gerät (High-Bandwidth Digital Content Protection) ab, das an die Videoausgabe angehängt ist. Die folgenden Informationen werden zurückgegeben:

-   Der HDCP Key Selection Vector (KSV) des Geräts.
-   Gibt an, ob das Gerät ein HDCP-Repeater ist.



| Anforderung | Wert |
|--------------|---------------------------------------------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ get \_ Connected \_ HDCP- \_ Geräte \_ Informationen                                                          |
| Eingabedaten   | Keine                                                                                                    |
| Daten zurückgeben  | Eine [**mit OPM \_ verbundene \_ HDCP- \_ Geräte \_ Informations**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) Struktur |



 

## <a name="remarks"></a>Bemerkungen

Diese Abfrage kann nur mit dem *COPP-Emulations Modus* verwendet werden. Wenn die [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Schnittstelle eine OPM-Semantik (Output Protection Manager) verwendet, wird diese Status Anforderung nicht unterstützt.

Der KSV ist ein Bezeichner, der dem Gerätehersteller zur Verfügung gestellt wird und im HDCP-Authentifizierungs-und-Setup Prozess verwendet wird. Im COPP-Emulations Modus verwendet die Anwendung den KSV, um zu bestimmen, ob das HDCP-Gerät gesperrt wird. Wenn dies der Fall ist, sollte die Anwendung geschützte Inhalte nicht wiedergeben. Außerdem sollte die Anwendung geschützte Inhalte nicht wiedergeben, wenn es sich bei dem Gerät um einen HDCP-Repeater handelt, da COPP HDCP-Repeaters nicht unterstützt.

Diese Abfrage wird bei Verwendung der OPM-Semantik nicht benötigt, da OPM die Geräte Sperrung und HDCP-Repeater unterstützt.

Diese Abfrage entspricht der DXVA- \_ Abfrage "coppqueryhdcpkeydata", die im Certified Output Protection Protocol (COPP) verwendet wird.

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

[OPM-Status Anforderungen](opm-status-requests.md)
</dt> </dl>

 

 




