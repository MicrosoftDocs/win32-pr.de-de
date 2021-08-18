---
description: Das <locationProvider> optionale -Element gibt den Suchanbieter an, der vom Suchconnector des Webdienstanbieters verwendet werden soll. Dieses Element enthält ein obligatorisches Attribut und ein optionales untergeordnetes Element.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: locationProvider-Element (Connectorschema suchen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21101fd0e7c57b73af7bc9de525baaca9583d11e425b168d806f750063ac7203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711040"
---
# <a name="locationprovider-element-search-connector-schema"></a>locationProvider-Element (Connectorschema suchen)

Das <locationProvider> optionale -Element gibt den Suchanbieter an, der vom Suchconnector des Webdienstanbieters verwendet werden soll. Dieses Element enthält ein obligatorisches Attribut und ein optionales untergeordnetes Element.

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
| [searchConnectorDescriptionType-Element (Search Connector Schema)](search-schema-searchconnectordescription.md) | [propertyBag-Element (Suchconnectorschema)](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a>Attribute



| attribute | Beschreibung                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | Erforderlich. Der Klassenbezeichner (CLSID) des Suchanbieters. |
| codebase  | Optional.                                                      |



 

## <a name="remarks"></a>Hinweise

Der Attributwert für den @clsid OpenSearch-Anbieter ist {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.

Dateisystem- und Protokollhandler-basierte Suchconnectors können stattdessen das [<simpleLocation>](search-schema-sconn-simplelocation.md) -Element verwenden. Wenn <locationProvider> vorhanden ist, DARF KEIN -Element in der Beschreibung des <simpleLocation> Search-Connectors vorhanden sein.

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



 

 



