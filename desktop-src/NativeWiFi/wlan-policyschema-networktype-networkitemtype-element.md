---
description: Gibt einen Netzwerktyp an.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: NetworkType (networkitemtype)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c63b8afdaf699fde6871c198a8235772c59da1ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352272"
---
# <a name="networktype-networkitemtype-element"></a>NetworkType (networkitemtype)-Element

Das NetworkType (networkitemtype)-Element gibt einen Netzwerktyp an. Es gibt zwei Arten von Netzwerken: Infrastruktur Netzwerke (ESS) und Ad-hoc-Netzwerke (IBSS).

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

Das **NetworkType** -Element wird durch den komplexen Typ [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) definiert.

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

 

 




