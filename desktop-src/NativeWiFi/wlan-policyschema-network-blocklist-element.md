---
description: Definiert ein blockiertes Netzwerk.
ms.assetid: ccf24d45-cae0-4eb7-951a-004a5f71e04a
title: Network (blocklist)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- network
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f58948573db281aacb00e227ff0fbc2f1cdf82b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352728"
---
# <a name="network-blocklist-element"></a>Network (blocklist)-Element

Das Network (blocklist)-Element definiert ein blockiertes Netzwerk. Ein Computer kann keine Verbindung mit einem blockierten Netzwerk herstellen.

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

Das **Network** -Element wird durch das [**Block List**](wlan-policyschema-blocklist-networkfilter-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Blocklisten**](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**blocklist (NetworkFilter)**](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> </dl>

 

 




