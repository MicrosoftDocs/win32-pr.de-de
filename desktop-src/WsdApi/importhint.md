---
description: 'Gibt den Download Speicherort für eine <WSDL: Import-> Direktive an, die nicht explizit einen Speicherort angibt.'
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: importhint-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce8da0a7fa45ed00489d405aaba8f1f6d7ab8fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347911"
---
# <a name="importhint-element"></a><span data-ttu-id="09045-103">importhint-Element</span><span class="sxs-lookup"><span data-stu-id="09045-103">importHint element</span></span>

<span data-ttu-id="09045-104">Gibt den Download Speicherort für eine <WSDL: Import-> Direktive an, die nicht explizit einen Speicherort angibt.</span><span class="sxs-lookup"><span data-stu-id="09045-104">Specifies the download location for a <wsdl:import> directive that does not explicitly specify a location.</span></span>

## <a name="usage"></a><span data-ttu-id="09045-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="09045-105">Usage</span></span>

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a><span data-ttu-id="09045-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="09045-106">Attributes</span></span>

<span data-ttu-id="09045-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="09045-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="09045-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="09045-108">Child elements</span></span>



| <span data-ttu-id="09045-109">Element</span><span class="sxs-lookup"><span data-stu-id="09045-109">Element</span></span>                                   | <span data-ttu-id="09045-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09045-110">Description</span></span>                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09045-111">**location**</span><span class="sxs-lookup"><span data-stu-id="09045-111">**location**</span></span>](location.md)<br/>   | <span data-ttu-id="09045-112">Der Speicherort der zu importierenden Datei.</span><span class="sxs-lookup"><span data-stu-id="09045-112">The location of the file to import.</span></span> <span data-ttu-id="09045-113">Der Speicherort kann ein relativer Pfad, ein absoluter Pfad oder eine HTTP-URL sein.</span><span class="sxs-lookup"><span data-stu-id="09045-113">The location may be a relative path, an absolute path, or an HTTP URL.</span></span><br/> <br/> |
| [<span data-ttu-id="09045-114">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="09045-114">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="09045-115">Der zu importierende Namespace.</span><span class="sxs-lookup"><span data-stu-id="09045-115">The namespace to import.</span></span> <span data-ttu-id="09045-116">Dies sollte dem im <WSDL: Import>-Element angegebenen Namespace entsprechen.</span><span class="sxs-lookup"><span data-stu-id="09045-116">This should match the namespace specified in the <wsdl:import> element.</span></span><br/> <br/>     |



### <a name="child-element-sequence"></a><span data-ttu-id="09045-117">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="09045-117">Child element sequence</span></span>

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a><span data-ttu-id="09045-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="09045-118">Parent elements</span></span>



| <span data-ttu-id="09045-119">Element</span><span class="sxs-lookup"><span data-stu-id="09045-119">Element</span></span>                         | <span data-ttu-id="09045-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09045-120">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="09045-121">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="09045-121">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="09045-122">Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="09045-122">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="09045-123">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="09045-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="09045-124">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="09045-124">Minimum supported system</span></span><br/> | <span data-ttu-id="09045-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09045-125">Windows Vista</span></span> |
| <span data-ttu-id="09045-126">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="09045-126">Can be empty</span></span>                        | <span data-ttu-id="09045-127">Nein</span><span class="sxs-lookup"><span data-stu-id="09045-127">No</span></span>            |



 

 




