---
title: komplexer headerfieldstype-Typ
description: Definiert die Elemente, die die Felder für einen e-Mail-Header angeben.
ms.assetid: 1ad1b62d-5aca-4be4-b956-6f8c64761b2b
keywords:
- komplexer headerfieldstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- headerFieldsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: edb783972217d0455eb2ee25fed31cf20e5b774b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475963"
---
# <a name="headerfieldstype-complex-type"></a>komplexer headerfieldstype-Typ

Definiert die Elemente, die die Felder für einen e-Mail-Header angeben.

``` syntax
<xs:complexType name="headerFieldsType">
    <xs:sequence>
        <xs:element name="HeaderField"
            type="headerFieldType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                         | type                                                                       | BESCHREIBUNG                                       |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------|
| [**Headerfield**](taskschedulerschema-headerfield-headerfieldstype-element.md) | [**headerfieldtype**](taskschedulerschema-headerfieldtype-complextype.md) | Gibt ein Feld in einem e-Mail-Header an. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





