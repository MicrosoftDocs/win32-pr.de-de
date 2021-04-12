---
description: Das optionale boolesche <isDefaultSaveLocation> Element gibt an, ob der im Suchconnector beschriebene Speicherort als Standard Speicherort verwendet werden soll. Dieses Element hat keine untergeordneten Elemente und keine Attribute.
ms.assetid: 4a33f411-d71e-41d3-b5fd-018a92dceeac
title: isdefaultsaveloation-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b664e4cd6f7c88f1dfbeb44ba23faee5d24a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342909"
---
# <a name="isdefaultsavelocation-element-search-connector-schema"></a>isdefaultsaveloation-Element (Suchconnector-Schema)

Das optionale boolesche <isDefaultSaveLocation> Element gibt an, ob der im Suchconnector beschriebene Speicherort als Standard Speicherort verwendet werden soll. Dieses Element hat keine untergeordneten Elemente und keine Attribute.

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
| [searchconnectordescriptiontype-Element (suchconnectorschema)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein Benutzer ein Element speichert, speichert Windows-Explorer das Element an der Position, die im- <simpleLocation> Element angegeben ist. Benutzer können diese Einstellung im Dialogfeld "Eigenschaften" für den Suchconnector ändern.

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



