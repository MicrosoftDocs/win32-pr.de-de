---
description: Das optionale <scope> -Element gibt eine Auflistung von- <scopeItem> Elementen an, die die Inklusions-und Ausschlüsse für diesen bestimmten Suchconnector definieren.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Scope-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f49041170db80de48d312596249d5c4dca835e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343651"
---
# <a name="scope-element-search-connector-schema"></a>Scope-Element (Suchconnector-Schema)

Das optionale <scope> -Element gibt eine Auflistung von- <scopeItem> Elementen an, die die Inklusions-und Ausschlüsse für diesen bestimmten Suchconnector definieren. Wenn <scope> vorhanden ist, muss Sie mindestens ein Element enthalten <scopeItem> . Dieses Element weist keine Attribute auf.

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
| [searchconnectordescriptiontype-Element (suchconnectorschema)](search-schema-searchconnectordescription.md) | [scopeitem-Element (Suchconnector-Schema)](search-schema-sconn-scopeitem.md). |



 

## <a name="remarks"></a>Bemerkungen

Verwenden <scope> Sie das-Element und das- <scopeItem> Element, um zu ermitteln, welche Orte gesucht werden sollen und welche Standorte von der Suche ausgeschlossen werden sollen

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt einen Suchbereich, der c: \\ examplefolder und alle seine untergeordneten Ordner mit Ausnahme von c: \\ examplefolder \\ excludebug enthält.


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



 

 



