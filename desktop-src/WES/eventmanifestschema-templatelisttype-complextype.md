---
title: Komplexer templatelisttype-Typ
description: Definiert eine Liste von Vorlagen, die die Daten angeben, die in die Ereignisse eingeschlossen werden sollen. | Komplexer templatelisttype-Typ
ms.assetid: 7f676746-6773-4ae2-8330-60d432c29e3a
keywords:
- Datentyp "templatelisttype" (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- TemplateListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a60b31fd88d05f00229f27a616a29483a29bd49d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761778"
---
# <a name="templatelisttype-complex-type"></a>Komplexer templatelisttype-Typ

Definiert eine Liste von Vorlagen, die die Daten angeben, die in die Ereignisse eingeschlossen werden sollen.

``` syntax
<xs:complexType name="TemplateListType">
    <xs:sequence>
        <xs:element name="template"
            type="TemplateItemType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                   | type                                                                         | BESCHREIBUNG                                                           |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**fungiert**](eventmanifestschema-template-templatelisttype-element.md) | [**Templateitemtype**](eventmanifestschema-templateitemtype-complextype.md) | Eine Vorlage, die die Daten definiert, die in einem Ereignis enthalten sein sollen.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





