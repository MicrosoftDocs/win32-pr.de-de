---
title: Imsrdpclienttransportsettings (gatewayissupported-Eigenschaft)
description: Gibt an, ob Remotedesktop Gateway (RD-Gateway) unterstützt wird.
ms.assetid: 31edd35b-251d-404d-bec8-e082bb2427b3
ms.tgt_platform: multiple
keywords:
- Gatewayissupported-Eigenschaft Remotedesktopdienste
- Gatewayissupported-Eigenschaft Remotedesktopdienste, imsrdpclienttransportsettings-Schnittstelle
- Imsrdpclienttransportsettings-Schnittstelle Remotedesktopdienste, gatewayissupported-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayIsSupported
- IMsRdpClientTransportSettings.get_GatewayIsSupported
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de79033c2ab9bae73aae4213e72a54590170a184
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391525"
---
# <a name="imsrdpclienttransportsettingsgatewayissupported-property"></a>Imsrdpclienttransportsettings:: gatewayissupported-Eigenschaft

Gibt an, ob Remotedesktop Gateway (RD-Gateway) unterstützt wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_GatewayIsSupported(
  [out] BOOL *pfProxyIsSupported
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt an, ob RD-Gateway unterstützt wird.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ imsrdpclienttransportsettings ist definiert als 720298c0-A099-46f 5-9F 82-96921bae4701<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclienttransportsettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





