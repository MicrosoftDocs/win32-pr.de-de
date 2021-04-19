---
description: Gibt einen Sortierungs Alias oder eine Liste von Sortier Aliasen an, indem ein Element angegeben wird, das eine Sortier Eigenschaft oder eine Liste von Sortier Eigenschaften enthält.
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: aliasInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052409864617bdaba7acbf9ae561752c83d18395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372970"
---
# <a name="aliasinfo"></a><span data-ttu-id="105fc-103">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="105fc-103">aliasInfo</span></span>

<span data-ttu-id="105fc-104">Gibt einen Sortierungs Alias oder eine Liste von Sortier Aliasen an, indem ein Element angegeben wird, das eine Sortier Eigenschaft oder eine Liste von Sortier Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="105fc-104">Specifies a sort alias or list of sort aliases by specifying an element that contains a sort property or list of sort properties.</span></span> <span data-ttu-id="105fc-105">Es darf nur ein [AliasInfo]() -Element für jedes [propertydescription](./propdesc-schema-propertydescription.md) -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="105fc-105">There should be only one [aliasInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span> <span data-ttu-id="105fc-106">Bei Eigenschaften, bei denen cangroupby = true festgelegt ist, kann es beim aliasInfo/@additionalSortByAliases Ändern der Sortierreihenfolge in einer Ansicht, die nach der-Eigenschaft gruppiert ist, zu unerwartetem Verhalten kommen, es sei denn, es wird eine sekundäre Sortier Eigenschaft angegeben (= prop: example)</span><span class="sxs-lookup"><span data-stu-id="105fc-106">For properties that set canGroupBy=true, unless a secondary sort property is specified (aliasInfo/@additionalSortByAliases=prop:example), the user may experience unexpected behavior when changing the sort order in a view that is grouped by the property.</span></span> <span data-ttu-id="105fc-107">Insbesondere wird die Reihenfolge der Gruppen geändert, aber die Reihenfolge der Elemente in den Gruppen ist nicht.</span><span class="sxs-lookup"><span data-stu-id="105fc-107">Specifically, the order of the groups will change, but the order of items within the groups will not.</span></span>

## <a name="syntax"></a><span data-ttu-id="105fc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="105fc-108">Syntax</span></span>


```
<!-- aliasInfo -->
<xs:element name="aliasInfo">
    <xs:complexType>
        <xs:attribute name="sortByAlias" type="canonical-name"/>
        <xs:attribute name="additionalSortByAliases" type="proplist"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="105fc-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="105fc-109">Element Information</span></span>



| <span data-ttu-id="105fc-110">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="105fc-110">Parent Element</span></span>                                                   | <span data-ttu-id="105fc-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="105fc-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="105fc-112">propertydescription</span><span class="sxs-lookup"><span data-stu-id="105fc-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="105fc-113">Keine</span><span class="sxs-lookup"><span data-stu-id="105fc-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="105fc-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="105fc-114">Attributes</span></span>



| <span data-ttu-id="105fc-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="105fc-115">Attribute</span></span>               | <span data-ttu-id="105fc-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="105fc-116">Description</span></span>                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="105fc-117">sortbyalias</span><span class="sxs-lookup"><span data-stu-id="105fc-117">sortByAlias</span></span>             | <span data-ttu-id="105fc-118">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="105fc-118">Public.</span></span> <span data-ttu-id="105fc-119">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="105fc-119">Optional.</span></span> <span data-ttu-id="105fc-120">Der kanonische Name der Eigenschaft, die zum Sortieren nach verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="105fc-120">The canonical name of the property that should be used to sort by.</span></span> <span data-ttu-id="105fc-121">Diese Zeichenfolge ist vom Typ "Canonical-Type".</span><span class="sxs-lookup"><span data-stu-id="105fc-121">This string is of type canonical-type.</span></span>                                            |
| <span data-ttu-id="105fc-122">additionalsortbyaliases</span><span class="sxs-lookup"><span data-stu-id="105fc-122">additionalSortByAliases</span></span> | <span data-ttu-id="105fc-123">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="105fc-123">Public.</span></span> <span data-ttu-id="105fc-124">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="105fc-124">Optional.</span></span> <span data-ttu-id="105fc-125">Eine durch Semikolons getrennte Liste der zusätzlichen Eigenschaften, die beim Sortieren verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="105fc-125">A semi-colon delimited list of additional properties to be used when sorting.</span></span> <span data-ttu-id="105fc-126">Die Eigenschaften werden auf die Sortierreihenfolge in der von Ihnen angegebenen Reihenfolge angewendet.</span><span class="sxs-lookup"><span data-stu-id="105fc-126">The properties are applied to the sort in the sequence they are given.</span></span> |



 

 

 
