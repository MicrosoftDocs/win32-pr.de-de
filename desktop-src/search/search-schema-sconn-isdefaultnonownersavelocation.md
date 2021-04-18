---
description: Das optionale boolesche <isDefaultNonOwnerSaveLocation> Element gibt an, ob der im Suchconnector beschriebene Speicherort als Standard Speicherort verwendet werden soll, wenn ein Benutzer von einem anderen Computer in einer Heim Netzgruppe ein Element speichern möchte.
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: isdefaultnonbesitzsaveloationselement (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edd39ab76ae1b99d6518ca40407d328f5da9778c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344261"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a>isdefaultnonbesitzsaveloationselement (Suchconnector-Schema)

Das optionale boolesche <isDefaultNonOwnerSaveLocation> Element gibt an, ob der im Suchconnector beschriebene Speicherort als Standard Speicherort verwendet werden soll, wenn ein Benutzer von einem anderen Computer in einer Heim Netzgruppe ein Element speichern möchte. Dieses Element hat keine untergeordneten Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- isDefaultNonOwnerSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/>
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

Wenn "true", wenn ein Benutzer eines anderen Computers in einer Heim Netzgruppe ein Element speichert, speichert Windows-Explorer das Element an dem im-Element angegebenen Speicherort <simpleLocation> .

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



