---
title: dcl_usage Eingabe (sm1, sm2, sm3 – vs asm)
description: Deklarieren Sie die Zuordnung zwischen einer Vertexelementverwendung und einem Verwendungsindex für ein Vertex-Shader-Eingaberegister.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 44bd976d05c0734ca2e498b5de405564f689e20d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998387"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="d33e8-103">dcl \_ usage input (sm1, sm2, sm3 - vs asm) (dcl usage input (sm1, sm2, sm3 – vs asm))</span><span class="sxs-lookup"><span data-stu-id="d33e8-103">dcl\_usage input (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="d33e8-104">Deklarieren Sie die Zuordnung zwischen einer Vertexelementverwendung und einem Verwendungsindex für ein Vertex-Shader-Eingaberegister.</span><span class="sxs-lookup"><span data-stu-id="d33e8-104">Declare the association between a vertex element usage and a usage index for a vertex shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="d33e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d33e8-105">Syntax</span></span>



|                                |
|--------------------------------|
| <span data-ttu-id="d33e8-106">dcl \_ usage usage index \[ \_ \] v\#</span><span class="sxs-lookup"><span data-stu-id="d33e8-106">dcl\_usage\[usage\_index\] v\#</span></span> |



 

<span data-ttu-id="d33e8-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="d33e8-107">Where:</span></span>

-   <span data-ttu-id="d33e8-108">dcl \_ usage gibt an, wie die Registerdaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d33e8-108">dcl\_usage identifies how the register data will be used.</span></span> <span data-ttu-id="d33e8-109">Dies ist der gleiche Wert wie die Member von [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) ohne das Präfix D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="d33e8-109">This is the same value as the members of [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) without the D3DDECLUSAGE prefix.</span></span>
-   <span data-ttu-id="d33e8-110">Usage \_ Index ist ein optionaler ganzzahliger Index zwischen 0 und 15.</span><span class="sxs-lookup"><span data-stu-id="d33e8-110">usage\_index is an optional integer index between 0 and 15.</span></span> <span data-ttu-id="d33e8-111">Die Nutzungsdaten werden geändert.</span><span class="sxs-lookup"><span data-stu-id="d33e8-111">It modifies the usage data.</span></span> <span data-ttu-id="d33e8-112">Der Index entspricht dem Verwendungsindex in einer Scheitelpunktdeklaration.</span><span class="sxs-lookup"><span data-stu-id="d33e8-112">The index matches the usage index in a vertex declaration.</span></span> <span data-ttu-id="d33e8-113">Weitere Informationen finden Sie unter [Vertexdeklaration (Direct3D 9).](/windows/desktop/direct3d9/vertex-declaration)</span><span class="sxs-lookup"><span data-stu-id="d33e8-113">See [Vertex Declaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span></span> <span data-ttu-id="d33e8-114">Der Index wird ohne Leerzeichen an den Verwendungswert (dcl \_ usage) angefügt.</span><span class="sxs-lookup"><span data-stu-id="d33e8-114">The index is appended to the usage value (dcl\_usage ) with no space.</span></span> <span data-ttu-id="d33e8-115">Wenn sie nicht angegeben wird, wird angenommen, dass sie 0 ist.</span><span class="sxs-lookup"><span data-stu-id="d33e8-115">If it is not supplied, it is assumed to be 0.</span></span>
-   <span data-ttu-id="d33e8-116">v \# ist ein [Eingaberegister.](dx9-graphics-reference-asm-vs-registers-input.md)</span><span class="sxs-lookup"><span data-stu-id="d33e8-116">v\# is a [Input Register](dx9-graphics-reference-asm-vs-registers-input.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d33e8-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d33e8-117">Remarks</span></span>



| <span data-ttu-id="d33e8-118">Vertex-Shaderversionen</span><span class="sxs-lookup"><span data-stu-id="d33e8-118">Vertex shader versions</span></span> | <span data-ttu-id="d33e8-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="d33e8-119">1\_1</span></span> | <span data-ttu-id="d33e8-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d33e8-120">2\_0</span></span> | <span data-ttu-id="d33e8-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d33e8-121">2\_x</span></span> | <span data-ttu-id="d33e8-122">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d33e8-122">2\_sw</span></span> | <span data-ttu-id="d33e8-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d33e8-123">3\_0</span></span> | <span data-ttu-id="d33e8-124">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d33e8-124">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d33e8-125">dcl \_ usage</span><span class="sxs-lookup"><span data-stu-id="d33e8-125">dcl\_usage</span></span>             | <span data-ttu-id="d33e8-126">x</span><span class="sxs-lookup"><span data-stu-id="d33e8-126">x</span></span>    | <span data-ttu-id="d33e8-127">x</span><span class="sxs-lookup"><span data-stu-id="d33e8-127">x</span></span>    | <span data-ttu-id="d33e8-128">x</span><span class="sxs-lookup"><span data-stu-id="d33e8-128">x</span></span>    | <span data-ttu-id="d33e8-129">x</span><span class="sxs-lookup"><span data-stu-id="d33e8-129">x</span></span>     | <span data-ttu-id="d33e8-130">x</span><span class="sxs-lookup"><span data-stu-id="d33e8-130">x</span></span>    | <span data-ttu-id="d33e8-131">x</span><span class="sxs-lookup"><span data-stu-id="d33e8-131">x</span></span>     |



 

<span data-ttu-id="d33e8-132">Alle \_ dcl-Verwendungsanweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d33e8-132">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d33e8-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d33e8-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d33e8-134">Vertex-Shader-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="d33e8-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
