---
title: D1109 Draw Failure
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Fehler bei einem Draw-Aufruf durch ein Renderziel
keywords:
- D1109 Draw Failure Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 09d84f549b2361d2753ac40650ce057de9e4f84c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549965"
---
# <a name="d1109-draw-failure"></a><span data-ttu-id="390e4-104">D1109: Draw Failure</span><span class="sxs-lookup"><span data-stu-id="390e4-104">D1109: Draw Failure</span></span>

<span data-ttu-id="390e4-105">Ein Draw-Aufruf durch eine fehlerhafte \[ *Renderzielressource.* \]</span><span class="sxs-lookup"><span data-stu-id="390e4-105">A Draw call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="390e4-106">Tags \[ *tag1*, *tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="390e4-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="390e4-107">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="390e4-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="390e4-108"><span id="resource"></span><span id="RESOURCE"></span>*Ressource*</span><span class="sxs-lookup"><span data-stu-id="390e4-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="390e4-109">Die Adresse des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="390e4-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="390e4-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span><span class="sxs-lookup"><span data-stu-id="390e4-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="390e4-111">Der erste Tagwert (weitere Informationen finden Sie unter [**SetTags).**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)</span><span class="sxs-lookup"><span data-stu-id="390e4-111">The first tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> <dt>

<span data-ttu-id="390e4-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span><span class="sxs-lookup"><span data-stu-id="390e4-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="390e4-113">Der zweite Tagwert (weitere Informationen finden Sie unter [**SetTags).**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)</span><span class="sxs-lookup"><span data-stu-id="390e4-113">The second tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="390e4-114">Fehlerstufe</span><span class="sxs-lookup"><span data-stu-id="390e4-114">Error Level</span></span> | <span data-ttu-id="390e4-115">Warnung</span><span class="sxs-lookup"><span data-stu-id="390e4-115">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="390e4-116">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="390e4-116">Possible Causes</span></span>

<span data-ttu-id="390e4-117">Es gibt viele Gründe, warum ein Draw-Aufruf fehlschlagen kann.</span><span class="sxs-lookup"><span data-stu-id="390e4-117">There are many reasons that a Draw call might fail.</span></span> <span data-ttu-id="390e4-118">Weitere Informationen finden Sie in der Direct2D SDK-Dokumentation für die Methode, bei der ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="390e4-118">For more information, see the Direct2D SDK documentation for the method that failed.</span></span>

 

 