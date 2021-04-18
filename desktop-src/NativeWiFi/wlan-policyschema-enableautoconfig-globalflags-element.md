---
description: Gibt an, ob Computer den integrierten automatischen Konfigurations Dienst (AutoConfig) zum Verwalten von Drahtlos Verbindungen verwenden.
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
title: enableautoconfig (globalflags)-Element (LAN_policy) für WLAN
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- enableAutoConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5105b8e634aa5affa8648b763a82bbd60cbaec17
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106364581"
---
# <a name="enableautoconfig-globalflags-element-lan_policy-for-wlan"></a>enableautoconfig (globalflags)-Element (LAN_policy) für WLAN 

Das **enableautoconfig** (globalflags)-Element gibt an, ob Computer den integrierten automatischen Konfigurations Dienst (AutoConfig) zum Verwalten von Drahtlos Verbindungen verwenden. Wenn **enableautoconfig** den Wert false aufweist, dürfen Computer keine automatische Konfiguration zum Verwalten von Drahtlos Verbindungen verwenden, und der Auto Config-Dienst antwortet nur auf Anforderungen zum Aktivieren des Dienstanbieter. Wenn **enableautoconfig** den Wert true aufweist, kann der AutoConfig-Dienst von Computern verwendet werden.

Dieses Element ist obligatorisch. Wenn ein Profil vom AutoConfig-Dienst erstellt wird, hat dieses Element den Standardwert true.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

Das **enableautoconfig** -Element wird durch das [**globalflags**](wlan-policyschema-globalflags-wlanpolicy-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**globalflags**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**globalflags (wlanpolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




