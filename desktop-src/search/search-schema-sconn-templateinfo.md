---
description: Dieses optionale &lt; templateInfo-Element &gt; gibt einen Ordnertyp zum Anzeigen der Ergebnisse einer Abfrage über diesen Suchconnector an. Dieses Element hat keine Attribute und nur ein obligatorisches untergeordnetes Element.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: templateInfo-Element (Connectorschema suchen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c815d04e23f1e1af9582ad93ba08d118855676
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880385"
---
# <a name="templateinfo-element-search-connector-schema"></a>templateInfo-Element (Connectorschema suchen)

Dieses optionale &lt; templateInfo-Element &gt; gibt einen Ordnertyp zum Anzeigen der Ergebnisse einer Abfrage über diesen Suchconnector an. Dieses Element hat keine Attribute und nur ein obligatorisches untergeordnetes Element.

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
| [searchConnectorDescriptionType-Element (Search Connector Schema)](search-schema-searchconnectordescription.md) | [folderType-Element (Search Connector Schema)](search-schema-sconn-foldertype.md) |



 

## <a name="remarks"></a>Hinweise

Wenn Sie im templateInfo-Element keinen bestimmten Ordnertyp &lt; &gt; angeben, verwendet Windows den Allgemeinen Suchconnectorordnertyp {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.

## <a name="example-of-a-templateinfo-element"></a>Beispiel für ein templateInfo-Element


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



