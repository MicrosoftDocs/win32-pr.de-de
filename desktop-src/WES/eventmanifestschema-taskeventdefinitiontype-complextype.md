---
title: Komplexer TaskEventDefinitionType-Typ
description: Definiert ein Aufgaben spezifisches Ereignis, das von Ihrem Anbieter protokolliert werden kann. | Komplexer TaskEventDefinitionType-Typ
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- TaskEventDefinitionType komplexer Typ (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ebf752dbaf97ceced84b6bd9698faf7b191c07e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106370386"
---
# <a name="taskeventdefinitiontype-complex-type"></a>Komplexer TaskEventDefinitionType-Typ

\[Beginnend mit dem Nachrichten Compiler, der mit der Windows 7-Version der Windows SDK ausgeliefert wird, ist der komplexe Typ TaskEventDefinitionType nicht mehr verfügbar. Verwenden Sie stattdessen aufgabenspezifische Opcodes, um die gleiche Funktionalität bereitzustellen.\]

Definiert ein Aufgaben spezifisches Ereignis, das von Ihrem Anbieter protokolliert werden kann.

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="event"
                        type="EventDefinitionType"
                        maxOccurs="unbounded"
                     />
                </xs:sequence>
                <xs:attribute name="name"
                    type="QName"
                    use="required"
                 />
            </xs:complexType>
        </xs:element>
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                      | type                                                                               | BESCHREIBUNG                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| **event**                                                                    | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Ein Aufgaben spezifisches Ereignis, das mit einer Aufgabe veröffentlicht wurde.<br/> |
| [**OpCode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | Ein Aufgaben spezifischer Opcode für ein Ereignis. <br/>   |



## <a name="attributes"></a>Attributes



| Name | type      | BESCHREIBUNG                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Der Name des aufgabenspezifischen OpCodes.<br/> |
| name | anyURI    | Der Name der Aufgabe.<br/>                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





