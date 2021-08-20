---
title: Komplexer BaseEapParameters-Typ– Verbindungseigenschaften
description: Definiert das Platzhalterelement für die methodentyp- und methodenspezifische Konfiguration.
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
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
ms.openlocfilehash: 4ae3abf23b19badb123f8eb49097c6b3e9d7ac6d26fc0132f34b84de5ac24c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086954"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a>Komplexer BaseEapParameters-Typ– Verbindungseigenschaften

Der **komplexe BaseEapParameters-Typ** definiert das Platzhalterelement für den Methodentyp und die methodenspezifische Konfiguration.

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



| Element                                                                            | Typ    | Beschreibung                                     |
|------------------------------------------------------------------------------------|---------|-------------------------------------------------|
| [**Typ**](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | integer | Hier ist jede Schemainstanz zulässig.<br/> |



## <a name="remarks"></a>Hinweise

In **BaseEapParameters** kann die Methode die konstituierenden Elemente definieren. Die -Methode führt auch eine Schemavalidierung für die Elemente in **BaseEapParameters aus.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[baseeapconnectionpropertiesv1-Schema](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





