---
title: IMsRdpClientTransportSettings2-GatewayCredSharing-Eigenschaft
description: Gibt die Einstellung an, mit der festgelegt wird, ob das Feature zum Freigeben von Anmeldeinformationen für Remotedesktop Gateway (RD-Gateway) aktiviert ist, oder ruft sie ab.
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- GatewayCredSharing-Eigenschaft Remotedesktopdienste
- GatewayCredSharing-Eigenschaft Remotedesktopdienste , IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2-Schnittstelle Remotedesktopdienste , GatewayCredSharing-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayCredSharing
- IMsRdpClientTransportSettings2.get_GatewayCredSharing
- IMsRdpClientTransportSettings2.put_GatewayCredSharing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d489678006e842a6da82f5d2f9489f84a9a20fd70bfe8f18018aaa6d412c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974650"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a>IMsRdpClientTransportSettings2::GatewayCredSharing-Eigenschaft

Gibt die Einstellung an, mit der festgelegt wird, ob das Feature zum Freigeben von Anmeldeinformationen für Remotedesktop Gateway (RD-Gateway) aktiviert ist, oder ruft sie ab. Wenn das Feature aktiviert ist, versucht das Remotedesktop ActiveX-Steuerelement, die gleichen Anmeldeinformationen für die Authentifizierung beim Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) und beim RD-Gatewayserver zu verwenden.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayCredSharing(
  [in]  ULONG ulProxyCredSharing
);

HRESULT get_GatewayCredSharing(
  [out] ULONG *pulProxyCredSharing
);
```



## <a name="property-value"></a>Eigenschaftswert

Wenn diese Einstellung auf 1 festgelegt ist, ist die Freigabe von Anmeldeinformationen aktiviert. Wenn null festgelegt ist, ist die Freigabe von Anmeldeinformationen deaktiviert.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird vom ActiveX-Steuerelement verwendet, um eine einzelne Eingabeaufforderung für die Freigabe von Anmeldeinformationen zwischen dem RD-Sitzungshost-Server und dem RD-Gatewayserver zu implementieren. Die Freigabe von Anmeldeinformationen unterstützt keine webbasierte Kennwortfreigabe mit [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) oder [**ClearTextPassword.**](imstscnonscriptable-cleartextpassword.md)

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

 

 





