---
description: Container für ein oder mehrere einzelne propertydescription-Elemente.
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: propertydescriptionlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd0beaf4dbbd8b71c7f4b3335c169754c704d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343807"
---
# <a name="propertydescriptionlist"></a>propertydescriptionlist

Container für ein oder mehrere einzelne [propertydescription](./propdesc-schema-propertydescription.md) -Elemente. Eine. PropDesc-Eigenschafts Beschreibungs-Schema Datei sollte mindestens ein [propertydescriptionlist]() -Element enthalten.

## <a name="syntax"></a>Syntax


```
<!-- propertyDescriptionList -->
<xs:element name="propertyDescriptionList">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="s:propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string" use="required"/>
        <xs:attribute name="product"   type="xs:string" use="required"/>
    </xs:complexType>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_formatid_and_propid">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@formatID"/>
        <xs:field    xpath="@propID"/>
    </xs:unique>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_canonical_name">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@name"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                        | Untergeordnete Elemente                                                   |
|---------------------------------------|------------------------------------------------------------------|
| [schema](./propdesc-schema-entry.md) | [propertydescription](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a>Attribute



| Attribut | BESCHREIBUNG                                                               |
|-----------|---------------------------------------------------------------------------|
| publisher | Öffentlich. Erforderlich. Der Anzeige Name des Verlegers, der das Schema bereitstellt. |
| product   | Öffentlich. Erforderlich. Der Anzeige Name des Produkts, das das Schema bereitstellt.   |



 

## <a name="remarks"></a>Bemerkungen

Die [propertydescriptionlist]() sollte nicht mit "Eigenschafts Listen" und " [**ipropertydescriptionlist**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)" verwechselt werden, die vollständig voneinander getrennt sind.

 

 
