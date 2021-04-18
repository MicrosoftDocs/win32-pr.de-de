---
title: Komplexer XmlType-Typ
description: Definiert ein XML-Fragment.
ms.assetid: ac6ce2a2-4584-4181-9a39-aceab85d5c51
keywords:
- Ereignisprotokoll für komplexen XmlType-Typ
topic_type:
- apiref
api_name:
- XmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a4d71d7f4f2685d6c5f1c0626392c79436b68d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391893"
---
# <a name="xmltype-complex-type"></a>Komplexer XmlType-Typ

Definiert ein XML-Fragment. Eine beliebige Schema Instanz ist zulässig. der Knoten der obersten Ebene im Fragment muss ein Namespace-Attribut enthalten.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





