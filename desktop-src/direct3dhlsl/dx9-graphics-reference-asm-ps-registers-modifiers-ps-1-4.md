---
title: PS \_ 1 \_ 4-quellregistrierungs modifiziererer für texld, texcrd
description: Zwei Pixel-Shader Version 1 \_ 4 Textur Adress Anweisungen, texld-PS \_ 1 \_ 4 und texcrd-PS, haben eine benutzerdefinierte Syntax.
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af2097ee682aec7da0ca36df9e4b465fb360f814
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/27/2019
ms.locfileid: "104101142"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a><span data-ttu-id="8b83e-103">PS \_ 1 \_ 4-quellregistrierungs modifiziererer für texld, texcrd</span><span class="sxs-lookup"><span data-stu-id="8b83e-103">ps\_1\_4 source register modifiers for texld, texcrd</span></span>

<span data-ttu-id="8b83e-104">Zwei Pixel-Shader Version 1 \_ 4 Textur Adress Anweisungen, [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) und [texcrd-PS](texcrd---ps.md), haben eine benutzerdefinierte Syntax.</span><span class="sxs-lookup"><span data-stu-id="8b83e-104">Two pixel shader version 1\_4 texture address instructions, [texld - ps\_1\_4](texld---ps-1-4.md) and [texcrd - ps](texcrd---ps.md), have custom syntax.</span></span> <span data-ttu-id="8b83e-105">Diese Anweisungen unterstützen Ihren eigenen Satz von Quell Registrierungs Modifizierern, Quell Registrierungs-Selectors und Ziel-Register-Schreib Masken, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8b83e-105">These instructions support their own set of source register modifiers, source register selectors, and destination-register write masks, as shown here.</span></span>

## <a name="source-register-modifiers-for-texld-and-texcrd"></a><span data-ttu-id="8b83e-106">Quellregistrierungs modifiziererer für texld und texcrd</span><span class="sxs-lookup"><span data-stu-id="8b83e-106">Source Register Modifiers for texld and texcrd</span></span>

<span data-ttu-id="8b83e-107">Diese Modifizierer stellen eine Projective Teilungs Funktionalität bereit, indem die x-und y-Werte durch die z-oder w-Werte aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="8b83e-107">These modifiers provide projective divide functionality by dividing the x and y values by either the z or w values.</span></span>



| <span data-ttu-id="8b83e-108">Quellregistrierungs modifiziererer</span><span class="sxs-lookup"><span data-stu-id="8b83e-108">Source register modifiers</span></span> | <span data-ttu-id="8b83e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b83e-109">Description</span></span>                | <span data-ttu-id="8b83e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b83e-110">Syntax</span></span>       |
|---------------------------|----------------------------|--------------|
| <span data-ttu-id="8b83e-111">\_DZ</span><span class="sxs-lookup"><span data-stu-id="8b83e-111">\_dz</span></span>                      | <span data-ttu-id="8b83e-112">Dividieren von x, y-Komponenten durch z</span><span class="sxs-lookup"><span data-stu-id="8b83e-112">Divide x,y components by z</span></span> | <span data-ttu-id="8b83e-113">Registrieren von \_ DZ</span><span class="sxs-lookup"><span data-stu-id="8b83e-113">register\_dz</span></span> |
| <span data-ttu-id="8b83e-114">\_db</span><span class="sxs-lookup"><span data-stu-id="8b83e-114">\_db</span></span>                      | <span data-ttu-id="8b83e-115">Dividieren von x, y-Komponenten durch z</span><span class="sxs-lookup"><span data-stu-id="8b83e-115">Divide x,y components by z</span></span> | <span data-ttu-id="8b83e-116">Datenbank \_ registrieren</span><span class="sxs-lookup"><span data-stu-id="8b83e-116">register\_db</span></span> |
| <span data-ttu-id="8b83e-117">\_DW</span><span class="sxs-lookup"><span data-stu-id="8b83e-117">\_dw</span></span>                      | <span data-ttu-id="8b83e-118">Dividieren von x, y-Komponenten durch w</span><span class="sxs-lookup"><span data-stu-id="8b83e-118">Divide x,y components by w</span></span> | <span data-ttu-id="8b83e-119">\_DW registrieren</span><span class="sxs-lookup"><span data-stu-id="8b83e-119">register\_dw</span></span> |
| <span data-ttu-id="8b83e-120">\_da</span><span class="sxs-lookup"><span data-stu-id="8b83e-120">\_da</span></span>                      | <span data-ttu-id="8b83e-121">Dividieren von x, y-Komponenten durch w</span><span class="sxs-lookup"><span data-stu-id="8b83e-121">Divide x,y components by w</span></span> | <span data-ttu-id="8b83e-122">Registrieren von \_ da</span><span class="sxs-lookup"><span data-stu-id="8b83e-122">register\_da</span></span> |



 

### <a name="remarks"></a><span data-ttu-id="8b83e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b83e-123">Remarks</span></span>

<span data-ttu-id="8b83e-124">Der-Modifizierer für die-oder-Datenbank \_ \_ führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="8b83e-124">The \_dz or \_db modifier does the following:</span></span>


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



<span data-ttu-id="8b83e-125">Der \_ DW-oder \_ da-Modifizierer führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="8b83e-125">The \_dw or \_da modifier does the following:</span></span>


```
x' = x/w ( x' = 1.0 if w == 0)
y' = y/w ( y' = 1.0 if w == 0)
z' is undefined
w' is undefined
```



## <a name="related-topics"></a><span data-ttu-id="8b83e-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8b83e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b83e-127">Pixel-Shader-quellregistrierungs Modifizierern</span><span class="sxs-lookup"><span data-stu-id="8b83e-127">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




