---
title: Imsrdpclienttransportsettings (gatewayusagemethod-Eigenschaft)
description: Gibt an, wann ein Remotedesktop Gateway-Server (RD-Gateway) verwendet werden soll.
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- Gatewayusagemethod-Eigenschaft Remotedesktopdienste
- Gatewayusagemethod-Eigenschaft Remotedesktopdienste, imsrdpclienttransportsettings-Schnittstelle
- Imsrdpclienttransportsettings-Schnittstelle Remotedesktopdienste, gatewayusagemethod-Eigenschaft
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
ms.openlocfilehash: f07bc10c67d01f957e588d1b50085e57b0fa10b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340986"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a>Imsrdpclienttransportsettings:: gatewayusagemethod-Eigenschaft

Gibt an, wann ein Remotedesktop Gateway-Server (RD-Gateway) verwendet werden soll.

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

Eine **ulong** -Variable, die die RD-Gateway Server-Verwendungs Methode angibt. Dieser Parameter kann einen der folgenden Werte annehmen.

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC \_ Proxy \_ Modus " \_ keine \_ direkt** " (0 (0x0))


</dt> <dd>

Verwenden Sie keinen RD-Gateway Server. In der Client Benutzeroberfläche des Remotedesktopverbindung (RDC) ist das Kontrollkästchen **RD-Gateway Server für lokale Adressen umgehen** deaktiviert.

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC \_ Proxy \_ Modus \_ Direct** (1 (0x1))


</dt> <dd>

Verwenden Sie immer einen RD-Gateway Server. In der RDC-Client-Benutzeroberfläche ist das Kontrollkästchen **RD-Gateway Server für lokale Adressen umgehen** deaktiviert.

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC \_ Proxy \_ Modus- \_ Erkennung** (2 (0x2))


</dt> <dd>

Verwenden Sie einen RD-Gateway Server, wenn keine direkte Verbindung mit dem RD-Sitzungshost Server hergestellt werden kann. Auf der RDC-Client Benutzeroberfläche ist das Kontrollkästchen **RD-Gateway Server für lokale Adressen umgehen** aktiviert.

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC \_ Proxy \_ Modus \_ Standard** (3 (0x3))


</dt> <dd>

Standard RD-Gateway Servereinstellungen verwenden.

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC \_ Proxy \_ Modus \_ keine \_ Erkennung** (4 (0x4))


</dt> <dd>

Verwenden Sie keinen RD-Gateway Server. Auf der RDC-Client Benutzeroberfläche ist das Kontrollkästchen **RD-Gateway Server für lokale Adressen umgehen** aktiviert.

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

 

 





