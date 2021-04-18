---
title: 'Basieeapparameters komplexer Typ: Benutzereigenschaften'
description: Definiert das Element, das die ausgewählte Legacy Methode und die Methoden spezifischen Anmelde Informationen angegeben hat.
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
keywords:
- Baseeapparameters komplexer Typ EAPHost
topic_type:
- apiref
api_name:
- BaseEapParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 451c03123634dd98a1f4a49292db0a807009f6f5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106365360"
---
# <a name="baseeapparameters-complex-type---user-properties"></a>Basieeapparameters komplexer Typ: Benutzereigenschaften

Der komplexe Typ **baseeapparameters** definiert das Element, das die ausgewählte Legacy Methode und die Methoden spezifischen Anmelde Informationen angegeben hat.

Die-Methode kann die konstituierenden Elemente innerhalb von **baseeapparameters** definieren. die-Methode führt auch eine Schema Validierung für die Elemente in **baseeapparameters** aus.

``` syntax
<xs:complexType name="BaseEapParameters">
    <xs:sequence>
        <xs:element name="Type"
            type="integer"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                      | type    | BESCHREIBUNG                                                                                               |
|------------------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|
| [**type**](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | integer | Definiert das Platzhalter Element für den ausgewählten Methodentyp und die Methoden spezifischen Anmelde Informationen. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[baseeapuserpropertiesv1-Schema](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





