---
description: Das <propertyStore> optionale -Element gibt den Speicherort eines XML-basierten IPropertyStore an, um offene Metadaten für diesen Suchconnector zu speichern. Dieses Element verfügt über keine Attribute und nur über ein untergeordnetes Element.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: propertyStore-Element (Connectorschema suchen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de5a9e801163bd85635b82c1915394f24c39d3dfdafcb64c81fcff0bf84a219
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351850"
---
# <a name="propertystore-element-search-connector-schema"></a>propertyStore-Element (Connectorschema suchen)

Das <propertyStore> optionale -Element gibt den Speicherort eines XML-basierten IPropertyStore an, um offene Metadaten für diesen Suchconnector zu speichern. Dieses Element verfügt über keine Attribute und nur über ein untergeordnetes Element.

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
| [searchConnectorDescriptionType-Element (Search Connector Schema)](search-schema-searchconnectordescription.md) | [property-Element von propertyStore (Connectorschema suchen)](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt ein <propertyStore> -Element mit zwei <property> -Elementen.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



