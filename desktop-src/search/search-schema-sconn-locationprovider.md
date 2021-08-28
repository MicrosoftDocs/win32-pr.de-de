---
description: Das optionale &lt; locationProvider-Element &gt; gibt den Suchanbieter an, der vom Suchconnector des Webdienstanbieters verwendet werden soll. Dieses Element enthält ein obligatorisches Attribut und ein optionales untergeordnetes Element.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: locationProvider-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f049a01cc0c51075c147918a2f43b740000f2e36
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883362"
---
# <a name="locationprovider-element-search-connector-schema"></a>locationProvider-Element (Search Connector Schema)

Das optionale &lt; locationProvider-Element &gt; gibt den Suchanbieter an, der vom Suchconnector des Webdienstanbieters verwendet werden soll. Dieses Element enthält ein obligatorisches Attribut und ein optionales untergeordnetes Element.

## <a name="syntax"></a>Syntax


```
<!-- locationProvider -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
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



| Übergeordnetes Element                                                                                                   | Untergeordnete Elemente                                                                       |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [searchConnectorDescriptionType-Element (Search Connector Schema)](search-schema-searchconnectordescription.md) | [propertyBag-Element (Connectorschema suchen)](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a>Attribute



| attribute | Beschreibung                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | Erforderlich. Der Klassenbezeichner (CLSID) des Suchanbieters. |
| codebase  | Optional.                                                      |



 

## <a name="remarks"></a>Hinweise

Der @clsid Attributwert für den OpenSearch Anbieter ist {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.

Dateisystem- und Protokollhandlerbasierte Suchconnectors können stattdessen das [ &lt; &gt; simpleLocation-Element](search-schema-sconn-simplelocation.md) verwenden. Wenn &lt; locationProvider &gt; vorhanden ist, darf in der Beschreibung &lt; des Suchconnectors KEIN simpleLocation-Element vorhanden &gt; sein.

## <a name="example-of-a-locationprovider-element"></a>Beispiel für ein locationProvider-Element


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



