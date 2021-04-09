---
description: Das optionale boolesche <isIndexed> Element gibt an, ob der vom Suchconnector beschriebene Speicherort indiziert wird (entweder lokal oder Remote mit Windows Search 4 oder höher).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: isinentxed-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f658f6b932f6241b7af84e763d564ca0a8f1b5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128496"
---
# <a name="isindexed-element-search-connector-schema"></a><span data-ttu-id="a2d3d-103">isinentxed-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="a2d3d-103">isIndexed Element (Search Connector Schema)</span></span>

<span data-ttu-id="a2d3d-104">Das optionale boolesche <isIndexed> Element gibt an, ob der vom Suchconnector beschriebene Speicherort indiziert wird (entweder lokal oder Remote mit Windows Search 4 oder höher).</span><span class="sxs-lookup"><span data-stu-id="a2d3d-104">The optional Boolean <isIndexed> element specifies whether the location described by the search connector is indexed (either locally or remotely using Windows Search 4 or higher).</span></span> <span data-ttu-id="a2d3d-105">Der Standardwert ist true für lokale Ordner.</span><span class="sxs-lookup"><span data-stu-id="a2d3d-105">The default value is true for local folders.</span></span> <span data-ttu-id="a2d3d-106">Dieses Element hat keine untergeordneten Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="a2d3d-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2d3d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2d3d-107">Syntax</span></span>


```
<!-- isIndexed -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isIndexed" type="xsIboolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="a2d3d-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a2d3d-108">Element Information</span></span>



| <span data-ttu-id="a2d3d-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="a2d3d-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="a2d3d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a2d3d-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="a2d3d-111">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="a2d3d-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a><span data-ttu-id="a2d3d-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a2d3d-112">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <isIndexed>false</isIndexed>
    ...
</searchConnectionDescription>
```



 

 



