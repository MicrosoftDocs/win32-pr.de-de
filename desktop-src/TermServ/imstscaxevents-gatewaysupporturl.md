---
title: IMsRdpClientTransportSettings2 GatewaySupportUrl-Eigenschaft
description: Gibt die Webadresse der Website an, die technischen Support für diesen Remotedesktop Gatewayserver (RD Gateway) bereitstellt, oder ruft sie ab.
ms.assetid: e9c0f5ec-1b2f-4e09-8169-4316fd394443
ms.tgt_platform: multiple
keywords:
- GatewaySupportUrl-Eigenschaft Remotedesktopdienste
- GatewaySupportUrl-Eigenschaft Remotedesktopdienste , IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2-Schnittstelle Remotedesktopdienste , GatewaySupportUrl-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewaySupportUrl
- IMsRdpClientTransportSettings2.get_GatewaySupportUrl
- IMsRdpClientTransportSettings2.put_GatewaySupportUrl
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2833962f66fb6fab2597629877c5990c9234eb5b2dfe076073bedc2ceab9fd65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770690"
---
# <a name="imsrdpclienttransportsettings2gatewaysupporturl-property"></a>IMsRdpClientTransportSettings2::GatewaySupportUrl-Eigenschaft

Gibt die Webadresse der Website an, die technischen Support für diesen Remotedesktop Gatewayserver (RD Gateway) bereitstellt, oder ruft sie ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewaySupportUrl(
  [in]  BSTR bstrProxySupportUrl
);

HRESULT get_GatewaySupportUrl(
  [out] BSTR *pbstrProxySupportUrl
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt die Webadresse der Website an, die technischen Support für diesen RD-Gatewayserver bereitstellt, oder ruft sie ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista mit SP1<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                    |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 ist als 67341688-D606-4c73-A5D2-2E0489009319 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





