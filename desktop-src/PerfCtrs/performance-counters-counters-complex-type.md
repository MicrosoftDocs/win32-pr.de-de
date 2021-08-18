---
description: Definiert den Abschnitt des Instrumentierungsmanifests, der den Anbieter und die von ihnen zur Verfügung stellenden Leistungsindikatoren identifiziert.
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: counters Complex Type
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 14630fa4e0e9461e59d377b4defc3edacee8dca9560d1f7eb42acb317ffd1f57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143963"
---
# <a name="counters-complex-type"></a>counters Complex Type

Definiert den Abschnitt des Instrumentierungsmanifests, der den Anbieter und die von ihnen zur Verfügung stellenden Leistungsindikatoren identifiziert.

``` syntax
<xs:complexType name="counters">
    <xs:choice
        minOccurs="1"
        maxOccurs="1"
    >
        <xs:element name="provider"
            type="man:provider"
         />
    </xs:choice>
    <xs:attribute name="schemaVersion"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="1.1"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element      | type                                                               | Beschreibung                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| **Anbieter** | [**man:provider**](performance-counters-provider-complex-type.md) | Identifiziert einen Anbieter, der Leistungsindikatoren bietet.<br/> |



## <a name="attributes"></a>Attributes



| Name          | type | Beschreibung                                                      |
|---------------|------|------------------------------------------------------------------|
| schemaVersion |      | Die Version des Schemas, das zum Schreiben des Manifests verwendet wird.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Instrumentation**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

