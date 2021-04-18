---
description: Das boolesche <supportsAdvancedQuerySyntax> Element gibt an, ob der Suchanbieter die Erweiterte Abfrage Syntax unterstützt. Die Standardeinstellung ist „false“. Dieses Element ist optional und verfügt über keine untergeordneten Elemente und keine Attribute.
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: supportsadvancedquerysyntax-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d31eb96615c952f703729fd9d22f2e5d27f38b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341185"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a><span data-ttu-id="a2283-105">supportsadvancedquerysyntax-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="a2283-105">supportsAdvancedQuerySyntax Element (Search Connector Schema)</span></span>

<span data-ttu-id="a2283-106">Das boolesche <supportsAdvancedQuerySyntax> Element gibt an, ob der Suchanbieter die [Erweiterte Abfrage Syntax](-search-3x-advancedquerysyntax.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a2283-106">The Boolean <supportsAdvancedQuerySyntax> element specifies whether the search provider supports the [Advanced Query Syntax](-search-3x-advancedquerysyntax.md).</span></span> <span data-ttu-id="a2283-107">Die Standardeinstellung ist „false“.</span><span class="sxs-lookup"><span data-stu-id="a2283-107">The default is false.</span></span> <span data-ttu-id="a2283-108">Dieses Element ist optional und verfügt über keine untergeordneten Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="a2283-108">This element is optional and has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2283-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2283-109">Syntax</span></span>


```
<!-- supportsAdvancedQuerySyntax -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="a2283-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a2283-110">Element Information</span></span>



| <span data-ttu-id="a2283-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="a2283-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="a2283-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a2283-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="a2283-113">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="a2283-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="a2283-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2283-114">Remarks</span></span>

<span data-ttu-id="a2283-115">Der Wert `true` gibt an, dass der Suchanbieter Erweiterte Abfrage Syntax unterstützt, die in Such Abfragen gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2283-115">The value `true` indicates that the search provider supports Advanced Query Syntax sent in search queries.</span></span>

## <a name="example"></a><span data-ttu-id="a2283-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a2283-116">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <supportsAdvancedQuerySyntax>true</supportsAdvancedQuerySyntax>
    ...
</searchConnectionDescription>
```



 

 



