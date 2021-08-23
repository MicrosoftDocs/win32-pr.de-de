---
description: Das optionale boolesche Element gibt an, ob der im Suchconnector beschriebene Speicherort als <isDefaultSaveLocation> Standardspeicherort verwendet werden soll. Dieses Element verfügt über keine untergeordneten Elemente und keine Attribute.
ms.assetid: 4a33f411-d71e-41d3-b5fd-018a92dceeac
title: isDefaultSaveLocation-Element (Connectorschema suchen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94cfe2f620dd7c4ccac2bed27dd87511e9174861aeb74dce9ac5737263e9275
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597480"
---
# <a name="isdefaultsavelocation-element-search-connector-schema"></a>isDefaultSaveLocation-Element (Connectorschema suchen)

Das optionale boolesche Element gibt an, ob der im Suchconnector beschriebene Speicherort als <isDefaultSaveLocation> Standardspeicherort verwendet werden soll. Dieses Element verfügt über keine untergeordneten Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- isDefaultSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
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

Wenn ein Benutzer ein Element speichert, speichert Windows Explorer das Element an dem im -Element angegebenen <simpleLocation> Speicherort. Benutzer können diese Einstellung über das Dialogfeld Eigenschaften für den Suchconnector ändern.

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



