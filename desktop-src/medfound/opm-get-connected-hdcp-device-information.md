---
description: 'Weitere Informationen finden Sie unter: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION'
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d692680e6492a3dc5d92073baf069eefffde68841925ced9afd69dde4d5fcd97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239893"
---
# <a name="opm_get_connected_hdcp_device_information"></a>OPM \_ GET \_ CONNECTED \_ HDCP \_ DEVICE \_ INFORMATION

Ruft Informationen zu einem High-Bandwidth Digital Content Protection(HDCP)-Gerät ab, das an die Videoausgabe angefügt ist. Die folgenden Informationen werden zurückgegeben:

-   Der HDCP-Schlüsselauswahlvektor (KSV) des Geräts.
-   Gibt an, ob es sich bei dem Gerät um einen HDCP-Repeater handelt.



| Anforderung | Wert |
|--------------|---------------------------------------------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ GET \_ CONNECTED \_ HDCP \_ DEVICE \_ INFORMATION                                                          |
| Eingabedaten   | Keine                                                                                                    |
| Daten zurückgeben  | Eine [**OPM \_ CONNECTED \_ HDCP DEVICE \_ \_ INFORMATION-Struktur**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) |



 

## <a name="remarks"></a>Hinweise

Diese Abfrage kann nur mit dem *COPP-Emulationsmodus verwendet werden.* Wenn die [**IOPMVideoOutput-Schnittstelle**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) die OPM-Semantik (Output Protection Manager) verwendet, wird diese Statusanforderung nicht unterstützt.

Die KSV ist ein Bezeichner, der dem Gerätehersteller bereitgestellt wird und bei der HDCP-Authentifizierung und -Einrichtung verwendet wird. Im COPP-Emulationsmodus verwendet die Anwendung die KSV, um zu bestimmen, ob das HDCP-Gerät widerrufen wird. Wenn dies der Dera ist, sollte die Anwendung keine geschützten Inhalte wieder geben. Außerdem sollte die Anwendung keine geschützten Inhalte wieder geben, wenn es sich bei dem Gerät um einen HDCP-Repeater handelt, da COPP keine HDCP-Repeater unterstützt.

Diese Abfrage ist nicht erforderlich, wenn OPM-Semantik verwendet wird, da OPM Gerätesperren und HDCP-Repeater unterstützt.

Diese Abfrage entspricht der \_ DXVA-Abfrage COPPQueryHDCPKeyData, die im Certified Output Protection Protocol (COPP) verwendet wird.

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

[OPM-Statusanforderungen](opm-status-requests.md)
</dt> </dl>

 

 




