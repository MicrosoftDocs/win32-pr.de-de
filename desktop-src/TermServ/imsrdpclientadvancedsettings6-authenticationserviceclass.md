---
title: IMsRdpClientAdvancedSettings6 AuthenticationServiceClass-Eigenschaft
description: Gibt den Dienstprinzipalnamen (Service Principal Name, SPN) an, der für die Authentifizierung beim Server verwendet werden soll.
ms.assetid: 65d10b1f-295a-44b8-a790-306ae4e3e5e2
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der AuthenticationServiceClass-Eigenschaft
- AuthenticationServiceClass-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , AuthenticationServiceClass-Eigenschaft
- AuthenticationServiceClass-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , AuthenticationServiceClass-Eigenschaft
- AuthenticationServiceClass-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , AuthenticationServiceClass-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.put_AuthenticationServiceClass
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8453c0aef1548303e653f1ba57c9f05550975d93706eae1b9d3f05ea0b611a71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001368"
---
# <a name="imsrdpclientadvancedsettings6authenticationserviceclass-property"></a>IMsRdpClientAdvancedSettings6::AuthenticationServiceClass-Eigenschaft

Gibt den Dienstprinzipalnamen (Service Principal Name, SPN) an, der für die Authentifizierung beim Server verwendet werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AuthenticationServiceClass(
  [in]          BSTR bstrAuthServiceClass
);

HRESULT get_AuthenticationServiceClass(
  [out, retval] BSTR *pbstrAuthServiceClass
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt den zu verwendenden Dienstprinzipalnamen an.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird nur von Remotedesktopverbindung 6.1- und 7.0-Clients unterstützt.

Dienstprinzipalnamen (SPNs) sind dem Sicherheitsprinzipal (Benutzer oder Gruppen) zugeordnet, in dessen Sicherheitskontext der Dienst ausgeführt wird. SPNs werden verwendet, um die gegenseitige Authentifizierung zwischen einer Clientanwendung und einem Dienst zu unterstützen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





