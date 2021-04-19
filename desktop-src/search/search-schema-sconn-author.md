---
description: Das optionale- <author> Element gibt den Autor dieser Bibliothek an. Dieses Element hat keine untergeordneten Elemente und keine Attribute.
ms.assetid: c91042d5-9564-463a-9104-97b927027fc9
title: Author-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a2facbf4e3fa743b4dbe56a1c83eb57509c067
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346076"
---
# <a name="author-element-search-connector-schema"></a><span data-ttu-id="45cc5-104">Author-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="45cc5-104">author Element (Search Connector Schema)</span></span>

<span data-ttu-id="45cc5-105">Das optionale- <author> Element gibt den Autor dieser Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="45cc5-105">The optional <author> element specifies the author of this library.</span></span> <span data-ttu-id="45cc5-106">Dieses Element hat keine untergeordneten Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="45cc5-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="45cc5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="45cc5-107">Syntax</span></span>


```
<!-- author -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="author" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="45cc5-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="45cc5-108">Element Information</span></span>



| <span data-ttu-id="45cc5-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="45cc5-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="45cc5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45cc5-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="45cc5-111">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="45cc5-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a><span data-ttu-id="45cc5-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="45cc5-112">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <author>Joe Smith</author>
    ...
</searchConnectionDescription>
```



 

 



