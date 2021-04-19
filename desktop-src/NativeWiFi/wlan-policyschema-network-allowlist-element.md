---
description: Definiert ein zulässiges Netzwerk.
ms.assetid: 6dd90924-ded4-427d-a6cd-7742acf89c21
title: Network (AllowList)-Element
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
ms.openlocfilehash: eb89a3037b7684c4e20e26ef3a2b0502be69251a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373323"
---
# <a name="network-allowlist-element"></a>Network (AllowList)-Element

Das Network (AllowList)-Element definiert ein zulässiges Netzwerk. Ein Computer muss eine Verbindung mit einem zulässigen Netzwerk herstellen können.

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

Das **Network** -Element wird durch das [**AllowList**](wlan-policyschema-allowlist-networkfilter-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Zulassungs**](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**AllowList (NetworkFilter)**](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> </dl>

 

 




