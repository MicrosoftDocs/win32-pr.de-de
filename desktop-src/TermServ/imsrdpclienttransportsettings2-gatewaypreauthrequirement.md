---
title: IMsRdpClientTransportSettings2 gatewaypreauthrequirement (Eigenschaft)
description: Gibt die Einstellung für das einmalige Kennwort (One-time password, OTP) des Remotedesktop Gateway-Gateways (RD-Gateway) an oder ruft diese ab.
ms.assetid: cc8f7ebb-16ba-45ed-ba66-de4a339946d0
ms.tgt_platform: multiple
keywords:
- Gatewaypreauthrequirement-Eigenschaft Remotedesktopdienste
- Gatewaypreauthrequirement-Eigenschaft Remotedesktopdienste, IMsRdpClientTransportSettings2-Schnittstelle
- IMsRdpClientTransportSettings2 Interface Remotedesktopdienste, gatewaypreauthrequirement (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.get_GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.put_GatewayPreAuthRequirement
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058ca92237a4f9729f526030f5f8a836ce1c739c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518941"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthrequirement-property"></a>IMsRdpClientTransportSettings2:: gatewaypreauthrequirement (Eigenschaft)

Gibt die Einstellung für das einmalige Kennwort (One-time password, OTP) des Remotedesktop Gateway-Gateways (RD-Gateway) an oder ruft diese ab.

Wenn OTP aktiviert ist, versucht **gatewaypreauthrequirement** , das OTP-Cookie mithilfe der [**gatewaypreauthserveraddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) -Eigenschaft aus dem Internet Cookie-Speicher abzufragen. Bei erfolgreicher Ausführung sendet **gatewaypreauthrequirement** das OTP-Cookie für die Vorauthentifizierung an den Firewallserver (z. b. Microsoft Internet Security und Acceleration \[ ISA \] Server).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayPreAuthRequirement(
  [in]  ULONG ulProxyPreAuthRequirement
);

HRESULT get_GatewayPreAuthRequirement(
  [out] ULONG *pulProxyPreAuthRequirement
);
```



## <a name="property-value"></a>Eigenschaftswert

Wenn der Wert auf 1 festgelegt ist, ist die OTP-Funktion aktiviert. Wenn der Wert auf 0 festgelegt ist, ist die OTP-Funktion deaktiviert.

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

 

 





