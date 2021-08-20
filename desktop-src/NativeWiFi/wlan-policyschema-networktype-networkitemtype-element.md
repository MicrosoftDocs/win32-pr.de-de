---
description: Gibt einen Netzwerktyp an.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: networkType (networkItemType)-Element
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
ms.openlocfilehash: 57616d6701ab4663fa6757ddec5df4886ec02faaf5088f61b6cb466ca834ec81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684390"
---
# <a name="networktype-networkitemtype-element"></a>networkType (networkItemType)-Element

Das networkType -Element (networkItemType) gibt einen Netzwerktyp an. Es gibt zwei Arten von Netzwerken: Infrastrukturnetzwerke (ESS) und Ad-hoc-Netzwerke (IBSS).

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

Das **networkType-Element** wird vom komplexen [**networkItemType-Typ**](wlan-policyschema-networkitemtype-complextype.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**networkItemType**](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

**Mögliche unmittelbar übergeordnete Elemente in der Schemainstanz**
</dt> <dt>

[**network (allowList)**](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[**network (blockList)**](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




