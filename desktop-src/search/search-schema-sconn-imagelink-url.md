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
# <a name="imagelink-url-element-search-connector-schema"></a><span data-ttu-id="45900-105">IMAGELINK-URL-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="45900-105">imageLink url Element (Search Connector Schema)</span></span>

<span data-ttu-id="45900-106">Das- <url> Element gibt eine URL zur Miniaturansicht für diesen Suchconnector an.</span><span class="sxs-lookup"><span data-stu-id="45900-106">The <url> element specifies a URL to the thumbnail for this search connector.</span></span> <span data-ttu-id="45900-107">Wenn <imageLink> vorhanden ist, ist dieses Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="45900-107">If <imageLink> exists, this element is required.</span></span> <span data-ttu-id="45900-108">Sie verfügt über keine untergeordneten Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="45900-108">It has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="45900-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="45900-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="45900-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="45900-110">Element Information</span></span>



| <span data-ttu-id="45900-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="45900-111">Parent Element</span></span>                                                                   | <span data-ttu-id="45900-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45900-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="45900-113">IMAGELINK-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="45900-113">imageLink Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="45900-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45900-114">Remarks</span></span>

<span data-ttu-id="45900-115">Der Wert kann ein Pfad des lokalen Dateisystems oder eine URL sein.</span><span class="sxs-lookup"><span data-stu-id="45900-115">The value can be a local file system path or a URL.</span></span> <span data-ttu-id="45900-116">Die Bilddatei kann ein beliebiger grundlegender Bildtyp sein, der von Windows 7 unterstützt wird (PNG, BMP, JPG, GIF).</span><span class="sxs-lookup"><span data-stu-id="45900-116">The image file can be any of the basic image types supported by Windows 7 (PNG, BMP, JPG, GIF).</span></span>

## <a name="example-of-an-imagelinkurl-element"></a><span data-ttu-id="45900-117">Beispiel für ein imagelinkurl-Element</span><span class="sxs-lookup"><span data-stu-id="45900-117">Example of an imageLinkurl Element</span></span>


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



