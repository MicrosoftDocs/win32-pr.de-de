---
title: Eingabe Register
description: Eingabe Register
ms.assetid: 7cd8e555-4e69-4905-a541-62e09b41a602
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 983f0520ccc50fa1683d4b8254ac436fff7491a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947860"
---
# <a name="input-register"></a><span data-ttu-id="9fdf3-103">Eingabe Register</span><span class="sxs-lookup"><span data-stu-id="9fdf3-103">Input Register</span></span>

<span data-ttu-id="9fdf3-104">Vertex-Shader-Eingabe Register.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-104">Vertex shader input register.</span></span>

<span data-ttu-id="9fdf3-105">Daten aus jedem Scheitelpunkt (mit einem oder mehreren eingegebenen Scheitelpunkt strömen) werden vor dem Ausführen des Vertexshaders in die Scheitelpunkt Eingabe Register geladen.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-105">Data from each vertex (using one or more input vertex streams) is loaded into the vertex input registers before the vertex shader is run.</span></span> <span data-ttu-id="9fdf3-106">Die Eingabe Register bestehen aus 16 4-Komponenten-Gleit Komma Vektoren, die als v0 bis V15 bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-106">The input registers consist of 16 four-component floating-point vectors, designated as v0 through v15.</span></span> <span data-ttu-id="9fdf3-107">Diese Register sind schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-107">These registers are read-only.</span></span> <span data-ttu-id="9fdf3-108">Ein Eingabe Register ist über eine Scheitelpunkt Deklaration an Scheitelpunkt Daten gebunden.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-108">An input register is bound to vertex data through a vertex declaration.</span></span>

<span data-ttu-id="9fdf3-109">Die folgenden Register Eigenschaften steuern, wie sich die einzelnen Register Verhalten:</span><span class="sxs-lookup"><span data-stu-id="9fdf3-109">The following register properties control how each register behaves:</span></span>



| <span data-ttu-id="9fdf3-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9fdf3-110">Property</span></span>        | <span data-ttu-id="9fdf3-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9fdf3-111">Description</span></span>                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fdf3-112">Name</span><span class="sxs-lookup"><span data-stu-id="9fdf3-112">Name</span></span>            | <span data-ttu-id="9fdf3-113">v \[ n \] -n ist eine optionale Registernummer.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-113">v\[n\] - n is an optional register number.</span></span> <span data-ttu-id="9fdf3-114">0 ist der Standardwert, der verwendet wird, wenn er weggelassen wird.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-114">0 is the default value used, if it is omitted.</span></span>     |
| <span data-ttu-id="9fdf3-115">Anzahl</span><span class="sxs-lookup"><span data-stu-id="9fdf3-115">Count</span></span>           | <span data-ttu-id="9fdf3-116">Maximal 16 Register, v0-V15.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-116">A maximum of 16 registers, v0 - v15.</span></span>                                                          |
| <span data-ttu-id="9fdf3-117">E/a-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="9fdf3-117">I/O permissions</span></span> | <span data-ttu-id="9fdf3-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-118">Read-only.</span></span> <span data-ttu-id="9fdf3-119">Dieses Register kann nicht von der API oder im Shader geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-119">This register cannot be written by the API or within the shader.</span></span>                   |
| <span data-ttu-id="9fdf3-120">Leseports</span><span class="sxs-lookup"><span data-stu-id="9fdf3-120">Read ports</span></span>      | <span data-ttu-id="9fdf3-121">1. gibt an, wie oft ein Register innerhalb einer einzigen Anweisung gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-121">1. This is the number of times a register can be read within a single instruction.</span></span> <span data-ttu-id="9fdf3-122">Siehe unten.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-122">See below.</span></span> |



 

<span data-ttu-id="9fdf3-123">Jede einzelne Anweisung kann nur auf ein Scheitelpunkt Eingabe Register zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-123">Any single instruction can access only one vertex input register.</span></span> <span data-ttu-id="9fdf3-124">Allerdings kann jede Quelle in der Anweisung den Vektor beim Lesen unabhängig voneinander verwischen und negieren.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-124">However, each source in the instruction can independently swizzle and negate that vector as it is read.</span></span>

## <a name="example"></a><span data-ttu-id="9fdf3-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9fdf3-125">Example</span></span>

<span data-ttu-id="9fdf3-126">Es folgt ein Beispiel für die Verwendung einer Scheitelpunkt Deklaration zum Binden von 2D-Scheitelpunkt Positionsdaten an die Registrierung von v0</span><span class="sxs-lookup"><span data-stu-id="9fdf3-126">Here is an example using a vertex declaration to bind 2D vertex position data to register v0.</span></span>

<span data-ttu-id="9fdf3-127">Die Vertex-Deklaration gehört zu der Anwendung:</span><span class="sxs-lookup"><span data-stu-id="9fdf3-127">The vertex declaration belongs in the application:</span></span>


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



<span data-ttu-id="9fdf3-128">Im folgenden finden Sie die entsprechende Vertex-Shader-Deklaration:</span><span class="sxs-lookup"><span data-stu-id="9fdf3-128">Here is the corresponding vertex shader declaration:</span></span>


```
dcl_position v0
```





| <span data-ttu-id="9fdf3-129">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="9fdf3-129">Vertex shader versions</span></span> | <span data-ttu-id="9fdf3-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="9fdf3-130">1\_1</span></span> | <span data-ttu-id="9fdf3-131">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9fdf3-131">2\_0</span></span> | <span data-ttu-id="9fdf3-132">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9fdf3-132">2\_sw</span></span> | <span data-ttu-id="9fdf3-133">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9fdf3-133">2\_x</span></span> | <span data-ttu-id="9fdf3-134">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9fdf3-134">3\_0</span></span> | <span data-ttu-id="9fdf3-135">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9fdf3-135">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="9fdf3-136">Positions Register</span><span class="sxs-lookup"><span data-stu-id="9fdf3-136">Position Register</span></span>      | <span data-ttu-id="9fdf3-137">x</span><span class="sxs-lookup"><span data-stu-id="9fdf3-137">x</span></span>    | <span data-ttu-id="9fdf3-138">x</span><span class="sxs-lookup"><span data-stu-id="9fdf3-138">x</span></span>    | <span data-ttu-id="9fdf3-139">x</span><span class="sxs-lookup"><span data-stu-id="9fdf3-139">x</span></span>     | <span data-ttu-id="9fdf3-140">x</span><span class="sxs-lookup"><span data-stu-id="9fdf3-140">x</span></span>    | <span data-ttu-id="9fdf3-141">x</span><span class="sxs-lookup"><span data-stu-id="9fdf3-141">x</span></span>    | <span data-ttu-id="9fdf3-142">x</span><span class="sxs-lookup"><span data-stu-id="9fdf3-142">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="9fdf3-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9fdf3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fdf3-144">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="9fdf3-144">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




