---
description: Das- <scopeItem> Element stellt einen einzelnen Eintrag in der Ausschluss-/Inklusions Bereichs Tabelle dar.
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: scopeitem-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2033202be6d904880ec9c4efa1c60db4bb7e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128492"
---
# <a name="scopeitem-element-search-connector-schema"></a>scopeitem-Element (Suchconnector-Schema)

Das- <scopeItem> Element stellt einen einzelnen Eintrag in der Ausschluss-/Inklusions Bereichs Tabelle dar. <scopeItem> erweitert den standardmäßigen shelllinktype-Typ durch Hinzufügen von drei neuen Elementen, die das einschließen und Ausschließen von Ordnern steuern, die Tiefe der Ergebnisse steuern und den Speicherort des Bereichs angeben. Wenn das- <scope> Element vorhanden ist, ist dieses Element erforderlich. Sie verfügt über drei untergeordnete Elemente und keine Attribute.

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
| [Scope-Element (Suchconnector-Schema)](search-schema-sconn-scope.md) | [Scope-Element (Suchconnector-Schema)](search-schema-sconn-scope-mode.md).        |
|                                                                          | [Scope-Element (Suchconnector-Schema)](search-schema-sconn-scope-depth.md).       |
|                                                                          | [scopeitem-URL-Element (Suchconnector-Schema)](search-schema-sconn-scope-url.md). |



 

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



 

 



