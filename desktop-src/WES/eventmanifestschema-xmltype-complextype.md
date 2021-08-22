---
title: Komplexer XmlType-Typ
description: Definiert ein XML-Fragment.
ms.assetid: ac6ce2a2-4584-4181-9a39-aceab85d5c51
keywords:
- Komplexer XmlType-Typ EventLog
topic_type:
- apiref
api_name:
- XmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9ac529ad3d965af76c144d0f02c1e6f8e5aef36fb25fd2fb052a5fdedc1e45f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589161"
---
# <a name="xmltype-complex-type"></a>Komplexer XmlType-Typ

Definiert ein XML-Fragment. Jede Schemainstanz ist zulässig. Der Knoten der obersten Ebene im Fragment muss ein Namespaceattribut enthalten.

``` syntax
<xs:complexType name="XmlType">
    <xs:sequence>
        <xs:any
            processContents="skip"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





