---
description: Gibt an, ob Computer den integrierten automatischen Konfigurations Dienst zum Verwalten von Verbindungen mit verkabelten Netzwerken verwenden, die Layer 2-Authentifizierung erfordern (z. b. 802.1 x).
ms.assetid: c7a0f6bc-4d42-4d95-8483-2c480f4d8db9
title: enableautoconfig (globalflags)-Element (LAN_policy)
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
ms.openlocfilehash: af1ca32f177140bbfc6563f74df5afc519ee0c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757800"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a>enableautoconfig (globalflags)-Element (LAN_policy)

Das **enableautoconfig** (globalflags)-Element gibt an, ob Computer den integrierten automatischen Konfigurations Dienst zum Verwalten von Verbindungen mit Kabel Netzwerken verwenden, die Layer 2-Authentifizierung erfordern (z. b. 802.1 x).

Wenn **enableautoconfig** den Wert false aufweist, dürfen Computer den integrierten automatischen Konfigurations Dienst nicht zum Verwalten von Verbindungen verwenden, für die die Layer 2-Authentifizierung erforderlich ist. Stattdessen ist das im [**ProfileList**](lan-policyschema-profilelist-lanpolicy-element.md) -Element angegebene Netzwerk das einzige Netzwerk, das für die Verbindung verfügbar ist. Der Dienst für die automatische Konfiguration antwortet nur auf Anforderungen, um den Dienst zu aktivieren.

Wenn **enableautoconfig** den Wert true aufweist, können Computer den integrierten automatischen Konfigurations Dienst verwenden, um eine Verbindung mit Kabel Netzwerken herzustellen, für die Layer 2-Authentifizierung erforderlich ist.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

Das **enableautoconfig** -Element wird durch das [**globalflags**](lan-policyschema-globalflags-lanpolicy-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**globalflags**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**globalflags (lanpolicy)**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 




