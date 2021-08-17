---
description: Das -Element gibt an, ob der Bereich des <depth> Suchconnectors untergeordnete URLs enthalten soll. Die zulässigen Werte sind Deep und Shallow. Dieses Element verfügt über keine untergeordneten Elemente und keine Attribute.
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: depth-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245156088cd68fcf67103c18b987a9b459b0b760b3a04a1ced817badd25aada8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862525"
---
# <a name="depth-element-search-connector-schema"></a>depth-Element (Search Connector Schema)

Das -Element gibt an, ob der Bereich des <depth> Suchconnectors untergeordnete URLs enthalten soll. Die zulässigen Werte sind `Deep` und `Shallow`. Dieses Element verfügt über keine untergeordneten Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- depth -->
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
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Shallow"/>
                                            <xs:enumeration value="Deep"/>
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

Wenn die Tiefe tief ist, können Benutzer Elemente auf der URL-Ebene des scopeItem oder in untergeordneten URLs durchsuchen oder durchsuchen.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt einen Suchbereich, der C: FolderA und alle untergeordneten Ordner und \\ C: \\ FolderB, aber keinen der untergeordneten Ordner enthält.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\FolderA</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\FolderB</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



