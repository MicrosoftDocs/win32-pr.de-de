---
description: Das <depth> -Element gibt an, ob der Bereich des Suchconnector untergeordnete URLs einschließen soll. Die zulässigen Werte sind tief und flach. Dieses Element hat keine untergeordneten Elemente und keine Attribute.
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: tiefen Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf68bcbc96b6d1beb2c381f0a17532272b8d397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958780"
---
# <a name="depth-element-search-connector-schema"></a>tiefen Element (Suchconnector-Schema)

Das <depth> -Element gibt an, ob der Bereich des Suchconnector untergeordnete URLs einschließen soll. Die zulässigen Werte sind `Deep` und `Shallow`. Dieses Element hat keine untergeordneten Elemente und keine Attribute.

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
| [scopeitem-Element (Suchconnector-Schema)](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a>Bemerkungen

Wenn die Tiefe tiefer ist, können Benutzer Elemente in der URL-Ebene von scopeitem oder innerhalb von untergeordneten URLs durchsuchen oder durchsuchen.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt einen Suchbereich, der c: \\ FolderA und alle seine untergeordneten Ordner und c: \\ folderB, aber keinen seiner untergeordneten Ordner enthält.


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



 

 



