---
description: Definiert den Abschnitt des Instrumentierungs Manifests, mit dem der Anbieter und die von Ihnen bereitgestellten Indikatoren identifiziert werden.
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: komplexer Typ der Leistungsindikatoren
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ad87b79175b0cecdec17ad081340fa0be2b90b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959755"
---
# <a name="counters-complex-type"></a>komplexer Typ der Leistungsindikatoren

Definiert den Abschnitt des Instrumentierungs Manifests, mit dem der Anbieter und die von Ihnen bereitgestellten Indikatoren identifiziert werden.

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



| Element      | type                                                               | BESCHREIBUNG                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| **ab** | [**man: Provider**](performance-counters-provider-complex-type.md) | Identifiziert einen Anbieter, der Leistungsindikatoren bereitstellt.<br/> |



## <a name="attributes"></a>Attributes



| Name          | type | BESCHREIBUNG                                                      |
|---------------|------|------------------------------------------------------------------|
| schemaVersion |      | Die Version des Schemas, das zum Schreiben des Manifests verwendet wird.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ener**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

