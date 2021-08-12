---
title: IMsRdpClientTransportSettings GatewayDefaultUsageMethod (Eigenschaft)
description: Die Standardverwendungsmethode für Remotedesktop Gateway (RD-Gateway).
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- GatewayDefaultUsageMethod-Remotedesktopdienste
- GatewayDefaultUsageMethod-Eigenschaft Remotedesktopdienste , IMsRdpClientTransportSettings-Schnittstelle
- IMsRdpClientTransportSettings-Schnittstelle Remotedesktopdienste , GatewayDefaultUsageMethod (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayDefaultUsageMethod
- IMsRdpClientTransportSettings.get_GatewayDefaultUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6403f319eaa79b9d140a3d75f9dd4f7625eced916ee907755c017d3e58a1767f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607421"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a>IMsRdpClientTransportSettings::GatewayDefaultUsageMethod (Eigenschaft)

Die Standardverwendungsmethode für Remotedesktop Gateway (RD-Gateway).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf die Standardverwendungsmethode für rd-Gateway. Gibt eine Vereinigung der Benutzereinstellungen zurück, die durch [**put \_ GatewayUsageMethod() und**](imsrdpclienttransportsettings-gatewayusagemethod.md)Gruppenrichtlinieneinstellungen festgelegt werden. Wenn von **put \_ GatewayUsageMethod()** keine Benutzereinstellungen festgelegt wurden, gibt **get \_ GatewayDefaultUsageMethod()** den Standardwert **TSC PROXY MODE DETECT \_ \_ \_ zurück.**

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

 

 





