---
description: Gibt an, ob der Zugriff auf alle Infrastrukturnetzwerke blockiert wird.
ms.assetid: d57ae27c-3cd3-4e53-b5c9-cd3cbb91289b
title: denyAllESS (networkFilter)-Element
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
ms.openlocfilehash: 5057f94dd91e2d7090c4f147ba987324e369dda706031ecebb8a79b165214414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619865"
---
# <a name="denyalless-networkfilter-element"></a>denyAllESS (networkFilter)-Element

Das element denyAllESS (networkFilter) gibt an, ob der Zugriff auf alle Infrastrukturnetzwerke blockiert wird. Wenn **denyAllESS über** den Wert TRUE verfügt, können Computer keine Verbindung mit einem Infrastrukturnetzwerk herstellen. Andernfalls können Computer eine Verbindung mit Infrastrukturnetzwerken herstellen.

Der Standardwert für dieses Element ist FALSE. Wenn **denyAllESS** nicht in einem Profil angegeben ist, können Computer standardmäßig eine Verbindung mit Infrastrukturnetzwerken herstellen.

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

Das **denyAllESS-Element** wird durch das [**networkFilter-Element**](wlan-policyschema-networkfilter-wlanpolicy-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




