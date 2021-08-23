---
description: Definiert die Funknetzwerktypen.
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: networkTypeType Simple Type
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
ms.openlocfilehash: 40184bb027f80826baa3ad56090755a2cd9ec630f9eb105e402d30a6ecf2661c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800110"
---
# <a name="networktypetype-simple-type"></a>networkTypeType Simple Type

Der einfache NetworkTypeType-Typ definiert die Drahtlosnetzwerktypen. Es gibt zwei Arten von Netzwerken: Infrastrukturnetzwerke (ESS) und Ad-hoc-Netzwerke (IBSS).

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

Der einfache **networkTypeType-Typ** definiert die folgenden Werte.



| Wert | Beschreibung |
|-------|-------------|
| IBSS  |             |
| Ess   |             |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




