---
title: nonemptystringtype simple-Typ
description: Definiert die Werte, die für eine nicht leere Text Zeichenfolge verwendet werden.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- nonEmptyString Simple Type Taskplaner
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab9c9fa84c510fc4e67f6f63664a58d6d4093709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392037"
---
# <a name="nonemptystringtype-simple-type"></a>nonemptystringtype simple-Typ

Definiert die Werte, die für eine nicht leere Text Zeichenfolge verwendet werden.

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Enumerationswerte

Der einfache Typ **nonEmptyString** definiert den folgenden Wert.



| Wert | BESCHREIBUNG                                            |
|-------|--------------------------------------------------------|
| 1     | Die Zeichenfolge enthält mindestens ein Zeichen.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





