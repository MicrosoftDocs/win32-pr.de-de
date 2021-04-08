---
title: IMsRdpClientTransportSettings3-Schnittstelle
description: Definiert zusätzliche Eigenschaften für den Remotedesktop Gateway-Server (RD-Gateway). | IMsRdpClientTransportSettings3-Schnittstelle
ms.assetid: c0bdfe23-9a26-4feb-b9b7-e52f04f23aa1
ms.tgt_platform: multiple
keywords:
- IMsRdpClientTransportSettings3-Schnittstelle Remotedesktopdienste
- IMsRdpClientTransportSettings3 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7498db4b39a4ad0e89761cbec439895e4e9a152
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869755"
---
# <a name="imsrdpclienttransportsettings3-interface"></a>IMsRdpClientTransportSettings3-Schnittstelle

Definiert zusätzliche Eigenschaften für den Remotedesktop Gateway-Server (RD-Gateway).

## <a name="members"></a>Member

Die **IMsRdpClientTransportSettings3** -Schnittstelle erbt von [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md). **IMsRdpClientTransportSettings3** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientTransportSettings3** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                           | Zugriffstyp           | BESCHREIBUNG                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Gatewayauthcookieserveraddr**](imsrdpclienttransportsettings3-gatewayauthcookieserveraddr.md)<br/>       | Lesen/Schreiben<br/> | Die Server Adresse für die cookiebasierte Authentifizierung.<br/>                                                                                       |
| [**Gatewayauthloginpage**](imsrdpclienttransportsettings3-gatewayauthloginpage.md)<br/>                     | Lesen/Schreiben<br/> | Die Adresse der Anmelde Webseite, die zum Authentifizieren eines Benutzers verwendet werden soll.<br/>                                                                           |
| [**Gatewaykredsourcecookie**](imsrdpclienttransportsettings3-gatewaycredsourcecookie.md)<br/>               | Lesen/Schreiben<br/> | Gibt an, ob die Anmelde Informationsquelle cookiebasiert ist.<br/>                                                                                       |
| [**Gatewayverschlüsseltedauthcookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/>         | Lesen/Schreiben<br/> | Das verschlüsselte Authentifizierungs Cookie.<br/>                                                                                                      |
| [**Gatewayverschlüsseltedauthcookiesize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)<br/> | Lesen/Schreiben<br/> | Die Größe der [**gatewayverschlüsseltedauthcookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) -Eigenschaft in Zeichen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                    |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings3 ist als 3d5b21ac-748d-41to-8l30e15169586bd4 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





