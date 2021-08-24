---
description: Container für ein oder mehrere einzelne propertyDescription-Elemente.
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: propertyDescriptionList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f22e5e8e2c90b1a9f9587117f684ebfb89c55ee702749248cb0a886d5ba8266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341840"
---
# <a name="propertydescriptionlist"></a>propertyDescriptionList

Container für ein oder mehrere einzelne [propertyDescription-Elemente.](./propdesc-schema-propertydescription.md) Eine Propdesc-Eigenschaftenbeschreibungsschemadatei sollte mindestens ein [propertyDescriptionList-Element]() enthalten.

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
| [schema](./propdesc-schema-entry.md) | [propertyDescription](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a>Attribute



| attribute | BESCHREIBUNG                                                               |
|-----------|---------------------------------------------------------------------------|
| publisher | Öffentlich. Erforderlich. Der Anzeigename des Herausgebers, der das Schema an stellt. |
| product   | Öffentlich. Erforderlich. Der Anzeigename des Produkts, das das Schema enthält.   |



 

## <a name="remarks"></a>Hinweise

[PropertyDescriptionList]() sollte nicht mit "Eigenschaftenlisten" und [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)verwechselt werden, die vollständig getrennt sind.

 

 
