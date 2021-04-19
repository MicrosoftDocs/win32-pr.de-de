---
description: Generiert Funktionen zum Erstellen typisierter Proxys.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: proxybuilderimplementierungen-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2cb64a6ea87b1083871931359a4f7c01ece9b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352234"
---
# <a name="proxybuilderimplementations-element"></a><span data-ttu-id="f330e-103">proxybuilderimplementierungen-Element</span><span class="sxs-lookup"><span data-stu-id="f330e-103">proxyBuilderImplementations element</span></span>

<span data-ttu-id="f330e-104">Generiert Funktionen zum Erstellen typisierter Proxys.</span><span class="sxs-lookup"><span data-stu-id="f330e-104">Generates functions to create typed proxies.</span></span>

## <a name="usage"></a><span data-ttu-id="f330e-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="f330e-105">Usage</span></span>

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a><span data-ttu-id="f330e-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="f330e-106">Attributes</span></span>

<span data-ttu-id="f330e-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="f330e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f330e-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f330e-108">Child elements</span></span>



| <span data-ttu-id="f330e-109">Element</span><span class="sxs-lookup"><span data-stu-id="f330e-109">Element</span></span>                                     | <span data-ttu-id="f330e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f330e-110">Description</span></span>                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f330e-111">**codeName**</span><span class="sxs-lookup"><span data-stu-id="f330e-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="f330e-112">Der Name, der für den Porttyp im generierten Code verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f330e-112">The name to be used for the port type in the generated code.</span></span> <span data-ttu-id="f330e-113">Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.</span><span class="sxs-lookup"><span data-stu-id="f330e-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="f330e-114">**PortType**</span><span class="sxs-lookup"><span data-stu-id="f330e-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="f330e-115">Der Porttyp, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f330e-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                             |
| [<span data-ttu-id="f330e-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="f330e-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="f330e-117">Der Klassenname, der aus der Proxy Generatorfunktion generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f330e-117">Class name to generate from the proxy builder function.</span></span><br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="f330e-118">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="f330e-118">Child element sequence</span></span>

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a><span data-ttu-id="f330e-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f330e-119">Parent elements</span></span>



| <span data-ttu-id="f330e-120">Element</span><span class="sxs-lookup"><span data-stu-id="f330e-120">Element</span></span>                         | <span data-ttu-id="f330e-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f330e-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="f330e-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="f330e-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="f330e-123">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="f330e-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="f330e-124">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f330e-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="f330e-125">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="f330e-125">Minimum supported system</span></span><br/> | <span data-ttu-id="f330e-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f330e-126">Windows Vista</span></span> |
| <span data-ttu-id="f330e-127">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="f330e-127">Can be empty</span></span>                        | <span data-ttu-id="f330e-128">Nein</span><span class="sxs-lookup"><span data-stu-id="f330e-128">No</span></span>            |



 

 




