---
title: Datentypen (HLSL)
description: HLSL unterstützt viele verschiedene systeminterne Datentypen. Diese Tabelle zeigt, welche Typen zum Definieren von shadervariablen verwendet werden müssen.
ms.assetid: e4b7738d-e865-4151-a204-0a5b88a913b3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cee02e38180b903b235c32ebc2c7ca486777b20
ms.sourcegitcommit: 316ce582d9b972634a0521e0380e054e9cbb5bae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "104995230"
---
# <a name="data-types-hlsl"></a><span data-ttu-id="0d3b4-104">Datentypen (HLSL)</span><span class="sxs-lookup"><span data-stu-id="0d3b4-104">Data Types (HLSL)</span></span>

<span data-ttu-id="0d3b4-105">HLSL unterstützt viele verschiedene systeminterne Datentypen.</span><span class="sxs-lookup"><span data-stu-id="0d3b4-105">HLSL supports many different intrinsic data types.</span></span> <span data-ttu-id="0d3b4-106">Diese Tabelle zeigt, welche Typen zum Definieren von shadervariablen verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0d3b4-106">This table shows which types to use to define shader variables.</span></span>



|                                                                                                                         |                                            |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="0d3b4-107">Diesen systeminternen Typ verwenden</span><span class="sxs-lookup"><span data-stu-id="0d3b4-107">Use This Intrinsic Type</span></span>                                                                                                 | <span data-ttu-id="0d3b4-108">So definieren Sie diese Shader-Variable</span><span class="sxs-lookup"><span data-stu-id="0d3b4-108">To Define This Shader Variable</span></span>             |
| [<span data-ttu-id="0d3b4-109">Skalare</span><span class="sxs-lookup"><span data-stu-id="0d3b4-109">Scalar</span></span>](dx-graphics-hlsl-scalar.md)                                                                                   | <span data-ttu-id="0d3b4-110">Skalar mit einer Komponente</span><span class="sxs-lookup"><span data-stu-id="0d3b4-110">One-component scalar</span></span>                       |
| <span data-ttu-id="0d3b4-111">[Vektor](dx-graphics-hlsl-vector.md), [Matrix](dx-graphics-hlsl-matrix.md)</span><span class="sxs-lookup"><span data-stu-id="0d3b4-111">[Vector](dx-graphics-hlsl-vector.md), [Matrix](dx-graphics-hlsl-matrix.md)</span></span>                                            | <span data-ttu-id="0d3b4-112">Vektor oder Matrix mit mehreren Komponenten</span><span class="sxs-lookup"><span data-stu-id="0d3b4-112">Multiple-component vector or matrix</span></span>        |
| <span data-ttu-id="0d3b4-113">[Sampler](dx-graphics-hlsl-sampler.md), [Textur](dx-graphics-hlsl-texture.md) oder [Puffer](dx-graphics-hlsl-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="0d3b4-113">[Sampler](dx-graphics-hlsl-sampler.md), [Texture](dx-graphics-hlsl-texture.md) or [Buffer](dx-graphics-hlsl-buffer.md)</span></span>   | <span data-ttu-id="0d3b4-114">Sampler, Textur oder Puffer Objekt</span><span class="sxs-lookup"><span data-stu-id="0d3b4-114">Sampler, texture, or buffer object</span></span>         |
| <span data-ttu-id="0d3b4-115">[Struktur](dx-graphics-hlsl-struct.md), [Benutzer definiert](dx-graphics-hlsl-user-defined.md)</span><span class="sxs-lookup"><span data-stu-id="0d3b4-115">[Struct](dx-graphics-hlsl-struct.md), [User Defined](dx-graphics-hlsl-user-defined.md)</span></span>                                | <span data-ttu-id="0d3b4-116">Benutzerdefinierte Struktur oder TypeDef</span><span class="sxs-lookup"><span data-stu-id="0d3b4-116">Custom structure or typedef</span></span>                |
| <span data-ttu-id="0d3b4-117">Array</span><span class="sxs-lookup"><span data-stu-id="0d3b4-117">Array</span></span>                                                                                   | <span data-ttu-id="0d3b4-118">Literale skalare Ausdrücke, die mit den meisten anderen Typen deklariert sind</span><span class="sxs-lookup"><span data-stu-id="0d3b4-118">Literal scalar expressions declared containing most other types</span></span>                       |
| [<span data-ttu-id="0d3b4-119">State-Objekt</span><span class="sxs-lookup"><span data-stu-id="0d3b4-119">State Object</span></span>](dx-graphics-hlsl-state-object.md) | <span data-ttu-id="0d3b4-120">HLSL-Darstellungen von Zustands Objekten</span><span class="sxs-lookup"><span data-stu-id="0d3b4-120">HLSL representations of state objects</span></span> |


 

<span data-ttu-id="0d3b4-121">Damit Sie besser verstehen können, wie Vektoren und Matrizen in HLSL verwendet werden, sollten Sie diese Hintergrundinformationen darüber lesen, wie HLSL [pro-Komponenten-](dx-graphics-hlsl-per-component-math.md) Math verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d3b4-121">To help you better understand how to use vectors and matrices in HLSL, you may want to read this background information on how HLSL uses [per-component](dx-graphics-hlsl-per-component-math.md) math.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d3b4-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d3b4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d3b4-123">Variablen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0d3b4-123">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 




