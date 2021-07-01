---
title: dcl_usage eingabe (sm1, sm2, sm3 – vs asm)
description: Deklarieren Sie die Zuordnung zwischen der Verwendung eines Scheitelpunktelements und einem Verwendungsindex für ein Vertex-Shader-Eingaberegister.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae4b024bbce0636127b0ed0fc5f42bc466e1b7fd
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129687"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="32f0f-103">dcl \_ usage input (sm1, sm2, sm3 – vs asm)</span><span class="sxs-lookup"><span data-stu-id="32f0f-103">dcl\_usage input (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="32f0f-104">Deklarieren Sie die Zuordnung zwischen der Verwendung eines Scheitelpunktelements und einem Verwendungsindex für ein Vertex-Shader-Eingaberegister.</span><span class="sxs-lookup"><span data-stu-id="32f0f-104">Declare the association between a vertex element usage and a usage index for a vertex shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="32f0f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="32f0f-105">Syntax</span></span>

<span data-ttu-id="32f0f-106">dcl \_ usage usage index \[ \_ \] v\#</span><span class="sxs-lookup"><span data-stu-id="32f0f-106">dcl\_usage\[usage\_index\] v\#</span></span>



 

<span data-ttu-id="32f0f-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="32f0f-107">Where:</span></span>

-   <span data-ttu-id="32f0f-108">dcl \_ usage gibt an, wie die Registerdaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32f0f-108">dcl\_usage identifies how the register data will be used.</span></span> <span data-ttu-id="32f0f-109">Dies ist der gleiche Wert wie die Elemente von [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) ohne das Präfix D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="32f0f-109">This is the same value as the members of [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) without the D3DDECLUSAGE prefix.</span></span>
-   <span data-ttu-id="32f0f-110">der \_ Nutzungsindex ist ein optionaler ganzzahliger Index zwischen 0 und 15.</span><span class="sxs-lookup"><span data-stu-id="32f0f-110">usage\_index is an optional integer index between 0 and 15.</span></span> <span data-ttu-id="32f0f-111">Sie ändert die Nutzungsdaten.</span><span class="sxs-lookup"><span data-stu-id="32f0f-111">It modifies the usage data.</span></span> <span data-ttu-id="32f0f-112">Der Index entspricht dem Verwendungsindex in einer Scheitelpunktdeklaration.</span><span class="sxs-lookup"><span data-stu-id="32f0f-112">The index matches the usage index in a vertex declaration.</span></span> <span data-ttu-id="32f0f-113">Weitere Informationen [finden Sie unter Vertexdeklaration (Direct3D 9).](/windows/desktop/direct3d9/vertex-declaration)</span><span class="sxs-lookup"><span data-stu-id="32f0f-113">See [Vertex Declaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span></span> <span data-ttu-id="32f0f-114">Der Index wird ohne Speicherplatz an den Nutzungswert (dcl \_ usage) angefügt.</span><span class="sxs-lookup"><span data-stu-id="32f0f-114">The index is appended to the usage value (dcl\_usage ) with no space.</span></span> <span data-ttu-id="32f0f-115">Wenn sie nicht angegeben wird, wird davon ausgegangen, dass sie 0 ist.</span><span class="sxs-lookup"><span data-stu-id="32f0f-115">If it is not supplied, it is assumed to be 0.</span></span>
-   <span data-ttu-id="32f0f-116">v \# ist ein [Eingaberegister.](dx9-graphics-reference-asm-vs-registers-input.md)</span><span class="sxs-lookup"><span data-stu-id="32f0f-116">v\# is a [Input Register](dx9-graphics-reference-asm-vs-registers-input.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="32f0f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32f0f-117">Remarks</span></span>



| <span data-ttu-id="32f0f-118">Vertex-Shaderversionen</span><span class="sxs-lookup"><span data-stu-id="32f0f-118">Vertex shader versions</span></span> | <span data-ttu-id="32f0f-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="32f0f-119">1\_1</span></span> | <span data-ttu-id="32f0f-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="32f0f-120">2\_0</span></span> | <span data-ttu-id="32f0f-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="32f0f-121">2\_x</span></span> | <span data-ttu-id="32f0f-122">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="32f0f-122">2\_sw</span></span> | <span data-ttu-id="32f0f-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="32f0f-123">3\_0</span></span> | <span data-ttu-id="32f0f-124">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="32f0f-124">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="32f0f-125">dcl \_ usage</span><span class="sxs-lookup"><span data-stu-id="32f0f-125">dcl\_usage</span></span>             | <span data-ttu-id="32f0f-126">x</span><span class="sxs-lookup"><span data-stu-id="32f0f-126">x</span></span>    | <span data-ttu-id="32f0f-127">x</span><span class="sxs-lookup"><span data-stu-id="32f0f-127">x</span></span>    | <span data-ttu-id="32f0f-128">x</span><span class="sxs-lookup"><span data-stu-id="32f0f-128">x</span></span>    | <span data-ttu-id="32f0f-129">x</span><span class="sxs-lookup"><span data-stu-id="32f0f-129">x</span></span>     | <span data-ttu-id="32f0f-130">x</span><span class="sxs-lookup"><span data-stu-id="32f0f-130">x</span></span>    | <span data-ttu-id="32f0f-131">x</span><span class="sxs-lookup"><span data-stu-id="32f0f-131">x</span></span>     |



 

<span data-ttu-id="32f0f-132">Alle \_ dcl-Verwendungsanweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="32f0f-132">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32f0f-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32f0f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32f0f-134">Vertex-Shader-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="32f0f-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
