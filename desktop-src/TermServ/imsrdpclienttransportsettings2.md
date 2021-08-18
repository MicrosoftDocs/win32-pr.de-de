---
title: IMsRdpClientTransportSettings2-Schnittstelle
description: Verwaltet Clienttransporteinstellungen für den Remotedesktop Gatewayserver (RD Gateway). | IMsRdpClientTransportSettings2-Schnittstelle
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- IMsRdpClientTransportSettings2-Schnittstelle Remotedesktopdienste
- IMsRdpClientTransportSettings2-Schnittstelle Remotedesktopdienste beschrieben
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
ms.openlocfilehash: 479fdceee0a1fc168725ef9b5acccb471e1b32b8c13a0e0ff6b12096f14ff0ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000950"
---
# <a name="imsrdpclienttransportsettings2-interface"></a>IMsRdpClientTransportSettings2-Schnittstelle

Verwaltet Clienttransporteinstellungen für den Remotedesktop Gatewayserver (RD Gateway).

## <a name="members"></a>Member

Die **IMsRdpClientTransportSettings2-Schnittstelle** erbt von [**IMsRdpClientTransportSettings.**](imsrdpclienttransportsettings.md) **IMsRdpClientTransportSettings2** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientTransportSettings2-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                    | Zugriffstyp           | BESCHREIBUNG                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [**GatewayCredSharing**](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | Lesen/Schreiben<br/> | Gibt an, ob das Feature für einmaliges Anmelden für RD-Gateway aktiviert ist.<br/>                |
| [**GatewayDomain**](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | Lesen/Schreiben<br/> | Der Domänenname, den ein Benutzer bereitstellt, um eine Verbindung mit dem RD-Gatewayserver herzustellen.<br/>              |
| [**GatewayEncryptedOtpCookie**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | Lesen/Schreiben<br/> | Das verschlüsselte OTP-Cookie.<br/>                                                              |
| [**GatewayEncryptedOtpCookieSize**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | Lesen/Schreiben<br/> | Die Größe des verschlüsselten OTP-Cookies in Bytes.<br/>                                       |
| [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | Lesegeschützt<br/> | Das Kennwort, das ein Benutzer bereitstellt, um eine Verbindung mit dem RD-Gatewayserver herzustellen.<br/>                 |
| [**GatewayPreAuthRequirement**](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | Lesen/Schreiben<br/> | Gibt an, ob die Funktion für das RD-Gateway-Einmalkennwort (One-Time Password, OTP) aktiviert ist.<br/>           |
| [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | Lesen/Schreiben<br/> | Die Webadresse des Vorauthentifizierungsservers.<br/>                                      |
| [**GatewaySupportUrl**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | Lesen/Schreiben<br/> | Die Webadresse der Website, die technischen Support für den RD-Gatewayserver bereitstellt.<br/> |
| [**GatewayUsername**](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | Lesen/Schreiben<br/> | Der Benutzername, den ein Benutzer bereitstellt, um eine Verbindung mit dem RD-Gatewayserver herzustellen.<br/>                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista mit SP1<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                    |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 ist als 67341688-D606-4c73-A5D2-2E0489009319 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





