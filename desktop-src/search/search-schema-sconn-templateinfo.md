---
description: Dieses optionale <templateInfo> Element gibt einen Ordnertyp zum Anzeigen der Ergebnisse einer Abfrage über diesen Suchconnector an. Dieses Element weist keine Attribute und nur ein obligatorisches untergeordnetes Element auf.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: templateingefo-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fd28780689b4d544f251bbaf1542bc379ecdaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346494"
---
# <a name="templateinfo-element-search-connector-schema"></a>templateingefo-Element (Suchconnector-Schema)

Dieses optionale <templateInfo> Element gibt einen Ordnertyp zum Anzeigen der Ergebnisse einer Abfrage über diesen Suchconnector an. Dieses Element weist keine Attribute und nur ein obligatorisches untergeordnetes Element auf.

## <a name="syntax"></a>Syntax


```
<!-- templateInfo -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="templateInfo" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="folderType" minOccurs="0"/>
                    </xs:all>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                                                                   | Untergeordnete Elemente                                                                     |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [searchconnectordescriptiontype-Element (suchconnectorschema)](search-schema-searchconnectordescription.md) | [foldertype-Element (Suchconnector-Schema)](search-schema-sconn-foldertype.md) |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie keinen bestimmten Ordnertyp im- <templateInfo> Element angeben, verwendet Windows den Ordner "General Search Connector" {8faf9629-1980-46ff-8023-9dceab9c3ee3}.

## <a name="example-of-a-templateinfo-element"></a>Beispiel für ein templateingefo-Element


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



