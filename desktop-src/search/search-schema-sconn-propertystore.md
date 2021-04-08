---
description: Das optionale <propertyStore> -Element gibt den Speicherort eines XML-basierten IPropertyStore an, um geöffnete Metadaten für diesen Suchconnector zu speichern. Dieses Element weist keine Attribute und nur ein untergeordnetes Element auf.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: PropertyStore-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11f8cda6457de764b00519a81a1134e7eecc8638
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750329"
---
# <a name="propertystore-element-search-connector-schema"></a>PropertyStore-Element (Suchconnector-Schema)

Das optionale <propertyStore> -Element gibt den Speicherort eines XML-basierten IPropertyStore an, um geöffnete Metadaten für diesen Suchconnector zu speichern. Dieses Element weist keine Attribute und nur ein untergeordnetes Element auf.

## <a name="syntax"></a>Syntax


```
<!-- propertyStore -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0">
            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                                                                   | Untergeordnete Elemente                                                                                            |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [searchconnectordescriptiontype-Element (suchconnectorschema)](search-schema-searchconnectordescription.md) | [Property-Element von PropertyStore (Suchconnector-Schema)](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt ein- <propertyStore> Element mit zwei- <property> Elementen.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



