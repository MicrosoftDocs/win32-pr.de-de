---
title: IMsRdpClientTransportSettings2 GatewayPassword (Eigenschaft)
description: Gibt das Kennwort an, das ein Benutzer zum Herstellen einer Verbindung mit dem Remotedesktop Gatewayserver (RD-Gateway) angibt.
ms.assetid: f29078e5-49ab-45a0-8d79-4b57d7c35e3a
ms.tgt_platform: multiple
keywords:
- GatewayPassword-Remotedesktopdienste
- GatewayPassword-Eigenschaft Remotedesktopdienste , IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2-Schnittstelle Remotedesktopdienste, GatewayPassword-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPassword
- IMsRdpClientTransportSettings2.put_GatewayPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977ac8114a8be4f4f5ef8aa21a4a00f48aead31ee18f7fe41f789ff2a3c9b478
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959350"
---
# <a name="imsrdpclienttransportsettings2gatewaypassword-property"></a>IMsRdpClientTransportSettings2::GatewayPassword(Eigenschaft)

Gibt das Kennwort an, das ein Benutzer zum Herstellen einer Verbindung mit dem Remotedesktop Gatewayserver (RD-Gateway) angibt.

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayPassword(
  [in] BSTR proxyPassword
);
```



## <a name="property-value"></a>Eigenschaftswert

Das Kennwort, das ein Benutzer zum Herstellen einer Verbindung mit dem RD-Gatewayserver anpasst.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





