---
description: Generiert eine Deklaration für eine Funktion, mit der ein typisierter Host erstellt wird.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: hostbuilderdeclaration-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16576050efc76264f42dff6a19549f69933185b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352503"
---
# <a name="hostbuilderdeclaration-element"></a><span data-ttu-id="4aebb-103">hostbuilderdeclaration-Element</span><span class="sxs-lookup"><span data-stu-id="4aebb-103">hostBuilderDeclaration element</span></span>

<span data-ttu-id="4aebb-104">Generiert eine Deklaration für eine Funktion, mit der ein typisierter Host erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4aebb-104">Generates a declaration for a function that creates a typed host.</span></span>

## <a name="usage"></a><span data-ttu-id="4aebb-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="4aebb-105">Usage</span></span>

``` syntax
<hostBuilderDeclaration>
  child elements
</hostBuilderDeclaration>
```

## <a name="attributes"></a><span data-ttu-id="4aebb-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="4aebb-106">Attributes</span></span>

<span data-ttu-id="4aebb-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="4aebb-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4aebb-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4aebb-108">Child elements</span></span>



| <span data-ttu-id="4aebb-109">Element</span><span class="sxs-lookup"><span data-stu-id="4aebb-109">Element</span></span>                                   | <span data-ttu-id="4aebb-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4aebb-110">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4aebb-111">**Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4aebb-111">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="4aebb-112">Der Name der Dienst Schnittstelle, die für den Host eingeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4aebb-112">The name of service interface to be included for host.</span></span> <span data-ttu-id="4aebb-113">Der Wert dieses Elements muss mit dem Wert des untergeordneten [**Schnitt**](interface.md) stellen-Elements von " [**hustedservice**](hostedservice.md)" identisch sein.</span><span class="sxs-lookup"><span data-stu-id="4aebb-113">The value of this element must match the value of the [**interface**](interface.md) child element of [**hostedService**](hostedservice.md).</span></span> <br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="4aebb-114">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="4aebb-114">Child element sequence</span></span>

``` syntax
interface+
```

## <a name="parent-elements"></a><span data-ttu-id="4aebb-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4aebb-115">Parent elements</span></span>



| <span data-ttu-id="4aebb-116">Element</span><span class="sxs-lookup"><span data-stu-id="4aebb-116">Element</span></span>                         | <span data-ttu-id="4aebb-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4aebb-117">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="4aebb-118">**Datei**</span><span class="sxs-lookup"><span data-stu-id="4aebb-118">**file**</span></span>](file.md)<br/> | <span data-ttu-id="4aebb-119">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="4aebb-119">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="4aebb-120">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4aebb-120">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="4aebb-121">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="4aebb-121">Minimum supported system</span></span><br/> | <span data-ttu-id="4aebb-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4aebb-122">Windows Vista</span></span> |
| <span data-ttu-id="4aebb-123">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="4aebb-123">Can be empty</span></span>                        | <span data-ttu-id="4aebb-124">Nein</span><span class="sxs-lookup"><span data-stu-id="4aebb-124">No</span></span>            |



 

 




