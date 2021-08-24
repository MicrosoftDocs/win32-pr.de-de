---
description: Das <imageLink> optionale -Element gibt eine Miniaturansicht für diesen Suchconnector an. Dieses Element verfügt über ein obligatorisches untergeordnetes Element und keine Attribute.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: imageLink-Element (Connectorschema suchen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007ad8c2500e2739210646c446d9f906d5a83571ea4ac9780ab9136b73805c83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711090"
---
# <a name="imagelink-element-search-connector-schema"></a>imageLink-Element (Connectorschema suchen)

Das <imageLink> optionale -Element gibt eine Miniaturansicht für diesen Suchconnector an. Dieses Element verfügt über ein obligatorisches untergeordnetes Element und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- imageLink -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="imageLink" minOccurs="0">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="url" type="xs:anyURI"/>
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



| Übergeordnetes Element                                                                                                   | Untergeordnete Elemente                                                                           |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [searchConnectorDescriptionType-Element (Search Connector Schema)](search-schema-searchconnectordescription.md) | [imageLink url-Element (Search Connector Schema)](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a>Hinweise

Der ImageLink-Wert kann ein lokaler Dateisystempfad oder eine URL sein. Die Bilddatei kann einer der grundlegenden Bildtypen sein, die von Windows 7 (PNG, BMP, JPG, GIF) unterstützt werden.

## <a name="example-of-an-imagelink-element"></a>Beispiel für ein imageLink-Element


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



