---
title: Komplexer BaseEapParameters-Typ – Benutzereigenschaften
description: Definiert das Element, das die ausgewählte Legacymethode und methodenspezifische Anmeldeinformationen angegeben hat.
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
keywords:
- Komplexer BaseEapParameters-Typ EAPHost
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
ms.openlocfilehash: 80ae1dc749d1c31ee11809b530fe1b04a59ce3e4e4dc76e84323b7dc078ec44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978290"
---
# <a name="baseeapparameters-complex-type---user-properties"></a>Komplexer BaseEapParameters-Typ – Benutzereigenschaften

Der komplexe **BaseEapParameters-Typ** definiert das Element, das die ausgewählte Legacymethode und methodenspezifische Anmeldeinformationen angegeben hat.

Die -Methode kann die konstituierenden Elemente in **BaseEapParameters** definieren. Die -Methode führt auch eine Schemavalidierung für die Elemente in **BaseEapParameters durch.**

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



| Element                                                                      | type    | Beschreibung                                                                                               |
|------------------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|
| [**type**](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | integer | Definiert das Platzhalterelement für den ausgewählten Methodentyp und methodenspezifische Anmeldeinformationen. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[baseeapuserpropertiesv1-Schema](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





