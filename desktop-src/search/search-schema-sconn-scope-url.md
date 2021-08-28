---
description: Das &lt; &gt; URL-Element gibt eine URL an, die den Bereich des Suchconnectors darstellt. Dieses Element weist keine untergeordneten Elemente und keine Attribute auf.
ms.assetid: 5afd84aa-98e3-4118-845a-d4efad19a488
title: scopeItem url-Element (Connectorschema suchen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a1db669f7365f04bed49c769ab695ab674b20b
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886707"
---
# <a name="scopeitem-url-element-search-connector-schema"></a>scopeItem url-Element (Connectorschema suchen)

Das &lt; &gt; URL-Element gibt eine URL an, die den Bereich des Suchconnectors darstellt. Dieses Element weist keine untergeordneten Elemente und keine Attribute auf.

## <a name="syntax"></a>Syntax


```
<!-- url -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0"><xs:all>
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="url" type="xs:anyURI"/>
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence></xs:all>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                                   | Untergeordnete Elemente |
|----------------------------------------------------------------------------------|----------------|
| [scopeItem-Element (Search Connector Schema)](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a>Hinweise

Der Wert kann ein lokaler Dateisystempfad oder eine URL sein.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt einen Suchbereich, der C: \\ ExampleFolder und alle seine untergeordneten Ordner mit Ausnahme von C: \\ ExampleFolder \\ ExcludeMe enthält.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder</url>
        </scopeItem>
        <scopeItem>
            <mode>Exclude</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



