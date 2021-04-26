---
description: Generiert Funktionen, um typierte Proxys zu erstellen.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: proxyBuilderImplementations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ad22348b33c60689adf60c029e3a08c2f4d417c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996467"
---
# <a name="proxybuilderimplementations-element"></a><span data-ttu-id="c2997-103">proxyBuilderImplementations-Element</span><span class="sxs-lookup"><span data-stu-id="c2997-103">proxyBuilderImplementations element</span></span>

<span data-ttu-id="c2997-104">Generiert Funktionen, um typierte Proxys zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2997-104">Generates functions to create typed proxies.</span></span>

## <a name="usage"></a><span data-ttu-id="c2997-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="c2997-105">Usage</span></span>

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a><span data-ttu-id="c2997-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="c2997-106">Attributes</span></span>

<span data-ttu-id="c2997-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="c2997-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c2997-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c2997-108">Child elements</span></span>



| <span data-ttu-id="c2997-109">Element</span><span class="sxs-lookup"><span data-stu-id="c2997-109">Element</span></span>                                     | <span data-ttu-id="c2997-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2997-110">Description</span></span>                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2997-111">**Codename**</span><span class="sxs-lookup"><span data-stu-id="c2997-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="c2997-112">Der Name, der für den Porttyp im generierten Code verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2997-112">The name to be used for the port type in the generated code.</span></span> <span data-ttu-id="c2997-113">Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.</span><span class="sxs-lookup"><span data-stu-id="c2997-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="c2997-114">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="c2997-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="c2997-115">Porttyp, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2997-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                             |
| [<span data-ttu-id="c2997-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="c2997-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="c2997-117">Klassenname, der aus der Proxy-Generatorfunktion generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2997-117">Class name to generate from the proxy builder function.</span></span><br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="c2997-118">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="c2997-118">Child element sequence</span></span>

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a><span data-ttu-id="c2997-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c2997-119">Parent elements</span></span>



| <span data-ttu-id="c2997-120">Element</span><span class="sxs-lookup"><span data-stu-id="c2997-120">Element</span></span>                         | <span data-ttu-id="c2997-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2997-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="c2997-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c2997-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="c2997-123">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="c2997-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="c2997-124">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c2997-124">Element information</span></span>



| <span data-ttu-id="c2997-125">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="c2997-125">Label</span></span> | <span data-ttu-id="c2997-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c2997-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="c2997-127">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="c2997-127">Minimum supported system</span></span><br/> | <span data-ttu-id="c2997-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2997-128">Windows Vista</span></span> |
| <span data-ttu-id="c2997-129">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="c2997-129">Can be empty</span></span>                        | <span data-ttu-id="c2997-130">Nein</span><span class="sxs-lookup"><span data-stu-id="c2997-130">No</span></span>            |



 

 




