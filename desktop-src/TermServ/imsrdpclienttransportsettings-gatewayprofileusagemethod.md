---
title: IMsRdpClientTransportSettings GatewayProfileUsageMethod-Eigenschaft
description: Gibt an, ob die Standardeinstellungen für Remotedesktop Gateway (RD-Gateway) verwendet werden sollen.
ms.assetid: ce774790-31ad-40ba-ba8f-e81b0dbda175
ms.tgt_platform: multiple
keywords:
- GatewayProfileUsageMethod-Eigenschaft Remotedesktopdienste
- GatewayProfileUsageMethod-Eigenschaft Remotedesktopdienste , IMsRdpClientTransportSettings-Schnittstelle
- IMsRdpClientTransportSettings-Schnittstelle Remotedesktopdienste , GatewayProfileUsageMethod-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.get_GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.put_GatewayProfileUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3386e6a38c99539aebb84280dc8250b2d779f5d81229763d2d926ae499e144e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138623"
---
# <a name="imsrdpclienttransportsettingsgatewayprofileusagemethod-property"></a>IMsRdpClientTransportSettings::GatewayProfileUsageMethod-Eigenschaft

Gibt an, ob die Standardeinstellungen für Remotedesktop Gateway (RD-Gateway) verwendet werden sollen.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayProfileUsageMethod(
  [in]  ULONG ulProxyProfileMethod
);

HRESULT get_GatewayProfileUsageMethod(
  [out] ULONG *pulProxyProfileUsageMethod
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Rd-Gateway-Profilverwendungsmethode. Dieser Parameter kann einen der folgenden Werte annehmen.

<dt>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC \_ \_ \_ PROXYPROFILMODUS \_ STANDARD** (0 (0x0))


</dt> <dd>

Verwenden Sie den Vom Administrator angegebenen Standardprofilmodus.

</dd> <dt>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC \_ \_ \_ PROXYPROFILMODUS \_ EXPLICIT** (1 (0x1))


</dt> <dd>

Verwenden Sie explizite Einstellungen, wie vom Benutzer angegeben.

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

 

 





