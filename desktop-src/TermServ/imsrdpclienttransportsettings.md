---
title: Imsrdpclienttransportsettings-Schnittstelle
description: Verwaltet die Client Transport Einstellungen für den Remotedesktop Gateway-Server (RD-Gateway). | Imsrdpclienttransportsettings-Schnittstelle
ms.assetid: d2573727-1dcc-4d4d-af5c-038e9467ba84
ms.tgt_platform: multiple
keywords:
- Imsrdpclienttransportsettings-Schnittstelle Remotedesktopdienste
- Imsrdpclienttransportsettings-Schnittstelle Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: ec240d008ef2f9469fb67f4041cfb33c08383079
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350612"
---
# <a name="imsrdpclienttransportsettings-interface"></a>Imsrdpclienttransportsettings-Schnittstelle

Verwaltet die Client Transport Einstellungen für den Remotedesktop Gateway-Server (RD-Gateway).

## <a name="members"></a>Member

Die **imsrdpclienttransportsettings** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Imsrdpclienttransportsettings** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **imsrdpclienttransportsettings** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                          | Zugriffstyp           | BESCHREIBUNG                                                 |
|:------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [**Gatewaykredssource**](imsrdpclienttransportsettings-gatewaycredssource.md)<br/>                         | Lesen/Schreiben<br/> | Die RD-Gateway Server-Authentifizierungsmethode.<br/>     |
| [**Gatewaydefaultusagemethod**](imsrdpclienttransportsettings-gatewaydefaultusagemethod.md)<br/>           | Schreibgeschützt<br/>  | Die Standard-RD-Gateway Verwendungs Methode.<br/>             |
| [**Gatewayhostname**](imsrdpclienttransportsettings-gatewayhostname.md)<br/>                               | Lesen/Schreiben<br/> | Der Hostname des RD-Gateway Servers.<br/>              |
| [**Gatewayissupported**](imsrdpclienttransportsettings-gatewayissupported.md)<br/>                         | Schreibgeschützt<br/>  | Gibt an, ob RD-Gateway unterstützt wird.<br/>       |
| [**Gatewayprofileusagemethod**](imsrdpclienttransportsettings-gatewayprofileusagemethod.md)<br/>           | Lesen/Schreiben<br/> | Die RD-Gateway Profil Verwendungs Methode.<br/>             |
| [**GatewayUsageMethod**](imsrdpclienttransportsettings-gatewayusagemethod.md)<br/>                         | Lesen/Schreiben<br/> | Die RD-Gateway Server-Verwendungs Methode.<br/>              |
| [**Gatewayuserselectedkredssource**](imsrdpclienttransportsettings-gatewayuserselectedcredssource.md)<br/> | Lesen/Schreiben<br/> | Der benutzerdefinierte RD-Gateway Anmelde Informationsquelle.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ imsrdpclienttransportsettings ist definiert als 720298c0-A099-46f 5-9F 82-96921bae4701<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

