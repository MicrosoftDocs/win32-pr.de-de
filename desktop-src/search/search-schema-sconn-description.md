---
description: Der optionale <description> das-Element gibt eine Beschreibung für diesen Suchconnector an. Dieses Element hat keine untergeordneten Elemente und keine Attribute.
ms.assetid: 0e9d806c-7dfd-4e7f-8843-15a4e22f317f
title: Description-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9d82fd6ad3ae45c4a8c3700c4822387a81880d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342919"
---
# <a name="description-element-search-connector-schema"></a><span data-ttu-id="629ca-105">Description-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="629ca-105">description Element (Search Connector Schema)</span></span>

<span data-ttu-id="629ca-106">Der optionale</span><span class="sxs-lookup"><span data-stu-id="629ca-106">The optional</span></span> <description> <span data-ttu-id="629ca-107">das-Element gibt eine Beschreibung für diesen Suchconnector an.</span><span class="sxs-lookup"><span data-stu-id="629ca-107">element specifies a description for this search connector.</span></span> <span data-ttu-id="629ca-108">Dieses Element hat keine untergeordneten Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="629ca-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="629ca-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="629ca-109">Syntax</span></span>


```
<!-- description -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="description" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="629ca-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="629ca-110">Element Information</span></span>



| <span data-ttu-id="629ca-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="629ca-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="629ca-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="629ca-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="629ca-113">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="629ca-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="629ca-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="629ca-114">Remarks</span></span>

<span data-ttu-id="629ca-115">Die Beschreibung sollte benutzerfreundlich sein, da Sie in Quick Infos verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="629ca-115">The description should be user-friendly as it may be used in tooltips.</span></span>

## <a name="example"></a><span data-ttu-id="629ca-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="629ca-116">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <description>Search AdventureWorks.com</description>
    ...
</searchConnectionDescription>
```



 

 



