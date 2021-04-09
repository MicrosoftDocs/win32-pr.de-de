---
description: Gibt den Service Set Identifier (SSID) eines drahtlos Netzwerks an.
ms.assetid: 103808f2-9e5f-4605-b42a-337a13455294
title: Network Name (networkitemtype)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkName
api_type:
- Schema
api_location: ''
ms.openlocfilehash: da635c392a29419e7b151cc2c4fb080ff7d3fca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867908"
---
# <a name="networkname-networkitemtype-element"></a>Network Name (networkitemtype)-Element

Das networkName (networkitemtype)-Element gibt den Service Set Identifier (SSID) eines drahtlos Netzwerks an.

``` syntax
<xs:element name="networkName"
    type="networkNameType"
 />
```

Das **networkName** -Element wird durch den komplexen Typ [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

**Mögliche direkt übergeordnete Elemente in der Schema Instanz**
</dt> <dt>

[**Netzwerk (AllowList)**](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[**Netzwerk (blocklist)**](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




