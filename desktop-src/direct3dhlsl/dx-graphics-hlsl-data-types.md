---
title: Datentypen (HLSL)
description: HLSL unterstützt viele verschiedene systeminterne Datentypen. Diese Tabelle zeigt, welche Typen zum Definieren von Shadervariablen verwendet werden.
ms.assetid: e4b7738d-e865-4151-a204-0a5b88a913b3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c4cb8f6fd15db857daa3005c99381d437a5289f6
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129647"
---
# <a name="data-types-hlsl"></a><span data-ttu-id="5d6d3-104">Datentypen (HLSL)</span><span class="sxs-lookup"><span data-stu-id="5d6d3-104">Data Types (HLSL)</span></span>

<span data-ttu-id="5d6d3-105">HLSL unterstützt viele verschiedene systeminterne Datentypen.</span><span class="sxs-lookup"><span data-stu-id="5d6d3-105">HLSL supports many different intrinsic data types.</span></span> <span data-ttu-id="5d6d3-106">Diese Tabelle zeigt, welche Typen zum Definieren von Shadervariablen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d6d3-106">This table shows which types to use to define shader variables.</span></span>



| <span data-ttu-id="5d6d3-107">Verwenden dieses systeminternen Typs</span><span class="sxs-lookup"><span data-stu-id="5d6d3-107">Use this intrinsic type</span></span>                                                                                                                         | <span data-ttu-id="5d6d3-108">So definieren Sie diese Shadervariable</span><span class="sxs-lookup"><span data-stu-id="5d6d3-108">To define this shader variable</span></span>                                            |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [<span data-ttu-id="5d6d3-109">Skalar</span><span class="sxs-lookup"><span data-stu-id="5d6d3-109">Scalar</span></span>](dx-graphics-hlsl-scalar.md)                                                                                   | <span data-ttu-id="5d6d3-110">Skalar mit einer Komponente</span><span class="sxs-lookup"><span data-stu-id="5d6d3-110">One-component scalar</span></span>                       |
| <span data-ttu-id="5d6d3-111">[Vektor,](dx-graphics-hlsl-vector.md) [Matrix](dx-graphics-hlsl-matrix.md)</span><span class="sxs-lookup"><span data-stu-id="5d6d3-111">[Vector](dx-graphics-hlsl-vector.md), [Matrix](dx-graphics-hlsl-matrix.md)</span></span>                                            | <span data-ttu-id="5d6d3-112">Vektor oder Matrix mit mehreren Komponenten</span><span class="sxs-lookup"><span data-stu-id="5d6d3-112">Multiple-component vector or matrix</span></span>        |
| <span data-ttu-id="5d6d3-113">[Sampler,](dx-graphics-hlsl-sampler.md) [Textur](dx-graphics-hlsl-texture.md) oder [Puffer](dx-graphics-hlsl-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="5d6d3-113">[Sampler](dx-graphics-hlsl-sampler.md), [Texture](dx-graphics-hlsl-texture.md) or [Buffer](dx-graphics-hlsl-buffer.md)</span></span>   | <span data-ttu-id="5d6d3-114">Sampler, Textur oder Pufferobjekt</span><span class="sxs-lookup"><span data-stu-id="5d6d3-114">Sampler, texture, or buffer object</span></span>         |
| <span data-ttu-id="5d6d3-115">[Struktur,](dx-graphics-hlsl-struct.md) [benutzerdefiniert](dx-graphics-hlsl-user-defined.md)</span><span class="sxs-lookup"><span data-stu-id="5d6d3-115">[Struct](dx-graphics-hlsl-struct.md), [User Defined](dx-graphics-hlsl-user-defined.md)</span></span>                                | <span data-ttu-id="5d6d3-116">Benutzerdefinierte Struktur oder Typdefinition</span><span class="sxs-lookup"><span data-stu-id="5d6d3-116">Custom structure or typedef</span></span>                |
| <span data-ttu-id="5d6d3-117">Array</span><span class="sxs-lookup"><span data-stu-id="5d6d3-117">Array</span></span>                                                                                   | <span data-ttu-id="5d6d3-118">Literale skalare Ausdrücke, die mit den meisten anderen Typen deklariert sind</span><span class="sxs-lookup"><span data-stu-id="5d6d3-118">Literal scalar expressions declared containing most other types</span></span>                       |
| [<span data-ttu-id="5d6d3-119">State-Objekt</span><span class="sxs-lookup"><span data-stu-id="5d6d3-119">State Object</span></span>](dx-graphics-hlsl-state-object.md) | <span data-ttu-id="5d6d3-120">HLSL-Darstellungen von Zustandsobjekten</span><span class="sxs-lookup"><span data-stu-id="5d6d3-120">HLSL representations of state objects</span></span> |


 

<span data-ttu-id="5d6d3-121">Damit Sie besser verstehen können, wie Vektoren und Matrizen in HLSL verwendet werden, sollten Sie diese Hintergrundinformationen zur Verwendung der komponentenspezifischen Mathematik durch HLSL [lesen.](dx-graphics-hlsl-per-component-math.md)</span><span class="sxs-lookup"><span data-stu-id="5d6d3-121">To help you better understand how to use vectors and matrices in HLSL, you may want to read this background information on how HLSL uses [per-component](dx-graphics-hlsl-per-component-math.md) math.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d6d3-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5d6d3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d6d3-123">Variablen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5d6d3-123">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 




