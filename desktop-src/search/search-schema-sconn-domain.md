---
description: Das optionale- <domain> Element gibt die URL des Such Dienstanbieter an, der von diesem Suchconnector verwendet wird. Er wird im Detailfenster angezeigt. Dieses Element hat keine untergeordneten Elemente und keine Attribute.
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: Domain-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b57819cf485bccbe63e7560f3fcb92811d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862147"
---
# <a name="domain-element-search-connector-schema"></a><span data-ttu-id="76f64-105">Domain-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="76f64-105">domain Element (Search Connector Schema)</span></span>

<span data-ttu-id="76f64-106">Das optionale- <domain> Element gibt die URL des Such Dienstanbieter an, der von diesem Suchconnector verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76f64-106">The optional <domain> element specifies the URL of the search service used by this search connector.</span></span> <span data-ttu-id="76f64-107">Er wird im Detailfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76f64-107">It is displayed in the details pane.</span></span> <span data-ttu-id="76f64-108">Dieses Element hat keine untergeordneten Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="76f64-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="76f64-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="76f64-109">Syntax</span></span>


```
<!-- domain -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="domain" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="76f64-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="76f64-110">Element Information</span></span>



| <span data-ttu-id="76f64-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="76f64-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="76f64-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76f64-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="76f64-113">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="76f64-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="76f64-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76f64-114">Remarks</span></span>

<span data-ttu-id="76f64-115">Die URL sollte die Domäne der obersten Ebene für den Suchanbieter sein.</span><span class="sxs-lookup"><span data-stu-id="76f64-115">The URL should be the top-level domain for the search provider.</span></span> <span data-ttu-id="76f64-116">Beispiel: https://www.example.com.</span><span class="sxs-lookup"><span data-stu-id="76f64-116">For example, https://www.example.com.</span></span>

## <a name="example"></a><span data-ttu-id="76f64-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="76f64-117">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 



