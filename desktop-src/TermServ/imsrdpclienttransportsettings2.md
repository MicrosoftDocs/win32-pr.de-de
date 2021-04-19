---
title: IMsRdpClientTransportSettings2-Schnittstelle
description: Verwaltet die Client Transport Einstellungen für den Remotedesktop Gateway-Server (RD-Gateway). | IMsRdpClientTransportSettings2-Schnittstelle
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- IMsRdpClientTransportSettings2-Schnittstelle Remotedesktopdienste
- IMsRdpClientTransportSettings2 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f2f4887c6a4f55f3b9c97c389e9afd702d2ffab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366581"
---
# <a name="imsrdpclienttransportsettings2-interface"></a>IMsRdpClientTransportSettings2-Schnittstelle

Verwaltet die Client Transport Einstellungen für den Remotedesktop Gateway-Server (RD-Gateway).

## <a name="members"></a>Member

Die **IMsRdpClientTransportSettings2** -Schnittstelle erbt von [**imsrdpclienttransportsettings**](imsrdpclienttransportsettings.md). **IMsRdpClientTransportSettings2** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientTransportSettings2** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                    | Zugriffstyp           | BESCHREIBUNG                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [**Gatewaykredsharing**](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | Lesen/Schreiben<br/> | Gibt an, ob das Single Sign-On Feature für RD-Gateway aktiviert ist.<br/>                |
| [**Gatewaydomain**](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | Lesen/Schreiben<br/> | Der Domänen Name, der von einem Benutzer zum Herstellen einer Verbindung mit dem RD-Gateway Server bereitstellt.<br/>              |
| [**Gatewayverschlüsseltedotpcookie**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | Lesen/Schreiben<br/> | Das verschlüsselte OTP-Cookie.<br/>                                                              |
| [**Gatewayverschlüsseltedotpcookiesize**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | Lesen/Schreiben<br/> | Die Größe des verschlüsselten OTP-Cookies in Bytes.<br/>                                       |
| [**Gatewaypassword**](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | Lesegeschützt<br/> | Das Kennwort, das ein Benutzer zum Herstellen einer Verbindung mit dem RD-Gateway-Server bereitstellt.<br/>                 |
| [**Gatewaypreauthrequirement**](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | Lesen/Schreiben<br/> | Gibt an, ob das RD-Gateway Feature für einmal Kennwort (One-time password, OTP) aktiviert ist.<br/>           |
| [**Gatewaypreauthserveraddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | Lesen/Schreiben<br/> | Die Webadresse des Servers, der vor der Authentifizierung steht.<br/>                                      |
| [**Gatewaysupporturl**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | Lesen/Schreiben<br/> | Die Webadresse der Website, die technischen Support für den RD-Gateway Server bereitstellt.<br/> |
| [**Gatewayusername**](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | Lesen/Schreiben<br/> | Der Benutzername, den ein Benutzer zum Herstellen einer Verbindung mit dem RD-Gateway Server bereitstellt.<br/>                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista mit SP1<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                    |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 ist als 67341688-D606-4c73-A5D2-2e0489009319 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclienttransportsettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





