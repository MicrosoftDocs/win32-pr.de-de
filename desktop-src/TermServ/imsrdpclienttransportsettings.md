---
title: IMsRdpClientTransportSettings-Schnittstelle
description: Verwaltet Clienttransporteinstellungen für den Remotedesktop Gateway-Server (RD-Gateway). | IMsRdpClientTransportSettings-Schnittstelle
ms.assetid: d2573727-1dcc-4d4d-af5c-038e9467ba84
ms.tgt_platform: multiple
keywords:
- IMsRdpClientTransportSettings-Schnittstelle Remotedesktopdienste
- IMsRdpClientTransportSettings-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edd2cbcdaba0a4324c4501339e972f8bb967f64716d1688cef7c3c38bb22b5b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771450"
---
# <a name="imsrdpclienttransportsettings-interface"></a>IMsRdpClientTransportSettings-Schnittstelle

Verwaltet Clienttransporteinstellungen für den Remotedesktop Gateway-Server (RD-Gateway).

## <a name="members"></a>Member

Die **IMsRdpClientTransportSettings-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IMsRdpClientTransportSettings** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientTransportSettings-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                          | Zugriffstyp           | Beschreibung                                                 |
|:------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [**GatewayCredsSource**](imsrdpclienttransportsettings-gatewaycredssource.md)<br/>                         | Lesen/Schreiben<br/> | Die Rd-Gateway-Serverauthentifizierungsmethode.<br/>     |
| [**GatewayDefaultUsageMethod**](imsrdpclienttransportsettings-gatewaydefaultusagemethod.md)<br/>           | Schreibgeschützt<br/>  | Die Standardmäßige RD-Gateway-Verwendungsmethode.<br/>             |
| [**GatewayHostname**](imsrdpclienttransportsettings-gatewayhostname.md)<br/>                               | Lesen/Schreiben<br/> | Hostname des RD-Gatewayservers.<br/>              |
| [**GatewayIsSupported**](imsrdpclienttransportsettings-gatewayissupported.md)<br/>                         | Schreibgeschützt<br/>  | Gibt an, ob das RD-Gateway unterstützt wird.<br/>       |
| [**GatewayProfileUsageMethod**](imsrdpclienttransportsettings-gatewayprofileusagemethod.md)<br/>           | Lesen/Schreiben<br/> | Die Rd-Gateway-Profilverwendungsmethode.<br/>             |
| [**GatewayUsageMethod**](imsrdpclienttransportsettings-gatewayusagemethod.md)<br/>                         | Lesen/Schreiben<br/> | Die Rd-Gateway-Serververwendungsmethode.<br/>              |
| [**GatewayUserSelectedCredsSource**](imsrdpclienttransportsettings-gatewayuserselectedcredssource.md)<br/> | Lesen/Schreiben<br/> | Die vom Benutzer angegebene Rd-Gateway-Anmeldeinformationsquelle.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings ist als 720298C0-A099-46f5-9F82-96921BAE4701 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Remotedesktop-Webverbindung-Referenz](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

