---
description: Definiert die Typen von Drahtlos Netzwerken.
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: einfacher networktypetype-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d0acb998c879e718a0e201418610bb0aa6db8c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364188"
---
# <a name="networktypetype-simple-type"></a>einfacher networktypetype-Typ

Der einfache Typ networktypetype definiert die Typen von Drahtlos Netzwerken. Es gibt zwei Arten von Netzwerken: Infrastruktur Netzwerke (ESS) und Ad-hoc-Netzwerke (IBSS).

``` syntax
<xs:simpleType name="networkTypeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="IBSS"
         />
        <xs:enumeration
            value="ESS"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Enumerationswerte

Der einfache Typ **Network Typetype** definiert die folgenden Werte:



| Wert | BESCHREIBUNG |
|-------|-------------|
| IBSS  |             |
| Lich   |             |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




