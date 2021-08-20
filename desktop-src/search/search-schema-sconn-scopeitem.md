---
description: Das <scopeItem> -Element stellt einen einzelnen Eintrag in der Ausschluss-/Einschlussbereichstabelle dar.
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: scopeItem-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bf8cc7ba9d296503a9703845d8a03287006ed178dca7f51228e89827a0c710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118051502"
---
# <a name="scopeitem-element-search-connector-schema"></a>scopeItem-Element (Search Connector Schema)

Das <scopeItem> -Element stellt einen einzelnen Eintrag in der Ausschluss-/Einschlussbereichstabelle dar. <scopeItem> erweitert den standardmäßigen shellLinkType-Typ, indem drei neue Elemente hinzugefügt werden, die ein- und ausschließende Ordner steuern, die Tiefe der Ergebnisse steuern und den Speicherort des Bereichs angeben. Wenn das <scope> Element vorhanden ist, ist dieses Element erforderlich. Sie verfügt über drei untergeordnete Elemente und keine Attribute.

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
|                                                                          | [scopeItem url-Element (Search Connector Schema)](search-schema-sconn-scope-url.md). |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie die Elemente und , um zu bestimmen, welche Orte durchsucht werden sollen <scope> und welche Standorte von der Suche ausgeschlossen werden <scopeItem> sollen.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt einen Suchbereich, der C: ExampleFolder und alle untergeordneten Ordner außer \\ C: \\ ExampleFolder \\ ExcludeMe enthält.


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



 

 



