---
description: Generiert Deklarationen für Stub-Funktionen für Porttyp Vorgänge.
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: Stub-Deklarations Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ceaa8871928031edff90db0491483cfd06bdcc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363812"
---
# <a name="stubdeclarations-element"></a><span data-ttu-id="38670-103">Stub-Deklarations Element</span><span class="sxs-lookup"><span data-stu-id="38670-103">stubDeclarations element</span></span>

<span data-ttu-id="38670-104">Generiert Deklarationen für Stub-Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="38670-104">Generates declarations for stub functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="38670-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="38670-105">Usage</span></span>

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="38670-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="38670-106">Attributes</span></span>

<span data-ttu-id="38670-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="38670-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="38670-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38670-108">Child elements</span></span>



| <span data-ttu-id="38670-109">Element</span><span class="sxs-lookup"><span data-stu-id="38670-109">Element</span></span>                                   | <span data-ttu-id="38670-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38670-110">Description</span></span>                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38670-111">**events**</span><span class="sxs-lookup"><span data-stu-id="38670-111">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="38670-112">Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="38670-112">Specifies whether related events are included in the generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="38670-113">**Betriebs**</span><span class="sxs-lookup"><span data-stu-id="38670-113">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="38670-114">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="38670-114">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                 |
| [<span data-ttu-id="38670-115">**PortType**</span><span class="sxs-lookup"><span data-stu-id="38670-115">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="38670-116">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="38670-116">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                |



### <a name="child-element-sequence"></a><span data-ttu-id="38670-117">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="38670-117">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?
)
```

## <a name="parent-elements"></a><span data-ttu-id="38670-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38670-118">Parent elements</span></span>



| <span data-ttu-id="38670-119">Element</span><span class="sxs-lookup"><span data-stu-id="38670-119">Element</span></span>                         | <span data-ttu-id="38670-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38670-120">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="38670-121">**Datei**</span><span class="sxs-lookup"><span data-stu-id="38670-121">**file**</span></span>](file.md)<br/> | <span data-ttu-id="38670-122">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="38670-122">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="38670-123">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="38670-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="38670-124">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="38670-124">Minimum supported system</span></span><br/> | <span data-ttu-id="38670-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38670-125">Windows Vista</span></span> |
| <span data-ttu-id="38670-126">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="38670-126">Can be empty</span></span>                        | <span data-ttu-id="38670-127">Ja</span><span class="sxs-lookup"><span data-stu-id="38670-127">Yes</span></span>           |



 

 




