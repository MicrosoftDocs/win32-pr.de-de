---
description: Das optionale boolesche &lt; includeInStartMenuScope-Element &gt; gibt an, ob dieser Suchconnector in den suchbereich Startmenü aufgenommen werden soll.
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: includeInStartMenuScope-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20696dc6d2bc41b3f693e771a59541204e376e7
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882389"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a>includeInStartMenuScope-Element (Search Connector Schema)

Das optionale boolesche &lt; includeInStartMenuScope-Element &gt; gibt an, ob dieser Suchconnector in den suchbereich Startmenü aufgenommen werden soll. Der Standardwert ist true für Suchconnectors, die das Dateisystem als Datenquelle verwenden, und FALSE für Suchconnectors, die von Eigenschaftenhandlern verwendet werden. Dieses Element weist keine untergeordneten Elemente und keine Attribute auf.

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
| [searchConnectorDescriptionType-Element (Search Connector Schema)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Hinweise

Wenn Sie den Suchconnector in den bereich Startmenü einschließen, können Benutzer Ihren Standort über das Suchfeld im Startmenü durchsuchen.

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



