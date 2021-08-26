---
title: IMsRdpClientTransportSettings-Eigenschaft "GatewayHostname"
description: Gibt den Hostnamen des Remotedesktop Gatewayservers (RD-Gateway) an.
ms.assetid: 34c4b3b7-3768-4d98-b1e8-7fcb8f9c758d
ms.tgt_platform: multiple
keywords:
- GatewayHostname-Eigenschaft Remotedesktopdienste
- GatewayHostname-Eigenschaft Remotedesktopdienste , IMsRdpClientTransportSettings-Schnittstelle
- IMsRdpClientTransportSettings-Schnittstelle Remotedesktopdienste , GatewayHostname-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayHostname
- IMsRdpClientTransportSettings.get_GatewayHostname
- IMsRdpClientTransportSettings.put_GatewayHostname
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de618d31f4d0989ebce319260f0afe4548d658e3c28891a9d26dad0580d62452
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870840"
---
# <a name="imsrdpclienttransportsettingsgatewayhostname-property"></a>IMsRdpClientTransportSettings::GatewayHostname-Eigenschaft

Gibt den Hostnamen des Remotedesktop Gatewayservers (RD-Gateway) an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayHostname(
  [in]  BSTR newVal
);

HRESULT get_GatewayHostname(
  [out] BSTR *pProxyHostname
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die den Hostnamen des RD-Gatewayservers enthält.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings ist als 720298C0-A099-46f5-9F82-96921BAE4701 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





