---
description: Das optionale boolesche <includeInStartMenuScope> Element gibt an, ob dieser Suchconnector im Startmenü-Suchbereich enthalten sein soll.
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: includeinstartmenus-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 126d10a2b69dcec5057e732679c8531fd6e82bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343652"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a>includeinstartmenus-Element (Suchconnector-Schema)

Das optionale boolesche <includeInStartMenuScope> Element gibt an, ob dieser Suchconnector im Startmenü-Suchbereich enthalten sein soll. Der Standardwert ist true für Suchconnectors, die das Dateisystem als Datenquelle verwenden, und false für Suchconnectors, die von Eigenschaften Handlern verwendet werden. Dieses Element hat keine untergeordneten Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- includeInStartMenuScope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                                                                   | Untergeordnete Elemente |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [searchconnectordescriptiontype-Element (suchconnectorschema)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Suchconnector in den Startmenü Bereich einschließen, können Benutzer ihren Speicherort über das Suchfeld im Startmenü durchsuchen.

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



