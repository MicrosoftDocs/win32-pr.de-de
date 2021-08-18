---
title: IMsRdpClientTransportSettings GatewayUserSelectedCredsSource-Eigenschaft
description: Legt die vom Benutzer angegebene Remotedesktop Gateway-Anmeldeinformationsquelle (RD-Gateway) fest oder ruft sie ab.
ms.assetid: 0c12ddf6-52c2-40a2-af2b-effd4e8bbdb6
ms.tgt_platform: multiple
keywords:
- GatewayUserSelectedCredsSource-Eigenschaft Remotedesktopdienste
- GatewayUserSelectedCredsSource-Eigenschaft Remotedesktopdienste , IMsRdpClientTransportSettings-Schnittstelle
- IMsRdpClientTransportSettings-Schnittstelle Remotedesktopdienste , GatewayUserSelectedCredsSource-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.get_GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.put_GatewayUserSelectedCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7632609f34d0133f37af4e8df16ebd574b3ef84e248c2bb3d2b1a84313957b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001010"
---
# <a name="imsrdpclienttransportsettingsgatewayuserselectedcredssource-property"></a>IMsRdpClientTransportSettings::GatewayUserSelectedCredsSource-Eigenschaft

Legt die vom Benutzer angegebene Remotedesktop Gateway-Anmeldeinformationsquelle (RD-Gateway) fest oder ruft sie ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayUserSelectedCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayUserSelectedCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine **ULONG-Variable,** die die RD-Gateway-Authentifizierungsmethode angibt. Dieser Parameter kann einen der folgenden Werte annehmen.

<dt>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC \_ PROXY \_ CREDS \_ MODE \_ USERPASS** (0 (0x0))


</dt> <dd>

Verwenden Sie ein Kennwort (NTLM) als Authentifizierungsmethode für das RD-Gateway.

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC \_ PROXY \_ CREDS \_ MODE \_ SMARTCARD** (1 (0x1))


</dt> <dd>

Verwenden Sie eine Smartcard als Authentifizierungsmethode für das RD-Gateway.

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC \_ PROXY \_ CREDS \_ MODE \_ ANY** (4 (0x4))


</dt> <dd>

Verwenden Sie eine beliebige Authentifizierungsmethode für das RD-Gateway.

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
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings ist als 720298C0-A099-46f5-9F82-96921BAE4701 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





