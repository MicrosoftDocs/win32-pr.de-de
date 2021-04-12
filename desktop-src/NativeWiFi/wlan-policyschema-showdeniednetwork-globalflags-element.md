---
description: Gibt an, ob abgelehnte Netzwerke im Assistenten zum Herstellen einer Verbindung mit einem Netzwerk angezeigt werden.
ms.assetid: d0a13a80-2532-4383-8946-2536cc1f5e12
title: showdeniednetwork-Element (globalflags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- showDeniedNetwork
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33049dad00e5fda22e3f739d3dc200a282481a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527800"
---
# <a name="showdeniednetwork-globalflags-element"></a>showdeniednetwork-Element (globalflags)

Das **showdeniednetwork** (globalflags)-Element gibt an, ob abgelehnte Netzwerke im Assistenten **zum Herstellen einer Verbindung mit einem Netzwerk** angezeigt werden. Netzwerke können durch Gruppenrichtlinien oder Benutzereinstellungen verweigert werden. Wenn **showdeniednetwork** den Wert true aufweist, werden abgelehnte Netzwerke im Assistenten **zum Herstellen einer Verbindung mit einem Netzwerk** angezeigt. Andernfalls werden abgelehnte Netzwerke nicht im Assistenten angezeigt.

Dieses Element ist obligatorisch. Wenn ein Profil vom AutoConfig-Dienst erstellt wird, wird für dieses Element der Standardwert false verwendet.

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

Das **showdeniednetwork** -Element wird durch das [**globalflags**](wlan-policyschema-globalflags-wlanpolicy-element.md) -Element definiert.

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

 

 




