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
# <a name="imagelink-element-search-connector-schema"></a><span data-ttu-id="eaae0-104">IMAGELINK-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="eaae0-104">imageLink Element (Search Connector Schema)</span></span>

<span data-ttu-id="eaae0-105">Das optionale- <imageLink> Element gibt eine Miniaturansicht für diesen Suchconnector an.</span><span class="sxs-lookup"><span data-stu-id="eaae0-105">The optional <imageLink> element specifies a thumbnail for this search connector.</span></span> <span data-ttu-id="eaae0-106">Dieses Element besitzt ein obligatorisches untergeordnetes Element und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="eaae0-106">This element has one mandatory child element and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaae0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eaae0-107">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="eaae0-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="eaae0-108">Element Information</span></span>



| <span data-ttu-id="eaae0-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="eaae0-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="eaae0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eaae0-110">Child Elements</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eaae0-111">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="eaae0-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="eaae0-112">IMAGELINK-URL-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="eaae0-112">imageLink url Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a><span data-ttu-id="eaae0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eaae0-113">Remarks</span></span>

<span data-ttu-id="eaae0-114">Der IMAGELINK-Wert kann ein lokaler Dateisystempfad oder eine URL sein.</span><span class="sxs-lookup"><span data-stu-id="eaae0-114">The imageLink value can be a local file system path or a URL.</span></span> <span data-ttu-id="eaae0-115">Die Bilddatei kann ein beliebiger grundlegender Bildtyp sein, der von Windows 7 unterstützt wird (PNG, BMP, JPG, GIF).</span><span class="sxs-lookup"><span data-stu-id="eaae0-115">The image file can be any of the basic image types supported by Windows 7 (PNG, BMP, JPG, GIF).</span></span>

## <a name="example-of-an-imagelink-element"></a><span data-ttu-id="eaae0-116">Beispiel für ein IMAGELINK-Element</span><span class="sxs-lookup"><span data-stu-id="eaae0-116">Example of an imageLink Element</span></span>


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



