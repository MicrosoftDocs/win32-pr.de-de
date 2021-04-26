---
description: Gibt den Downloadspeicherort für eine wsdl:import-Direktive an, die keinen Speicherort explizit angibt.
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: importHint-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c874879ee0a608c100f32a0520a85efe76080cc2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998757"
---
# <a name="importhint-element"></a><span data-ttu-id="4411c-103">importHint-Element</span><span class="sxs-lookup"><span data-stu-id="4411c-103">importHint element</span></span>

<span data-ttu-id="4411c-104">Gibt den Downloadspeicherort für eine \<wsdl:import> -Direktive an, die nicht explizit einen Speicherort angibt.</span><span class="sxs-lookup"><span data-stu-id="4411c-104">Specifies the download location for a \<wsdl:import> directive that does not explicitly specify a location.</span></span>

## <a name="usage"></a><span data-ttu-id="4411c-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="4411c-105">Usage</span></span>

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a><span data-ttu-id="4411c-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="4411c-106">Attributes</span></span>

<span data-ttu-id="4411c-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="4411c-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4411c-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4411c-108">Child elements</span></span>



| <span data-ttu-id="4411c-109">Element</span><span class="sxs-lookup"><span data-stu-id="4411c-109">Element</span></span>                                   | <span data-ttu-id="4411c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4411c-110">Description</span></span>                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4411c-111">**Lage**</span><span class="sxs-lookup"><span data-stu-id="4411c-111">**location**</span></span>](location.md)<br/>   | <span data-ttu-id="4411c-112">Der Speicherort der zu importierende Datei.</span><span class="sxs-lookup"><span data-stu-id="4411c-112">The location of the file to import.</span></span> <span data-ttu-id="4411c-113">Der Speicherort kann ein relativer Pfad, ein absoluter Pfad oder eine HTTP-URL sein.</span><span class="sxs-lookup"><span data-stu-id="4411c-113">The location may be a relative path, an absolute path, or an HTTP URL.</span></span><br/> <br/> |
| [<span data-ttu-id="4411c-114">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4411c-114">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="4411c-115">Der zu importierende Namespace.</span><span class="sxs-lookup"><span data-stu-id="4411c-115">The namespace to import.</span></span> <span data-ttu-id="4411c-116">Dies sollte mit dem im -Element angegebenen Namespace \<wsdl:import> übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="4411c-116">This should match the namespace specified in the \<wsdl:import> element.</span></span><br/> <br/>     |



### <a name="child-element-sequence"></a><span data-ttu-id="4411c-117">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="4411c-117">Child element sequence</span></span>

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a><span data-ttu-id="4411c-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4411c-118">Parent elements</span></span>



| <span data-ttu-id="4411c-119">Element</span><span class="sxs-lookup"><span data-stu-id="4411c-119">Element</span></span>                         | <span data-ttu-id="4411c-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4411c-120">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="4411c-121">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="4411c-121">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="4411c-122">Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4411c-122">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="4411c-123">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4411c-123">Element information</span></span>



| <span data-ttu-id="4411c-124">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="4411c-124">Label</span></span> | <span data-ttu-id="4411c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="4411c-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="4411c-126">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="4411c-126">Minimum supported system</span></span><br/> | <span data-ttu-id="4411c-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4411c-127">Windows Vista</span></span> |
| <span data-ttu-id="4411c-128">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="4411c-128">Can be empty</span></span>                        | <span data-ttu-id="4411c-129">Nein</span><span class="sxs-lookup"><span data-stu-id="4411c-129">No</span></span>            |



 

 




