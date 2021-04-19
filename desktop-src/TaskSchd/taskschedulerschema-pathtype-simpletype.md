---
title: pfadtype simple-Typ
description: Definiert die minimale und maximale Anzahl von Zeichen für eine Zeichenfolge, die einen Dateipfad definiert.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- pfadtype-Typ "Simple" Taskplaner
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a75ef7d85eba2aa39e0c3c768fec0908c7ea16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342880"
---
# <a name="pathtype-simple-type"></a>pfadtype simple-Typ

Definiert die minimale und maximale Anzahl von Zeichen für eine Zeichenfolge, die einen Dateipfad definiert. Der Pfad darf keine leere Zeichenfolge sein und muss weniger als 260 Zeichen umfassen.

``` syntax
<xs:simpleType name="pathType">
    <xs:restriction
        base="nonEmptyString"
    >
        <xs:maxLength
            value="260"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





