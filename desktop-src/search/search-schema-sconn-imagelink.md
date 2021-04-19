---
description: Das optionale- <imageLink> Element gibt eine Miniaturansicht für diesen Suchconnector an. Dieses Element besitzt ein obligatorisches untergeordnetes Element und keine Attribute.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: IMAGELINK-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b2e5cbbfc8bbd98557ebd0405a09cf998e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348350"
---
# <a name="imagelink-element-search-connector-schema"></a>IMAGELINK-Element (Suchconnector-Schema)

Das optionale- <imageLink> Element gibt eine Miniaturansicht für diesen Suchconnector an. Dieses Element besitzt ein obligatorisches untergeordnetes Element und keine Attribute.

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
| [searchconnectordescriptiontype-Element (suchconnectorschema)](search-schema-searchconnectordescription.md) | [IMAGELINK-URL-Element (Suchconnector-Schema)](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a>Bemerkungen

Der IMAGELINK-Wert kann ein lokaler Dateisystempfad oder eine URL sein. Die Bilddatei kann ein beliebiger grundlegender Bildtyp sein, der von Windows 7 unterstützt wird (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelink-element"></a>Beispiel für ein IMAGELINK-Element


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



