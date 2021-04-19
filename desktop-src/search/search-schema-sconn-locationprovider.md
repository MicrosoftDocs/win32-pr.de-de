---
description: Das optionale- <locationProvider> Element gibt den Suchanbieter an, der vom Webdienstanbieter-Suchconnector verwendet werden soll. Dieses Element enthält ein obligatorisches Attribut und ein optionales untergeordnetes Element.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: locationprovider-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c68732300c190b44b984bbe64ca031a81ced84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346907"
---
# <a name="locationprovider-element-search-connector-schema"></a>locationprovider-Element (Suchconnector-Schema)

Das optionale- <locationProvider> Element gibt den Suchanbieter an, der vom Webdienstanbieter-Suchconnector verwendet werden soll. Dieses Element enthält ein obligatorisches Attribut und ein optionales untergeordnetes Element.

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
| [searchconnectordescriptiontype-Element (suchconnectorschema)](search-schema-searchconnectordescription.md) | [PropertyBag-Element (Suchconnector-Schema)](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a>Attribute



| Attribut | BESCHREIBUNG                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | Erforderlich. Der Klassen Bezeichner (CLSID) des Such Anbieters. |
| codebase  | Dies ist optional.                                                      |



 

## <a name="remarks"></a>Bemerkungen

Der @clsid Attribut Wert für den OpenSearch-Anbieter ist {48e277f 6-4e74-4cd6-ba6s-fa4s42898223}.

Auf Dateisystem-und protokollhandlerbasierten Suchconnectors kann stattdessen das-Element verwendet werden [<simpleLocation>](search-schema-sconn-simplelocation.md) . Wenn <locationProvider> vorhanden ist, darf <simpleLocation> in der Suchconnector-Beschreibung kein-Element vorhanden sein.

## <a name="example-of-a-locationprovider-element"></a>Beispiel für ein locationprovider-Element


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



