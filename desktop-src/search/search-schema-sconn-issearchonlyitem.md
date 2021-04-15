---
description: Das boolesche <isSearchOnlyItem> Element gibt an, ob der Suchanbieter zusätzlich zum Suchmodus den Durchsuchenmodus unterstützt. Dieses Element ist optional und verfügt über keine untergeordneten Elemente und keine Attribute.
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: issearchonlyitem-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded7b62cde5cf813603d5cc87c41fe2c443b42d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525454"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a><span data-ttu-id="e9899-104">issearchonlyitem-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="e9899-104">isSearchOnlyItem Element (Search Connector Schema)</span></span>

<span data-ttu-id="e9899-105">Das boolesche <isSearchOnlyItem> Element gibt an, ob der Suchanbieter zusätzlich zum Suchmodus den Durchsuchenmodus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9899-105">The Boolean <isSearchOnlyItem> element specifies whether the search provider supports browse mode in addition to search mode.</span></span> <span data-ttu-id="e9899-106">Dieses Element ist optional und verfügt über keine untergeordneten Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="e9899-106">This element is optional and has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9899-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9899-107">Syntax</span></span>


```
<!-- isSearchOnlyItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="e9899-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e9899-108">Element Information</span></span>



| <span data-ttu-id="e9899-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="e9899-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="e9899-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e9899-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="e9899-111">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="e9899-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="e9899-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9899-112">Remarks</span></span>

<span data-ttu-id="e9899-113">Der Wert `true` gibt an, dass der Suchconnector-Speicherort von Benutzern nicht durchsucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="e9899-113">The value `true` indicates that the search connector location cannot be browsed by users.</span></span> <span data-ttu-id="e9899-114">Der Wert `false` gibt an, dass Benutzer den Suchconnector-Speicherort durchsuchen können.</span><span class="sxs-lookup"><span data-stu-id="e9899-114">The value `false` indicates that users can browse the search connector location.</span></span>

## <a name="example"></a><span data-ttu-id="e9899-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e9899-115">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 



