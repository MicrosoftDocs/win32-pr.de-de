---
description: Beschreibt eine einzelne eindeutige kanonische Eigenschaft.
ms.assetid: 1a36ec83-5d8a-4fc5-be3d-a8c2f0983057
title: propertydescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233f6d9b1242a9f02b2edbb2bb29cefaef625c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959357"
---
# <a name="propertydescription"></a>propertydescription

Beschreibt eine einzelne eindeutige kanonische Eigenschaft. Jede solche Eigenschaft, die im System verfügbar sein soll, muss über ein entsprechendes [propertydescription]() -Element verfügen.

## <a name="syntax-for-windows-7"></a>Syntax für Windows 7


```
<!-- propertyDescription for Windows 7-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
            <xs:element ref="relatedPropertyInfo" minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="propid" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-vista"></a>Syntax für Vista


```
<!-- propertyDescription for Windows Vista-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                           | Untergeordnete Elemente                                                   |
|--------------------------------------------------------------------------|------------------------------------------------------------------|
| [propertydescriptionlist](./propdesc-schema-propertydescriptionlist.md) | [SearchInfo](./propdesc-schema-searchinfo.md)                   |
|                                                                          | [Labelinfo](./propdesc-schema-labelinfo.md)                     |
|                                                                          | [TypeInfo](./propdesc-schema-typeinfo.md)                       |
|                                                                          | [aliasInfo](./propdesc-schema-aliasinfo.md)                     |
|                                                                          | [Display Info](./propdesc-schema-displayinfo.md)                 |
|                                                                          | [relatedpropertyinfo](./propdesc-schema-relatedpropertyinfo.md) |



 

## <a name="attributes"></a>Attribute



| Attribut | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name      | Erforderlich. Der kanonische Eigenschaftsname, der für das System eindeutig ist. Beispiel: `System.Rating` . Diese Zeichenfolge ist vom Typ "Canonical-Type" und ist auf 64 Zeichen beschränkt. Beim Namen wird die Groß-/Kleinschreibung beachtet, und es sollte die folgende Syntax verwendet werden: Publisher. Application. PropertyName. [**Ipropertydescription:: GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) gibt diesen Wert zurück. |
| FormatID  | Erforderlich. Der Format Bezeichner (fmtid) der Eigenschaft. Der Wert muss einschließende geschweifte Klammern enthalten. Beispiel: `{64440492-4C8B-11D1-8B70-080036B11A03}` . [**Ipropertydescription:: getpropertykey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) gibt diesen Wert zurück.                                                                                                                       |
| propID    | Erforderlich. Der Eigenschaften Bezeichner (PID); Beispiel: `9` . [**Ipropertydescription:: getpropertykey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) gibt diesen Wert zurück. Dieser Wert muss größer oder gleich 2 sein. Die Werte 0 und 1 werden vom System reserviert.                                                                                                                  |



 

 

 
