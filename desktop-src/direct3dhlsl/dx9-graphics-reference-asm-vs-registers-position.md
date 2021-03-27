---
title: Positions Register
description: Dieses Vertex-Shader-Ausgabe Register enthält Daten pro Scheitelpunkt Position.
ms.assetid: 98f71027-d94b-4dd0-a6b6-4b263954eff9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 89470bb920db7c612b21cefb2c44c2c89d48ce28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711087"
---
# <a name="position-register"></a><span data-ttu-id="d3c79-103">Positions Register</span><span class="sxs-lookup"><span data-stu-id="d3c79-103">Position Register</span></span>

<span data-ttu-id="d3c79-104">Dieses Vertex-Shader-Ausgabe Register enthält Daten pro Scheitelpunkt Position.</span><span class="sxs-lookup"><span data-stu-id="d3c79-104">This vertex shader output register contains per-vertex position data.</span></span>



| <span data-ttu-id="d3c79-105">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="d3c79-105">Vertex shader versions</span></span> | <span data-ttu-id="d3c79-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="d3c79-106">1\_1</span></span> | <span data-ttu-id="d3c79-107">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d3c79-107">2\_0</span></span> | <span data-ttu-id="d3c79-108">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d3c79-108">2\_sw</span></span> | <span data-ttu-id="d3c79-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d3c79-109">2\_x</span></span> | <span data-ttu-id="d3c79-110">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d3c79-110">3\_0</span></span> | <span data-ttu-id="d3c79-111">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d3c79-111">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="d3c79-112">Positions Register</span><span class="sxs-lookup"><span data-stu-id="d3c79-112">Position Register</span></span>      | <span data-ttu-id="d3c79-113">x</span><span class="sxs-lookup"><span data-stu-id="d3c79-113">x</span></span>    | <span data-ttu-id="d3c79-114">x</span><span class="sxs-lookup"><span data-stu-id="d3c79-114">x</span></span>    | <span data-ttu-id="d3c79-115">x</span><span class="sxs-lookup"><span data-stu-id="d3c79-115">x</span></span>     | <span data-ttu-id="d3c79-116">x</span><span class="sxs-lookup"><span data-stu-id="d3c79-116">x</span></span>    | <span data-ttu-id="d3c79-117">x</span><span class="sxs-lookup"><span data-stu-id="d3c79-117">x</span></span>    | <span data-ttu-id="d3c79-118">x</span><span class="sxs-lookup"><span data-stu-id="d3c79-118">x</span></span>     |



 

<span data-ttu-id="d3c79-119">Ein Register besteht aus Eigenschaften, die bestimmen, wie sich die einzelnen Register Verhalten.</span><span class="sxs-lookup"><span data-stu-id="d3c79-119">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="d3c79-120">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d3c79-120">Property</span></span>        | <span data-ttu-id="d3c79-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3c79-121">Description</span></span> |
|-----------------|-------------|
| <span data-ttu-id="d3c79-122">Name</span><span class="sxs-lookup"><span data-stu-id="d3c79-122">Name</span></span>            | <span data-ttu-id="d3c79-123">OPOS</span><span class="sxs-lookup"><span data-stu-id="d3c79-123">oPos</span></span>        |
| <span data-ttu-id="d3c79-124">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d3c79-124">Count</span></span>           | <span data-ttu-id="d3c79-125">1 Vektor</span><span class="sxs-lookup"><span data-stu-id="d3c79-125">1 vector</span></span>    |
| <span data-ttu-id="d3c79-126">E/a-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="d3c79-126">I/O permissions</span></span> | <span data-ttu-id="d3c79-127">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d3c79-127">Write-only.</span></span> |



 

<span data-ttu-id="d3c79-128">Der Wert ist die Position im homogenen Clippingbereich.</span><span class="sxs-lookup"><span data-stu-id="d3c79-128">The value is the position in homogeneous clipping space.</span></span> <span data-ttu-id="d3c79-129">Dieser Wert muss vom Vertex-Shader geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d3c79-129">This value must be written by the vertex shader.</span></span>

<span data-ttu-id="d3c79-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d3c79-130">Example</span></span>


```
    dcl_position v0
    
    def c40, 0.0f,0.0f,0.0f,0.0f;
    // transform into projection space
    m4x4 r0,v0,c8
    max r0.z,c40.z,r0.z //clamp to 0
    max r0.w,c12.x,r0.w //clamp to near clip plane
    mov oPos,r0   
```



## <a name="related-topics"></a><span data-ttu-id="d3c79-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3c79-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3c79-132">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="d3c79-132">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




