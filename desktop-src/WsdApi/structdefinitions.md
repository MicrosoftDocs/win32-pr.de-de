---
description: Generiert C-Strukturdefinitionen für bekannte Typen.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: structdefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33ca9ac9ce3f9e868646c0bfff260238c30e572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373110"
---
# <a name="structdefinitions-element"></a><span data-ttu-id="d8e35-103">structdefinitions-Element</span><span class="sxs-lookup"><span data-stu-id="d8e35-103">structDefinitions element</span></span>

<span data-ttu-id="d8e35-104">Generiert C-Strukturdefinitionen für bekannte Typen.</span><span class="sxs-lookup"><span data-stu-id="d8e35-104">Generates C structure definitions for known types.</span></span>

## <a name="usage"></a><span data-ttu-id="d8e35-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="d8e35-105">Usage</span></span>

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a><span data-ttu-id="d8e35-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="d8e35-106">Attributes</span></span>

<span data-ttu-id="d8e35-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="d8e35-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d8e35-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d8e35-108">Child elements</span></span>

<span data-ttu-id="d8e35-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="d8e35-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d8e35-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d8e35-110">Parent elements</span></span>



| <span data-ttu-id="d8e35-111">Element</span><span class="sxs-lookup"><span data-stu-id="d8e35-111">Element</span></span>                         | <span data-ttu-id="d8e35-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8e35-112">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="d8e35-113">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d8e35-113">**file**</span></span>](file.md)<br/> | <span data-ttu-id="d8e35-114">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="d8e35-114">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d8e35-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8e35-115">Remarks</span></span>

<span data-ttu-id="d8e35-116">Auf Strukturen für bekannte Typen wird von einem Großteil des generierten Codes und des Anwendungs Codes verwiesen.</span><span class="sxs-lookup"><span data-stu-id="d8e35-116">Structures for known types are referenced by much of the generated code and by application code.</span></span> <span data-ttu-id="d8e35-117">Dieses Element wird zum Generieren von Include-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8e35-117">This element is used to generate include files.</span></span> <span data-ttu-id="d8e35-118">Dieses Element sollte nach einem [**struct-Deklarations**](structdeclarations.md) Element auftreten, sodass Verweise zwischen Strukturen ordnungsgemäß behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="d8e35-118">This element should occur after a [**structDeclarations**](structdeclarations.md) element so that references between structures are handled properly.</span></span>

## <a name="element-information"></a><span data-ttu-id="d8e35-119">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d8e35-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="d8e35-120">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="d8e35-120">Minimum supported system</span></span><br/> | <span data-ttu-id="d8e35-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8e35-121">Windows Vista</span></span> |
| <span data-ttu-id="d8e35-122">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="d8e35-122">Can be empty</span></span>                        | <span data-ttu-id="d8e35-123">Ja</span><span class="sxs-lookup"><span data-stu-id="d8e35-123">Yes</span></span>           |



 

 




