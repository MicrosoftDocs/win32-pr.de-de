---
title: IMsRdpClientTransportSettings2 gatewaykredsharing (Eigenschaft)
description: Gibt die Einstellung an, ob das Feature für die Freigabe von Anmelde Informationen für das Remotedesktop Gateway (RD-Gateway) aktiviert ist, oder ruft Sie ab.
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- Gatewaykredsharing-Eigenschaft Remotedesktopdienste
- Gatewaykredsharing-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2 Interface Remotedesktopdienste, gatewaykredsharing (Eigenschaft)
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
ms.openlocfilehash: 329e425631b674e050f246c4105115bd4326be3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475627"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a>IMsRdpClientTransportSettings2:: gatewaykredsharing (Eigenschaft)

Gibt die Einstellung an, ob das Feature für die Freigabe von Anmelde Informationen für das Remotedesktop Gateway (RD-Gateway) aktiviert ist, oder ruft Sie ab. Wenn das Feature aktiviert ist, versucht das Remotedesktop ActiveX-Steuerelement, die gleichen Anmelde Informationen für die Authentifizierung beim Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server und beim RD-Gateway Server zu verwenden.

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

Wenn Sie auf 1 festgelegt ist, ist die Freigabe von Anmelde Informationen aktiviert. Wenn der Wert auf NULL festgelegt ist, ist die Freigabe von Anmelde Informationen deaktiviert

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird vom ActiveX-Steuerelement verwendet, um eine einzelne Eingabeaufforderung für die Freigabe von Anmelde Informationen zwischen dem RD-Sitzungshost Server und dem RD-Gateway Server zu implementieren. Die Freigabe von Anmelde Informationen unterstützt keine webbasierte Kenn Wort Freigabe mit [**gatewaypassword**](imsrdpclienttransportsettings2-gatewaypassword.md) oder [**cleartextpassword**](imstscnonscriptable-cleartextpassword.md).

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

 

 





