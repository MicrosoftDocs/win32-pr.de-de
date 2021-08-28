---
description: Das optionale &lt; &gt; Scope-Element gibt eine Auflistung von &lt; scopeItem-Elementen &gt; an, die die Bereichseinschlüsse und -ausschlüsse für diesen bestimmten Suchconnector definieren.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: scope-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c011eee8def80a7f1d395a7a52a72d30fb4935
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886692"
---
# <a name="scope-element-search-connector-schema"></a>scope-Element (Search Connector Schema)

Das optionale &lt; &gt; Scope-Element gibt eine Auflistung von &lt; scopeItem-Elementen &gt; an, die die Bereichseinschlüsse und -ausschlüsse für diesen bestimmten Suchconnector definieren. Wenn &lt; scope &gt; vorhanden ist, MUSS er mindestens ein &lt; scopeItem-Element &gt; enthalten. Dieses Element weist keine Attribute auf.

## <a name="syntax"></a>Syntax


```
<!-- scope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                       ...
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                                                                   | Untergeordnete Elemente                                                                    |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [searchConnectorDescriptionType-Element (Search Connector Schema)](search-schema-searchconnectordescription.md) | [scopeItem-Element (Search Connector Schema)](search-schema-sconn-scopeitem.md). |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie die &lt; &gt; Scope- und &lt; scopeItem-Elemente, &gt; um zu ermitteln, welche Standorte durchsucht und von der Suche ausgeschlossen werden sollen.

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



 

 



