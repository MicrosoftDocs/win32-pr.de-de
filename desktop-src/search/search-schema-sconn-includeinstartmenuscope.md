---
description: Das optionale boolesche Element gibt an, ob dieser Suchconnector in den <includeInStartMenuScope> Suchbereich Startmenü werden soll.
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: includeInStartMenuScope-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60941ef06f3f7220c7bbbae652f5e8256c6256660ea8e9ece2ddd330858958b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937950"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a>includeInStartMenuScope-Element (Search Connector Schema)

Das optionale boolesche Element gibt an, ob dieser Suchconnector in den <includeInStartMenuScope> Suchbereich Startmenü werden soll. Der Standardwert ist true für Suchconnectors, die das Dateisystem als Datenquelle verwenden, und false für Suchconnectors, die von Eigenschaftenhandlern verwendet werden. Dieses Element verfügt über keine untergeordneten Elemente und keine Attribute.

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

Wenn Sie den Suchconnector in den bereich Startmenü, können Benutzer Ihren Standort über das Suchfeld im Startmenü.

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



