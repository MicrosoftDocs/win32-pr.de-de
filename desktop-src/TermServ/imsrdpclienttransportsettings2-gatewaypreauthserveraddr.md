---
title: IMsRdpClientTransportSettings2 gatewaypreauthserveraddr (Eigenschaft)
description: Gibt die Webadresse des Servers für die Vorauthentifizierung an, der für das einmalige Kennwort (RD-Gateway) von Remotedesktop Gateway verwendet wird, oder ruft Sie ab.
ms.assetid: 14edad82-ab19-46fe-b878-d34298763c56
ms.tgt_platform: multiple
keywords:
- Gatewaypreauthserveraddr-Eigenschaft Remotedesktopdienste
- Gatewaypreauthserveraddr-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2 Interface Remotedesktopdienste, gatewaypreauthserveraddr (Eigenschaft)
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
ms.openlocfilehash: 95d6fe2f397b0d445a6300d68a89b210debd449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391665"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthserveraddr-property"></a>IMsRdpClientTransportSettings2:: gatewaypreauthserveraddr (Eigenschaft)

Gibt die Webadresse des Servers für die Vorauthentifizierung an, der für das einmalige Kennwort (RD-Gateway) von Remotedesktop Gateway verwendet wird, oder ruft Sie ab.

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

Die Webadresse des Servers, der vor der Authentifizierung verwendet wird. beispielsweise die Webadresse des Microsoft Internet Security and Acceleration (ISA)-Servers. Geben Sie die Webadresse im Format "https://*Hostname*" an. *Domain Name*. com/*Websitename*"oder" https://*Hostname*. *Domain Name*. com/*Websitename*".

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

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
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





