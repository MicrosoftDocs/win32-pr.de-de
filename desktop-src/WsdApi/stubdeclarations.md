---
description: Generiert Deklarationen für Stubfunktionen für Porttypvorgänge.
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: stubDeclarations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1543883b4d41e7571cd4a4725e2aeab181530d30
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996407"
---
# <a name="stubdeclarations-element"></a><span data-ttu-id="c4cf6-103">stubDeclarations-Element</span><span class="sxs-lookup"><span data-stu-id="c4cf6-103">stubDeclarations element</span></span>

<span data-ttu-id="c4cf6-104">Generiert Deklarationen für Stubfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="c4cf6-104">Generates declarations for stub functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="c4cf6-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="c4cf6-105">Usage</span></span>

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="c4cf6-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="c4cf6-106">Attributes</span></span>

<span data-ttu-id="c4cf6-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="c4cf6-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c4cf6-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4cf6-108">Child elements</span></span>



| <span data-ttu-id="c4cf6-109">Element</span><span class="sxs-lookup"><span data-stu-id="c4cf6-109">Element</span></span>                                   | <span data-ttu-id="c4cf6-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4cf6-110">Description</span></span>                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4cf6-111">**events**</span><span class="sxs-lookup"><span data-stu-id="c4cf6-111">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="c4cf6-112">Gibt an, ob verknüpfte Ereignisse in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c4cf6-112">Specifies whether related events are included in the generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="c4cf6-113">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="c4cf6-113">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="c4cf6-114">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4cf6-114">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                 |
| [<span data-ttu-id="c4cf6-115">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="c4cf6-115">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="c4cf6-116">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4cf6-116">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                |



### <a name="child-element-sequence"></a><span data-ttu-id="c4cf6-117">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="c4cf6-117">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?
)
```

## <a name="parent-elements"></a><span data-ttu-id="c4cf6-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4cf6-118">Parent elements</span></span>



| <span data-ttu-id="c4cf6-119">Element</span><span class="sxs-lookup"><span data-stu-id="c4cf6-119">Element</span></span>                         | <span data-ttu-id="c4cf6-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4cf6-120">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="c4cf6-121">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c4cf6-121">**file**</span></span>](file.md)<br/> | <span data-ttu-id="c4cf6-122">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="c4cf6-122">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="c4cf6-123">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c4cf6-123">Element information</span></span>



| <span data-ttu-id="c4cf6-124">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="c4cf6-124">Label</span></span> | <span data-ttu-id="c4cf6-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c4cf6-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="c4cf6-126">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="c4cf6-126">Minimum supported system</span></span><br/> | <span data-ttu-id="c4cf6-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4cf6-127">Windows Vista</span></span> |
| <span data-ttu-id="c4cf6-128">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="c4cf6-128">Can be empty</span></span>                        | <span data-ttu-id="c4cf6-129">Ja</span><span class="sxs-lookup"><span data-stu-id="c4cf6-129">Yes</span></span>           |



 

 




