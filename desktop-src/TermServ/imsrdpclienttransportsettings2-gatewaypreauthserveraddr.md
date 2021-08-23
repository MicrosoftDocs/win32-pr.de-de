---
title: IMsRdpClientTransportSettings2 GatewayPreAuthServerAddr (Eigenschaft)
description: Gibt die Webadresse des Vorauthentifizierungsservers an oder ruft sie ab, die für das Einmalkennwortfeature des Remotedesktop-Gateways (RD-Gateway) verwendet wird.
ms.assetid: 14edad82-ab19-46fe-b878-d34298763c56
ms.tgt_platform: multiple
keywords:
- GatewayPreAuthServerAddr-Eigenschaft Remotedesktopdienste
- GatewayPreAuthServerAddr-Eigenschaft Remotedesktopdienste , IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2-Schnittstelle Remotedesktopdienste , GatewayPreAuthServerAddr (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.get_GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.put_GatewayPreAuthServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89fa3df8431f829c0dd85cd3a448965e98b4e6d5e6285ae75d18c76257ddbb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000910"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthserveraddr-property"></a>IMsRdpClientTransportSettings2::GatewayPreAuthServerAddr (Eigenschaft)

Gibt die Webadresse des Vorauthentifizierungsservers an oder ruft sie ab, die für das Einmalkennwortfeature des Remotedesktop-Gateways (RD-Gateway) verwendet wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayPreAuthServerAddr(
  [in]  BSTR bstrProxyPreAuthServerAddr
);

HRESULT get_GatewayPreAuthServerAddr(
  [out] BSTR *pbstrProxyPreAuthServerAddr
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Webadresse des Vorauthentifizierungsservers; Beispiel: die Webadresse des IsA-Servers (Microsoft Internet Security and Acceleration). Geben Sie die Webadresse im Format https://*Hostname an.* *DomainName*.com/*WebsiteName*" oder "https://*HostName*. *DomainName*.com/*WebsiteName*".

## <a name="error-codes"></a>Fehlercodes

Gibt **S \_ OK zurück,** wenn erfolgreich.

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
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





