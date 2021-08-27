---
description: Das erforderliche &lt; &gt; propertyBag-Element gibt einen Satz von Eigenschaften an, die von diesem Speicherortanbieter verwendet werden.
ms.assetid: 63f8f2e4-3b52-4d6e-8d3a-2e133aac0e86
title: propertyBag-Element (Suchconnectorschema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c186e9502c48a1fc052acf28bc8bd8063085b8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883323"
---
# <a name="propertybag-element-search-connector-schema"></a>propertyBag-Element (Suchconnectorschema)

Das erforderliche &lt; &gt; propertyBag-Element gibt einen Satz von Eigenschaften an, die von diesem Speicherortanbieter verwendet werden.

## <a name="syntax"></a>Syntax


```
<!-- propertyBag -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
                            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
                        </xs:element>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                                                 | Untergeordnete Elemente                                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [locationProvider-Element (Connectorschema suchen)](search-schema-sconn-locationprovider.md) | [property-Element (Search Connector Schema)](search-schema-sconn-locationproviderproperty.md) |



 

## <a name="example-of-a-propertybag-element-and-property-elements"></a>Beispiel für ein PropertyBag-Element und Eigenschaftenelemente


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



