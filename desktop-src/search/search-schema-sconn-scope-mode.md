---
description: Das- <mode> Element gibt an, ob die URL in den Gültigkeitsbereich des Suchconnector eingeschlossen oder ausgeschlossen werden soll. Die zulässigen Werte sind include und Exclude. Dieses Element hat keine untergeordneten Elemente und keine Attribute.
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: Mode-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8c09b4c6de138e6e390d2c31a82fe5d1f56566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750328"
---
# <a name="mode-element-search-connector-schema"></a>Mode-Element (Suchconnector-Schema)

Das- <mode> Element gibt an, ob die URL in den Gültigkeitsbereich des Suchconnector eingeschlossen oder ausgeschlossen werden soll. Die zulässigen Werte sind `Include` und `Exclude`. Dieses Element hat keine untergeordneten Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- mode -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="mode" default="Include">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Include"/>
                                            <xs:enumeration value="Exclude"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
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



| Übergeordnetes Element                                                                   | Untergeordnete Elemente |
|----------------------------------------------------------------------------------|----------------|
| [scopeitem-Element (Suchconnector-Schema)](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a>Bemerkungen

Ein ausgeschlossener Bereich kann nicht durchsucht oder durchsucht werden. Sie können scopeitem-URLs Schachteln. Beispielsweise können Sie einen übergeordneten Bereich und alle zugehörigen untergeordneten Elemente mit Ausnahme von einem übergeordneten Bereich einschließen, indem Sie die übergeordnete URL, den Tiefen Wert Deep und die untergeordnete URL hinzufügen.

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
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



