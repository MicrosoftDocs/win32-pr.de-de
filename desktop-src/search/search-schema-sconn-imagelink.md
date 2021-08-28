---
description: Das optionale &lt; imageLink-Element &gt; gibt eine Miniaturansicht für diesen Suchconnector an. Dieses Element verfügt über ein obligatorisches untergeordnetes Element und keine Attribute.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: imageLink-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6030f44e74f8f8441b3a6cd0835df9c5969619
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882395"
---
# <a name="imagelink-element-search-connector-schema"></a>imageLink-Element (Search Connector Schema)

Das optionale &lt; imageLink-Element &gt; gibt eine Miniaturansicht für diesen Suchconnector an. Dieses Element verfügt über ein obligatorisches untergeordnetes Element und keine Attribute.

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

Der imageLink-Wert kann ein lokaler Dateisystempfad oder eine URL sein. Die Bilddatei kann jeder der grundlegenden Bildtypen sein, die von Windows 7 (PNG, BMP, JPG, GIF) unterstützt werden.

## <a name="example-of-an-imagelink-element"></a>Beispiel für ein imageLink-Element


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



