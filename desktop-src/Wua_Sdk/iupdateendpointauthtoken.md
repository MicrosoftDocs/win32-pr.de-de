---
description: Stellt die Methoden bereit, die WUA zum Erfassen von Informationen über das Endpunkt Token verwenden kann.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: Iupdateendpointauthtoken-Schnittstelle (updateendpointauth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a5902b3c91b3ab12b311121bd7dcd8c415a68d6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485139"
---
# <a name="iupdateendpointauthtoken-interface"></a>Iupdateendpointauthtoken-Schnittstelle

Stellt die Methoden bereit, die WUA zum Erfassen von Informationen über das Endpunkt Token verwenden kann.

## <a name="members"></a>Member

Die **iupdateendpointauthtoken** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iupdateendpointauthtoken** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iupdateendpointauthtoken** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                | BESCHREIBUNG                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**ServiceID**](iupdateendpointauthtoken-serviceid.md)                               | Ruft den Bezeichner des Dienstanbieter ab, der authentifiziert werden soll.<br/>                                                          |
| [**SigningKey**](iupdateendpointauthtoken-signingkey.md)                             | Ruft den Schlüssel ab, der zum Signieren ausgehender Nachrichten zwischen dem Client Computer und dem Server verwendet wird.<br/>                        |
| [**Datenbankdaten**](iupdateendpointauthtoken-tokendata.md)                               | Ruft die XML-Daten (über das Netzwerk gesendet) ab, die das Token darstellen. <br/>                                               |
| [**"An ' referenceattached"**](iupdateendpointauthtoken-tokenreferenceattached.md)     | Ruft das XML-Format eines angefügten Verweises auf das Token ab.<br/>                                                       |
| [**"" Zu "".**](iupdateendpointauthtoken-tokenreferenceunattached.md) | Ruft das XML-Format eines nicht angefügten Verweises auf das Token ab.<br/>                                                     |
| [**TokenType**](iupdateendpointauthtoken-tokentype.md)                               | Ruft den Typ des Endpunkt Tokens ab, z. b. ein WS-Security SAML-Token (Security Assertion Markup Language) 1,1. <br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>                |
| Header<br/>                   | <dl> <dt>Updateendpointauth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Updateendpointauth. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Updateendpointauth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
