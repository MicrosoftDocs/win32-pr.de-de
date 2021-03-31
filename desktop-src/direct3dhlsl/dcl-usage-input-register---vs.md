---
title: dcl_usage Eingabe (SM1, SM2, SM3-vs ASM)
description: Deklarieren Sie die Zuordnung zwischen einer Vertex-Element Verwendung und einem Verwendungs Index für ein Vertex-Shader-Eingabe Register.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38113846fe62c37247bb2d3ca522a34dc9282441
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473533"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="f5bb7-103">DCL- \_ Verwendungs Eingabe (SM1, SM2, SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="f5bb7-103">dcl\_usage input (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="f5bb7-104">Deklarieren Sie die Zuordnung zwischen einer Vertex-Element Verwendung und einem Verwendungs Index für ein Vertex-Shader-Eingabe Register.</span><span class="sxs-lookup"><span data-stu-id="f5bb7-104">Declare the association between a vertex element usage and a usage index for a vertex shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5bb7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5bb7-105">Syntax</span></span>



|                                |
|--------------------------------|
| <span data-ttu-id="f5bb7-106">DCL- \_ Verwendungs \[ Verwendungs \_ Index \] v\#</span><span class="sxs-lookup"><span data-stu-id="f5bb7-106">dcl\_usage\[usage\_index\] v\#</span></span> |



 

<span data-ttu-id="f5bb7-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="f5bb7-107">Where:</span></span>

-   <span data-ttu-id="f5bb7-108">die DCL-Verwendung gibt an, \_ wie die Register Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5bb7-108">dcl\_usage identifies how the register data will be used.</span></span> <span data-ttu-id="f5bb7-109">Dies ist der gleiche Wert wie die Member von [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) ohne das D3DDECLUSAGE-Präfix.</span><span class="sxs-lookup"><span data-stu-id="f5bb7-109">This is the same value as the members of [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) without the D3DDECLUSAGE prefix.</span></span>
-   <span data-ttu-id="f5bb7-110">der Verwendungs \_ Index ist ein optionaler ganzzahliger Index zwischen 0 und 15.</span><span class="sxs-lookup"><span data-stu-id="f5bb7-110">usage\_index is an optional integer index between 0 and 15.</span></span> <span data-ttu-id="f5bb7-111">Sie ändert die Verwendungs Daten.</span><span class="sxs-lookup"><span data-stu-id="f5bb7-111">It modifies the usage data.</span></span> <span data-ttu-id="f5bb7-112">Der Index entspricht dem Verwendungs Index in einer Scheitelpunkt Deklaration.</span><span class="sxs-lookup"><span data-stu-id="f5bb7-112">The index matches the usage index in a vertex declaration.</span></span> <span data-ttu-id="f5bb7-113">Siehe [Vertex-Deklaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span><span class="sxs-lookup"><span data-stu-id="f5bb7-113">See [Vertex Declaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span></span> <span data-ttu-id="f5bb7-114">Der Index wird an den Verwendungs Wert (DCL- \_ Verwendung) ohne Leerzeichen angehängt.</span><span class="sxs-lookup"><span data-stu-id="f5bb7-114">The index is appended to the usage value (dcl\_usage ) with no space.</span></span> <span data-ttu-id="f5bb7-115">Wenn Sie nicht angegeben wird, wird davon ausgegangen, dass Sie 0 ist.</span><span class="sxs-lookup"><span data-stu-id="f5bb7-115">If it is not supplied, it is assumed to be 0.</span></span>
-   <span data-ttu-id="f5bb7-116">v \# ist ein [Eingabe Register](dx9-graphics-reference-asm-vs-registers-input.md).</span><span class="sxs-lookup"><span data-stu-id="f5bb7-116">v\# is a [Input Register](dx9-graphics-reference-asm-vs-registers-input.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5bb7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5bb7-117">Remarks</span></span>



| <span data-ttu-id="f5bb7-118">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="f5bb7-118">Vertex shader versions</span></span> | <span data-ttu-id="f5bb7-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="f5bb7-119">1\_1</span></span> | <span data-ttu-id="f5bb7-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f5bb7-120">2\_0</span></span> | <span data-ttu-id="f5bb7-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f5bb7-121">2\_x</span></span> | <span data-ttu-id="f5bb7-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f5bb7-122">2\_sw</span></span> | <span data-ttu-id="f5bb7-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f5bb7-123">3\_0</span></span> | <span data-ttu-id="f5bb7-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f5bb7-124">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="f5bb7-125">DCL- \_ Verwendung</span><span class="sxs-lookup"><span data-stu-id="f5bb7-125">dcl\_usage</span></span>             | <span data-ttu-id="f5bb7-126">x</span><span class="sxs-lookup"><span data-stu-id="f5bb7-126">x</span></span>    | <span data-ttu-id="f5bb7-127">x</span><span class="sxs-lookup"><span data-stu-id="f5bb7-127">x</span></span>    | <span data-ttu-id="f5bb7-128">x</span><span class="sxs-lookup"><span data-stu-id="f5bb7-128">x</span></span>    | <span data-ttu-id="f5bb7-129">x</span><span class="sxs-lookup"><span data-stu-id="f5bb7-129">x</span></span>     | <span data-ttu-id="f5bb7-130">x</span><span class="sxs-lookup"><span data-stu-id="f5bb7-130">x</span></span>    | <span data-ttu-id="f5bb7-131">x</span><span class="sxs-lookup"><span data-stu-id="f5bb7-131">x</span></span>     |



 

<span data-ttu-id="f5bb7-132">Alle DCL- \_ Verwendungs Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f5bb7-132">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5bb7-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f5bb7-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5bb7-134">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="f5bb7-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 