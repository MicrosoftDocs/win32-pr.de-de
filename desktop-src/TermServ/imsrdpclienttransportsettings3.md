---
title: IMsRdpClientTransportSettings3-Schnittstelle
description: Definiert zusätzliche Eigenschaften für den Remotedesktop Gatewayserver (RD-Gateway). | IMsRdpClientTransportSettings3-Schnittstelle
ms.assetid: c0bdfe23-9a26-4feb-b9b7-e52f04f23aa1
ms.tgt_platform: multiple
keywords:
- IMsRdpClientTransportSettings3-Schnittstelle Remotedesktopdienste
- IMsRdpClientTransportSettings3-Schnittstelle Remotedesktopdienste beschrieben
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
ms.openlocfilehash: 7a7680e27b0d67c9273e4f47da4725c0acab6d173c560bb5b288a30a96931d7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606925"
---
# <a name="imsrdpclienttransportsettings3-interface"></a>IMsRdpClientTransportSettings3-Schnittstelle

Definiert zusätzliche Eigenschaften für den Remotedesktop Gatewayserver (RD-Gateway).

## <a name="members"></a>Member

Die **IMsRdpClientTransportSettings3-Schnittstelle** erbt von [**IMsRdpClientTransportSettings2.**](imsrdpclienttransportsettings2.md) **IMsRdpClientTransportSettings3** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientTransportSettings3-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                           | Zugriffstyp           | BESCHREIBUNG                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GatewayAuthCookieServerAddr**](imsrdpclienttransportsettings3-gatewayauthcookieserveraddr.md)<br/>       | Lesen/Schreiben<br/> | Die Serveradresse für die cookiebasierte Authentifizierung.<br/>                                                                                       |
| [**GatewayAuthLoginPage**](imsrdpclienttransportsettings3-gatewayauthloginpage.md)<br/>                     | Lesen/Schreiben<br/> | Die Adresse der Anmeldewebseite, die zum Authentifizieren eines Benutzers verwendet werden soll.<br/>                                                                           |
| [**GatewayCredSourceCookie**](imsrdpclienttransportsettings3-gatewaycredsourcecookie.md)<br/>               | Lesen/Schreiben<br/> | Gibt an, ob die Anmeldeinformationsquelle cookiebasiert ist.<br/>                                                                                       |
| [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/>         | Lesen/Schreiben<br/> | Das verschlüsselte Authentifizierungscookie.<br/>                                                                                                      |
| [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)<br/> | Lesen/Schreiben<br/> | Die Größe der [**GatewayEncryptedAuthCookie-Eigenschaft**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) in Zeichen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                    |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings3 ist als 3D5B21AC-748D-41DE-8F30-E15169586BD4 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





