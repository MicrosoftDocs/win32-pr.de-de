---
description: Gibt an, ob der Zugriff auf alle Infrastruktur Netzwerke blockiert ist.
ms.assetid: d57ae27c-3cd3-4e53-b5c9-cd3cbb91289b
title: denyalless (NetworkFilter)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllESS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c3e83aeb14e0572f8e2ccc49bf2d04718afa7f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214519"
---
# <a name="denyalless-networkfilter-element"></a>denyalless (NetworkFilter)-Element

Das denyalless (NetworkFilter)-Element gibt an, ob der Zugriff auf alle Infrastruktur Netzwerke blockiert ist. Wenn **denyalless** den Wert true aufweist, können Computer keine Verbindung mit einem Infrastrukturnetzwerk herstellen. Andernfalls können Computer Verbindungen mit Infrastruktur Netzwerken herstellen.

Der Standardwert für dieses Element ist false. Wenn **denyalless** nicht in einem Profil angegeben ist, können Computer standardmäßig eine Verbindung mit Infrastruktur Netzwerken herstellen.

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

Das **denyalless** -Element wird durch das [**NetworkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Network Filter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Network Filter (wlanpolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




