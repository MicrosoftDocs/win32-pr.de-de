---
description: Enthält die Methoden, die zum Aushandeln des Tokentyps verwendet werden, um den Endpunkt eines Diensts zu authentifizieren.
ms.assetid: F6177B24-C166-4BEC-83D6-3AD5B5B3CF08
title: IUpdateEndpointAuthProvider-Schnittstelle (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 3cbc51ab0f1192e20612829532b907e3644a7da3f99fdedd8e3dbd45a780c54d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994570"
---
# <a name="iupdateendpointauthprovider-interface"></a>IUpdateEndpointAuthProvider-Schnittstelle

Die **IUpdateEndpointAuthProvider-Schnittstelle** enthält die Methoden, die zum Aushandeln des Tokentyps für die Authentifizierung des Endpunkts eines Diensts verwendet werden.

## <a name="members"></a>Member

Die **IUpdateEndpointAuthProvider-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IUpdateEndpointAuthProvider** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IUpdateEndpointAuthProvider-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                             | Beschreibung                                                                                    |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)                           | Fordern Sie mit den angegebenen Anmeldeinformationen ein Token für den Endpunkt des Diensts an.<br/>    |
| [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) | Gibt den bevorzugten Authentifizierungstokentyp für den Endpunkt des Diensts zurück.<br/> |



 

## <a name="remarks"></a>Hinweise

WUA ruft die [**GetPreferredEndpointTokenType-Methode**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) dieser Schnittstelle auf, um den Aushandlungsprozess zu starten. Wenn der Aufruf erfolgt, übergibt WUA den Dienstbezeichner, den Typ des vom Dienst implementierten Endpunkts und die verfügbaren Tokentypen. Die Implementierung dieser Schnittstelle gibt dann die Tokentypen zurück, die sie bevorzugt verwenden möchte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>                |
| Header<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
