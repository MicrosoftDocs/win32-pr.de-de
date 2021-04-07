---
title: D1109 Draw-Fehler
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Fehler bei einem zeichnen-Befehl durch ein Renderziel.
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
ms.openlocfilehash: 4b08dfb99d49dcb447443685e1fbfa01a2cbad1c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730080"
---
# <a name="d1109-draw-failure"></a><span data-ttu-id="abdbc-104">D1109: Zeichnen-Fehler</span><span class="sxs-lookup"><span data-stu-id="abdbc-104">D1109: Draw Failure</span></span>

<span data-ttu-id="abdbc-105">Ein zeichnen-Befehl durch die Ressource eines Renderziels ist fehlgeschlagen \[  \] .</span><span class="sxs-lookup"><span data-stu-id="abdbc-105">A Draw call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="abdbc-106">Tags \[ *Tag1*, *Tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="abdbc-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="abdbc-107">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="abdbc-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="abdbc-108"><span id="resource"></span><span id="RESOURCE"></span>*Ressource*</span><span class="sxs-lookup"><span data-stu-id="abdbc-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="abdbc-109">Die Adresse des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="abdbc-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="abdbc-110"><span id="tag1"></span><span id="TAG1"></span>*Tag1*</span><span class="sxs-lookup"><span data-stu-id="abdbc-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="abdbc-111">Der erste Tagwert (Weitere Informationen finden Sie unter [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).</span><span class="sxs-lookup"><span data-stu-id="abdbc-111">The first tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> <dt>

<span data-ttu-id="abdbc-112"><span id="tag2"></span><span id="TAG2"></span>*Tag2*</span><span class="sxs-lookup"><span data-stu-id="abdbc-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="abdbc-113">Der zweite Tagwert (Weitere Informationen finden Sie unter [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).</span><span class="sxs-lookup"><span data-stu-id="abdbc-113">The second tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="abdbc-114">Fehlerstufe</span><span class="sxs-lookup"><span data-stu-id="abdbc-114">Error Level</span></span> | <span data-ttu-id="abdbc-115">Warnung</span><span class="sxs-lookup"><span data-stu-id="abdbc-115">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="abdbc-116">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="abdbc-116">Possible Causes</span></span>

<span data-ttu-id="abdbc-117">Es gibt viele Gründe, warum ein zeichnen-Befehl fehlschlagen kann.</span><span class="sxs-lookup"><span data-stu-id="abdbc-117">There are many reasons that a Draw call might fail.</span></span> <span data-ttu-id="abdbc-118">Weitere Informationen finden Sie in der Direct2D SDK-Dokumentation für die fehlgeschlagene Methode.</span><span class="sxs-lookup"><span data-stu-id="abdbc-118">For more information, see the Direct2D SDK documentation for the method that failed.</span></span>

 

 