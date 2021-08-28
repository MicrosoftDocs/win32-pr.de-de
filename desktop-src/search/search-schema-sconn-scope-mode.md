---
description: Das &lt; mode-Element gibt an, ob die URL in den Bereich des Suchconnectors eingeschlossen oder &gt; daraus ausgeschlossen werden soll. Die zulässigen Werte sind Include und Exclude. Dieses Element verfügt über keine untergeordneten Elemente und keine Attribute.
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: mode-Element (Connectorschema suchen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e096bb21d634da6107359c014b82f1b367aba1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886748"
---
# <a name="mode-element-search-connector-schema"></a>mode-Element (Connectorschema suchen)

Das &lt; mode-Element gibt an, ob die URL in den Bereich des Suchconnectors eingeschlossen oder &gt; daraus ausgeschlossen werden soll. Die zulässigen Werte sind `Include` und `Exclude`. Dieses Element verfügt über keine untergeordneten Elemente und keine Attribute.

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
| [scopeItem-Element (Search Connector Schema)](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a>Hinweise

Ein ausgeschlossener Bereich kann nicht durchsucht oder durchsucht werden. Sie können scopeItem-URLs schachteln. Sie können z. B. einen übergeordneten Bereich und alle untergeordneten Bereiche mit Ausnahme eines übergeordneten Bereichs hinzufügen, indem Sie die übergeordnete URL als eingeschlossen, den Tiefenwert Deep und die untergeordnete URL ausschließen.

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
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



