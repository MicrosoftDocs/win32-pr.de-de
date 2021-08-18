---
description: Beschreibt eine einzelne eindeutige kanonische Eigenschaft.
ms.assetid: 1a36ec83-5d8a-4fc5-be3d-a8c2f0983057
title: propertyDescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1797880fbc9ce5bf56999c6fbd869b259f893f1391fbde6fca580da29dac3a61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011470"
---
# <a name="propertydescription"></a>propertyDescription

Beschreibt eine einzelne eindeutige kanonische Eigenschaft. Jede solche Eigenschaft, die im System verfügbar sein soll, muss über ein entsprechendes [propertyDescription-Element]() verfügen.

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
| [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) | [searchInfo](./propdesc-schema-searchinfo.md)                   |
|                                                                          | [labelInfo](./propdesc-schema-labelinfo.md)                     |
|                                                                          | [Typeinfo](./propdesc-schema-typeinfo.md)                       |
|                                                                          | [aliasInfo](./propdesc-schema-aliasinfo.md)                     |
|                                                                          | [displayInfo](./propdesc-schema-displayinfo.md)                 |
|                                                                          | [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) |



 

## <a name="attributes"></a>Attribute



| attribute | Beschreibung                                                                                                                                                                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name      | Erforderlich. Der kanonische Eigenschaftenname, der für das System eindeutig ist. Beispiel: `System.Rating` . Diese Zeichenfolge ist vom Typ kanonischer Typ und auf 64 Zeichen beschränkt. Bei dem Namen wird die Groß-/Kleinschreibung beachtet, und es sollte die folgende Syntax verwendet werden: Publisher. Application.PropertyName. [**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) gibt diesen Wert zurück. |
| formatID  | Erforderlich. Der Formatbezeichner der Eigenschaft (FMTID). Der Wert muss einschließende geschweifte Klammern enthalten. Beispiel: `{64440492-4C8B-11D1-8B70-080036B11A03}` . [**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) gibt diesen Wert zurück.                                                                                                                       |
| propID    | Erforderlich. Der Eigenschaftenbezeichner (PID); Beispiel: `9` . [**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) gibt diesen Wert zurück. Dieser Wert muss größer oder gleich 2 sein. Die Werte 0 und 1 werden vom System reserviert.                                                                                                                  |



 

 

 
