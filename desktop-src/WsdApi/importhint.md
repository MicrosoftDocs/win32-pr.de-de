---
description: Gibt den Downloadspeicherort für eine wsdl:import-Direktive an, die keinen Speicherort explizit angibt.
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: importHint-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29fcd65f9af02b8077ba828081ac9ed767d64e3
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380654"
---
# <a name="importhint-element"></a><span data-ttu-id="9cb12-103">importHint-Element</span><span class="sxs-lookup"><span data-stu-id="9cb12-103">importHint element</span></span>

<span data-ttu-id="9cb12-104">Gibt den Downloadspeicherort für eine \<wsdl:import> -Direktive an, die nicht explizit einen Speicherort angibt.</span><span class="sxs-lookup"><span data-stu-id="9cb12-104">Specifies the download location for a \<wsdl:import> directive that does not explicitly specify a location.</span></span>

## <a name="usage"></a><span data-ttu-id="9cb12-105">Verwendung</span><span class="sxs-lookup"><span data-stu-id="9cb12-105">Usage</span></span>

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a><span data-ttu-id="9cb12-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="9cb12-106">Attributes</span></span>

<span data-ttu-id="9cb12-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="9cb12-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9cb12-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9cb12-108">Child elements</span></span>



| <span data-ttu-id="9cb12-109">Element</span><span class="sxs-lookup"><span data-stu-id="9cb12-109">Element</span></span>                                   | <span data-ttu-id="9cb12-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cb12-110">Description</span></span>                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9cb12-111">**Lage**</span><span class="sxs-lookup"><span data-stu-id="9cb12-111">**location**</span></span>](location.md)<br/>   | <span data-ttu-id="9cb12-112">Der Speicherort der zu importierende Datei.</span><span class="sxs-lookup"><span data-stu-id="9cb12-112">The location of the file to import.</span></span> <span data-ttu-id="9cb12-113">Der Speicherort kann ein relativer Pfad, ein absoluter Pfad oder eine HTTP-URL sein.</span><span class="sxs-lookup"><span data-stu-id="9cb12-113">The location may be a relative path, an absolute path, or an HTTP URL.</span></span><br/> <br/> |
| [<span data-ttu-id="9cb12-114">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9cb12-114">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="9cb12-115">Der zu importierende Namespace.</span><span class="sxs-lookup"><span data-stu-id="9cb12-115">The namespace to import.</span></span> <span data-ttu-id="9cb12-116">Dies sollte mit dem im -Element angegebenen Namespace \<wsdl:import> übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9cb12-116">This should match the namespace specified in the \<wsdl:import> element.</span></span><br/> <br/>     |



### <a name="child-element-sequence"></a><span data-ttu-id="9cb12-117">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="9cb12-117">Child element sequence</span></span>

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a><span data-ttu-id="9cb12-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9cb12-118">Parent elements</span></span>



| <span data-ttu-id="9cb12-119">Element</span><span class="sxs-lookup"><span data-stu-id="9cb12-119">Element</span></span>                         | <span data-ttu-id="9cb12-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cb12-120">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="9cb12-121">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="9cb12-121">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="9cb12-122">Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9cb12-122">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="9cb12-123">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9cb12-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="9cb12-124">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="9cb12-124">Minimum supported system</span></span><br/> | <span data-ttu-id="9cb12-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cb12-125">Windows Vista</span></span> |
| <span data-ttu-id="9cb12-126">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="9cb12-126">Can be empty</span></span>                        | <span data-ttu-id="9cb12-127">Nein</span><span class="sxs-lookup"><span data-stu-id="9cb12-127">No</span></span>            |



 

 




