---
description: Das- <url> Element gibt eine URL zur Miniaturansicht für diesen Suchconnector an. Wenn <imageLink> vorhanden ist, ist dieses Element erforderlich. Sie verfügt über keine untergeordneten Elemente und keine Attribute.
ms.assetid: addb2614-9f4f-4cab-a678-b6020b8c4648
title: IMAGELINK-URL-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97daaafcbf6336dd4d88c3c92315e656d137b1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339754"
---
# <a name="imagelink-url-element-search-connector-schema"></a>IMAGELINK-URL-Element (Suchconnector-Schema)

Das- <url> Element gibt eine URL zur Miniaturansicht für diesen Suchconnector an. Wenn <imageLink> vorhanden ist, ist dieses Element erforderlich. Sie verfügt über keine untergeordneten Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- url -->
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



| Übergeordnetes Element                                                                   | Untergeordnete Elemente |
|----------------------------------------------------------------------------------|----------------|
| [IMAGELINK-Element (Suchconnector-Schema)](search-schema-sconn-imagelink.md) |                |



 

## <a name="remarks"></a>Bemerkungen

Der Wert kann ein Pfad des lokalen Dateisystems oder eine URL sein. Die Bilddatei kann ein beliebiger grundlegender Bildtyp sein, der von Windows 7 unterstützt wird (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelinkurl-element"></a>Beispiel für ein imagelinkurl-Element


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



