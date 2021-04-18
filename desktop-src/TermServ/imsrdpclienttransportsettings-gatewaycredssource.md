---
title: Imsrdpclienttransportsettings (gatewaykredssource-Eigenschaft)
description: Gibt die Authentifizierungsmethode für das Remotedesktop Gateway (RD-Gateway) an oder ruft Sie ab.
ms.assetid: 3b05edcb-f678-4d80-99fd-b76d27c80c68
ms.tgt_platform: multiple
keywords:
- Gatewaykredssource-Eigenschaft Remotedesktopdienste
- Gatewaykredssource-Eigenschaft Remotedesktopdienste, imsrdpclienttransportsettings-Schnittstelle
- Imsrdpclienttransportsettings-Schnittstelle Remotedesktopdienste, gatewaykredssource-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayCredsSource
- IMsRdpClientTransportSettings.get_GatewayCredsSource
- IMsRdpClientTransportSettings.put_GatewayCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2771998ddc7c53d05c5d0db452f34a734a7c3e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391670"
---
# <a name="imsrdpclienttransportsettingsgatewaycredssource-property"></a>Imsrdpclienttransportsettings:: gatewaykredssource-Eigenschaft

Gibt die Authentifizierungsmethode für das Remotedesktop Gateway (RD-Gateway) an oder ruft Sie ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine **ulong** -Variable, die die RD-Gateway Authentifizierungsmethode angibt. Dieser Parameter kann einen der folgenden Werte annehmen.

<dt>

Port für den TSC- \_ Proxy- \_ \_ \_ Benutzer Durchlauf (0)
</dt> <dd>

Verwenden Sie ein Kennwort (NTLM) als Authentifizierungsmethode für RD-Gateway.

</dd> <dt>

Smartcard für den TSC-Proxy-Anmelde \_ \_ \_ Modus \_ (1)
</dt> <dd>

Verwenden Sie eine Smartcard als Authentifizierungsmethode für RD-Gateway.

</dd> <dt>

Port für den TSC- \_ Proxy- \_ \_ Modus \_ Any (4)
</dt> <dd>

Verwenden Sie für RD-Gateway eine beliebige Authentifizierungsmethode.

</dd> </dl>

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

 

 





