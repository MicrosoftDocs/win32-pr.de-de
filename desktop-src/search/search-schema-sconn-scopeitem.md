---
description: Das &lt; scopeItem-Element &gt; stellt einen einzelnen Eintrag in der Ausschluss-/Einschlussbereichstabelle dar.
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: scopeItem-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a585acd065efcbc58091d4c8bebce733ed2c73
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880442"
---
# <a name="scopeitem-element-search-connector-schema"></a>scopeItem-Element (Search Connector Schema)

Das &lt; scopeItem-Element &gt; stellt einen einzelnen Eintrag in der Ausschluss-/Einschlussbereichstabelle dar. &lt;scopeItem &gt; erweitert den Standardtyp shellLinkType, indem drei neue Elemente hinzugefügt werden, die das Ein- und Ausschließen von Ordnern steuern, die Tiefe der Ergebnisse steuern und den Speicherort des Bereichs angeben. Wenn das &lt; &gt; Scope-Element vorhanden ist, ist dieses Element erforderlich. Es verfügt über drei untergeordnete Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- scopeItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                <xs:element name="mode" default="Include">
                                    ...
                                </xs:element>
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    ...
                                </xs:element>
                                <xs:element name="url" type="xs:anyURI"/>
                            </xs:all>
                        </xs:complexType>
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



| Übergeordnetes Element                                                           | Untergeordnete Elemente                                                                        |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [scope-Element (Search Connector Schema)](search-schema-sconn-scope.md) | [scope-Element (Search Connector Schema)](search-schema-sconn-scope-mode.md).        |
|                                                                          | [scope-Element (Search Connector Schema)](search-schema-sconn-scope-depth.md).       |
|                                                                          | [scopeItem url-Element (Connectorschema suchen)](search-schema-sconn-scope-url.md). |



 

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



 

 



