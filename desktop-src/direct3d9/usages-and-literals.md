---
description: Die Verwendung ähnelt dem Bereich eines Parameters, da der Bereich definiert wird, in dem der Parameter gültig ist.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Verwendungen und Literale (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ca6f010d2c1e05055fd4427b8b5f7d4ab445ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346006"
---
# <a name="usages-and-literals-direct3d-9"></a><span data-ttu-id="a2158-103">Verwendungen und Literale (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a2158-103">Usages and Literals (Direct3D 9)</span></span>

<span data-ttu-id="a2158-104">Die Verwendung ähnelt dem Bereich eines Parameters, da der Bereich definiert wird, in dem der Parameter gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a2158-104">Usage is similar to a parameter's scope, because it defines the scope in which the parameter is valid.</span></span>



|        |                                                                                                                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2158-105">Wert</span><span class="sxs-lookup"><span data-stu-id="a2158-105">Value</span></span>  | <span data-ttu-id="a2158-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2158-106">Description</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="a2158-107">const</span><span class="sxs-lookup"><span data-stu-id="a2158-107">const</span></span>  | <span data-ttu-id="a2158-108">Der-Parameter ist innerhalb des Bereichs aller Funktionen konstant.</span><span class="sxs-lookup"><span data-stu-id="a2158-108">The parameter will be constant within the scope of all functions.</span></span> <span data-ttu-id="a2158-109">(Beachten Sie, dass solche Parameter immer noch in mit [**ID3DXEffect**](id3dxeffect.md) oder [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)geschrieben werden können, da dies außerhalb des Gültigkeits Bereichs aller Funktionen auftritt.)</span><span class="sxs-lookup"><span data-stu-id="a2158-109">(Note that such parameters can still be written to with either [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), because this occurs outside the scope of all functions.)</span></span> |
| <span data-ttu-id="a2158-110">Freigegeben</span><span class="sxs-lookup"><span data-stu-id="a2158-110">shared</span></span> | <span data-ttu-id="a2158-111">Der Parameter wird im Effekt Pool freigegeben.</span><span class="sxs-lookup"><span data-stu-id="a2158-111">The parameter will be shared in the effect pool.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="a2158-112">static</span><span class="sxs-lookup"><span data-stu-id="a2158-112">static</span></span> | <span data-ttu-id="a2158-113">Der-Parameter ist für die Anwendung unsichtbar, d. h., Sie können nicht über [**ID3DXEffect**](id3dxeffect.md) oder [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)auf Sie zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a2158-113">The parameter will be invisible to the application, that is, you cannot access them from [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>                                                                                                  |



 

<span data-ttu-id="a2158-114">Das Markieren eines Parameters als Literalwert gibt an, dass sein Wert nie geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a2158-114">Marking a parameter as literal indicates that its value will never change.</span></span> <span data-ttu-id="a2158-115">Dadurch kann der Effekt Compiler zusätzliche Optimierungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="a2158-115">This enables the effect compiler to do extra optimization.</span></span>

<span data-ttu-id="a2158-116">Nur nicht freigegebene Parameter der obersten Ebene können als Literale gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="a2158-116">Only non-shared top-level parameters can be marked as literal.</span></span> <span data-ttu-id="a2158-117">Parameter können nur mit [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)als Literale gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="a2158-117">Parameters can only be marked as literal with [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span> <span data-ttu-id="a2158-118">Literalwerte können nicht mit [**ID3DXEffect**](id3dxeffect.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a2158-118">Literal values cannot be set with [**ID3DXEffect**](id3dxeffect.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2158-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a2158-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2158-120">Effekt Format</span><span class="sxs-lookup"><span data-stu-id="a2158-120">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



