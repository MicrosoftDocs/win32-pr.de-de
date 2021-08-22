---
description: Gibt an, ob Computer den integrierten automatischen Konfigurationsdienst verwenden, um Verbindungen mit kabelgebundenen Netzwerken zu verwalten, die eine Layer-2-Authentifizierung erfordern (z.B. 802.1X).
ms.assetid: c7a0f6bc-4d42-4d95-8483-2c480f4d8db9
title: enableAutoConfig-Element (globalFlags) (LAN_policy)
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
ms.openlocfilehash: 2842da69b07136df80d15ea84553aecdf2c62d417c73f7ec85d9c315b819a397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780200"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a>enableAutoConfig-Element (globalFlags) (LAN_policy)

Das **element enableAutoConfig** (globalFlags) gibt an, ob Computer den integrierten automatischen Konfigurationsdienst verwenden, um Verbindungen mit kabelgebundenen Netzwerken zu verwalten, die eine Layer-2-Authentifizierung erfordern (z.B. 802.1X).

Wenn **enableAutoConfig** den Wert FALSE auf hat, dürfen Computer keinen integrierten automatischen Konfigurationsdienst verwenden, um Verbindungen zu verwalten, die eine Layer-2-Authentifizierung erfordern. Stattdessen ist das im [**profileList-Element**](lan-policyschema-profilelist-lanpolicy-element.md) angegebene Netzwerk das einzige netzwerk, das für die Verbindung verfügbar ist. Der automatische Konfigurationsdienst antwortet nur auf Anforderungen, um den Dienst zu aktivieren.

Wenn **enableAutoConfig** den Wert TRUE hat, können Computer den integrierten automatischen Konfigurationsdienst verwenden, um eine Verbindung mit kabelgebundenen Netzwerken herzustellen, die eine Layer-2-Authentifizierung erfordern.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

Das **enableAutoConfig-Element** wird durch das [**globalFlags-Element**](lan-policyschema-globalflags-lanpolicy-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**globalFlags (LANPolicy)**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 




