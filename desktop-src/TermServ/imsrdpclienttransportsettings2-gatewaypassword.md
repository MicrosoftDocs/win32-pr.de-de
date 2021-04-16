---
title: IMsRdpClientTransportSettings2 gatewaypassword (Eigenschaft)
description: Gibt das Kennwort an, das ein Benutzer zum Herstellen einer Verbindung mit dem Remotedesktop Gateway-Server (RD-Gateway) bereitstellt.
ms.assetid: f29078e5-49ab-45a0-8d79-4b57d7c35e3a
ms.tgt_platform: multiple
keywords:
- Gatewaypassword-Eigenschaft Remotedesktopdienste
- Gatewaypassword-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2 Interface Remotedesktopdienste, gatewaypassword (Eigenschaft)
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
ms.openlocfilehash: 1d532f28023b7ff0eb3b8571e3875d0b63606535
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517486"
---
# <a name="imsrdpclienttransportsettings2gatewaypassword-property"></a>IMsRdpClientTransportSettings2:: gatewaypassword (Eigenschaft)

Gibt das Kennwort an, das ein Benutzer zum Herstellen einer Verbindung mit dem Remotedesktop Gateway-Server (RD-Gateway) bereitstellt.

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayPassword(
  [in] BSTR proxyPassword
);
```



## <a name="property-value"></a>Eigenschaftswert

Das Kennwort, das ein Benutzer zum Herstellen einer Verbindung mit dem RD-Gateway-Server bereitstellt.

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

 

 





