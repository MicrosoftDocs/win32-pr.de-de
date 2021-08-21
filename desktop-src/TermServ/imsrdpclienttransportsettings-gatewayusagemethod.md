---
title: IMsRdpClientTransportSettings GatewayUsageMethod (Eigenschaft)
description: Gibt an, wann ein Remotedesktop Gatewayserver (RD-Gateway) verwendet werden soll.
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- GatewayUsageMethod-Remotedesktopdienste
- GatewayUsageMethod-Eigenschaft Remotedesktopdienste , IMsRdpClientTransportSettings-Schnittstelle
- IMsRdpClientTransportSettings-Schnittstelle Remotedesktopdienste , GatewayUsageMethod -Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUsageMethod
- IMsRdpClientTransportSettings.get_GatewayUsageMethod
- IMsRdpClientTransportSettings.put_GatewayUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a177d191d3303cf44778713ebdef88db955d28ede58691bda1e9ad05aa51a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001040"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a>IMsRdpClientTransportSettings::GatewayUsageMethod (Eigenschaft)

Gibt an, wann ein Remotedesktop Gatewayserver (RD-Gateway) verwendet werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayUsageMethod(
  [in]  ULONG ulProxyMethod
);

HRESULT get_GatewayUsageMethod(
  [out] ULONG *pulProxyUsageMethod
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine **ULONG-Variable,** die die Verwendungsmethode des RD-Gatewayservers angibt. Dieser Parameter kann einen der folgenden Werte annehmen.

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC \_ PROXYMODUS \_ \_ NONE \_ DIRECT** (0 (0x0))


</dt> <dd>

Verwenden Sie keinen RD-Gatewayserver. Auf der Remotedesktopverbindung -Clientbenutzeroberfläche (RDC) ist das Kontrollkästchen **RD-Gatewayserver** für lokale Adressen umgehen nicht mehr verfügbar.

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC \_ PROXY \_ MODE \_ DIRECT** (1 (0x1))


</dt> <dd>

Verwenden Sie immer einen RD-Gatewayserver. Auf der Benutzeroberfläche des RDC-Clients ist das **Kontrollkästchen RD-Gatewayserver** für lokale Adressen umgehen nicht mehr verfügbar.

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC \_ PROXY \_ MODE \_ DETECT** (2 (0x2))


</dt> <dd>

Verwenden Sie einen RD-Gatewayserver, wenn keine direkte Verbindung mit dem RD-Sitzungshost hergestellt werden kann. Auf der Benutzeroberfläche des RDC-Clients ist das **Kontrollkästchen RD-Gatewayserver** für lokale Adressen umgehen aktiviert.

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC \_ PROXYMODUS \_ \_ STANDARD** (3 (0x3))


</dt> <dd>

Verwenden Sie die Standardeinstellungen des RD-Gatewayservers.

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC \_ PROXY \_ MODE \_ NONE \_ DETECT** (4 (0x4))


</dt> <dd>

Verwenden Sie keinen RD-Gatewayserver. Auf der Benutzeroberfläche des RDC-Clients ist das **Kontrollkästchen RD-Gatewayserver** für lokale Adressen umgehen aktiviert.

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Gibt **S \_ OK zurück,** wenn erfolgreich.

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

 

 





