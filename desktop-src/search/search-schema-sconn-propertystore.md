---
description: Das &lt; optionale propertyStore-Element gibt den Speicherort eines &gt; XML-basierten IPropertyStore an, um offene Metadaten für diesen Suchconnector zu speichern. Dieses Element verfügt über keine Attribute und nur über ein untergeordnetes Element.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: propertyStore-Element (Connectorschema suchen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c617f560e0471062064bcec8020dd5e6efa026
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886793"
---
# <a name="propertystore-element-search-connector-schema"></a>propertyStore-Element (Connectorschema suchen)

Das &lt; optionale propertyStore-Element gibt den Speicherort eines &gt; XML-basierten IPropertyStore an, um offene Metadaten für diesen Suchconnector zu speichern. Dieses Element verfügt über keine Attribute und nur über ein untergeordnetes Element.

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

Das folgende Beispiel zeigt ein &lt; propertyStore-Element &gt; mit zwei &lt; &gt; Eigenschaftenelementen.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



