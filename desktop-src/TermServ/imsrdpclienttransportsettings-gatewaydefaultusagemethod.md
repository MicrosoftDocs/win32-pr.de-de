---
title: Imsrdpclienttransportsettings (gatewaydefaultusagemethod-Eigenschaft)
description: Die Standard Verwendungs Methode für Remotedesktop Gateway (RD-Gateway).
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- Gatewaydefaultusagemethod-Eigenschaft Remotedesktopdienste
- Gatewaydefaultusagemethod-Eigenschaft Remotedesktopdienste, imsrdpclienttransportsettings-Schnittstelle
- Imsrdpclienttransportsettings-Schnittstelle Remotedesktopdienste, gatewaydefaultusagemethod-Eigenschaft
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
ms.openlocfilehash: 0b8417da30f9a692e6e233174a33f4b03682a5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338525"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a>Imsrdpclienttransportsettings:: gatewaydefaultusagemethod (Eigenschaft)

Die Standard Verwendungs Methode für Remotedesktop Gateway (RD-Gateway).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf die Standard Verwendungs Methode für RD-Gateway. Gibt eine Union der Benutzereinstellungen zurück, die durch [**Put \_ gatewayusagemethod ()**](imsrdpclienttransportsettings-gatewayusagemethod.md)und Gruppenrichtlinien Einstellungen festgelegt werden. Wenn keine Benutzereinstellungen durch **Put \_ gatewayusagemethod ()** festgelegt wurden, gibt **get \_ gatewaydefaultusagemethod ()** den Standardwert für die **Erkennung des TSC- \_ Proxy \_ Modus \_** zurück.

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

 

 





