---
title: pathType Simple Type
description: Definiert die minimale und maximale Anzahl von Zeichen für eine Zeichenfolge, die einen Dateipfad definiert.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- pathType simple type Taskplaner
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 289e91b3d7139001bfab22c81bfb0f9e9871033f6296286373c5bde18fdc366d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758379"
---
# <a name="pathtype-simple-type"></a>pathType Simple Type

Definiert die minimale und maximale Anzahl von Zeichen für eine Zeichenfolge, die einen Dateipfad definiert. Der Pfad darf keine leere Zeichenfolge sein und darf weniger als 260 Zeichen lang sein.

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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





