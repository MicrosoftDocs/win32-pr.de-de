---
description: Stellt die Methoden zur Verfügung, mit denen WUA Informationen zum Endpunkttoken sammeln kann.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: IUpdateEndpointAuthToken-Schnittstelle (UpdateEndpointAuth.h)
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
ms.openlocfilehash: 7b5afa1e9039b7f210dfbf71c8bceff4a7b438b413844a7a7e55dec0fd9fea8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855760"
---
# <a name="iupdateendpointauthtoken-interface"></a>IUpdateEndpointAuthToken-Schnittstelle

Stellt die Methoden zur Verfügung, mit denen WUA Informationen zum Endpunkttoken sammeln kann.

## <a name="members"></a>Member

Die **IUpdateEndpointAuthToken-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IUpdateEndpointAuthToken** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IUpdateEndpointAuthToken-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                | Beschreibung                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**ServiceID**](iupdateendpointauthtoken-serviceid.md)                               | Ruft den Bezeichner des diensts ab, der authentifiziert werden soll.<br/>                                                          |
| [**SigningKey**](iupdateendpointauthtoken-signingkey.md)                             | Ruft den Schlüssel ab, der zum Signieren ausgehender Nachrichten zwischen dem Clientcomputer und dem Gerät verwendet wird.<br/>                        |
| [**TokenData**](iupdateendpointauthtoken-tokendata.md)                               | Ruft die (über das Netzwerk gesendeten) XML-Daten ab, die das Token darstellt. <br/>                                               |
| [**TokenReferenceAttached**](iupdateendpointauthtoken-tokenreferenceattached.md)     | Ruft das XML-Format eines angefügten Verweises auf das Token ab.<br/>                                                       |
| [**TokenReferenceUnattached**](iupdateendpointauthtoken-tokenreferenceunattached.md) | Ruft das XML-Format eines nicht angefügten Verweises auf das Token ab.<br/>                                                     |
| [**Tokentype**](iupdateendpointauthtoken-tokentype.md)                               | Ruft den Typ des Endpunkttokens ab, z. B. ein WS-Security SAML (Security Assertion Markup Language) 1.1-Token. <br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>                |
| Header<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
