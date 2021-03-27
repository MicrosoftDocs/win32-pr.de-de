---
title: D3DCOMPILE_EFFECT Konstanten (D3DCompiler. h)
description: Diese Konstanten leiten direkt, wie der Compiler eine Effekt Datei kompiliert oder wie die Laufzeit die Effekt Datei verarbeitet.
ms.assetid: AA46E5ED-92DD-4327-B852-8DD23A878562
topic_type:
- apiref
api_name:
- D3DCOMPILE_EFFECT_CHILD_EFFECT
- D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69f0597341a331af82ed279a6030126d222b70f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982120"
---
# <a name="d3dcompile_effect-constants"></a><span data-ttu-id="beb71-103">D3DCOMPILE \_ Effect-Konstanten</span><span class="sxs-lookup"><span data-stu-id="beb71-103">D3DCOMPILE\_EFFECT Constants</span></span>

<span data-ttu-id="beb71-104">Diese Konstanten leiten direkt, wie der Compiler eine Effekt Datei kompiliert oder wie die Laufzeit die Effekt Datei verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="beb71-104">These constants direct how the compiler compiles an effect file or how the runtime processes the effect file.</span></span>

<dl> <dt>

<span data-ttu-id="beb71-105"><span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**Untergeordneter Effekt von D3DCOMPILE \_ Effect \_ \_**</span><span class="sxs-lookup"><span data-stu-id="beb71-105"><span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**D3DCOMPILE\_EFFECT\_CHILD\_EFFECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="beb71-106">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="beb71-106">(1 << 0)</span></span>
</dt> <dt>



<span data-ttu-id="beb71-107">Kompilieren Sie die Effekt Datei (. fx) in einen untergeordneten Effekt.</span><span class="sxs-lookup"><span data-stu-id="beb71-107">Compile the effects (.fx) file to a child effect.</span></span> <span data-ttu-id="beb71-108">Untergeordnete Effekte verfügen über keine Initialisierer für freigegebene Werte, da diese untergeordneten Effekte im Haupteffekt (dem Effekt Pool) initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="beb71-108">Child effects have no initializers for any shared values because these child effects are initialized in the master effect (the effect pool).</span></span>

> [!Note]  
> <span data-ttu-id="beb71-109">Effekt Pools werden von Effekten 10 (FX10) unterstützt, aber nicht durch Effekte 11 (FX11).</span><span class="sxs-lookup"><span data-stu-id="beb71-109">Effect pools are supported by Effects 10 (FX10) but not by Effects 11 (FX11).</span></span> <span data-ttu-id="beb71-110">Weitere Informationen zu Unterschieden zwischen den Effekts-Pools in Direct3D 10-und Effect-Gruppen in Direct3D 11 finden Sie unter [Auswirkungen von Pools und Gruppen](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).</span><span class="sxs-lookup"><span data-stu-id="beb71-110">For more info about differences between effect pools in Direct3D 10 and effect groups in Direct3D 11, see [Effect Pools and Groups](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="beb71-111"><span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE \_ Effekt \_ \_ langsame \_ Ops zulassen**</span><span class="sxs-lookup"><span data-stu-id="beb71-111"><span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE\_EFFECT\_ALLOW\_SLOW\_OPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="beb71-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="beb71-112">(1 << 1)</span></span>
</dt> <dt>



<span data-ttu-id="beb71-113">Deaktiviert den Leistungsmodus und ermöglicht änderbare Zustands Objekte.</span><span class="sxs-lookup"><span data-stu-id="beb71-113">Disables performance mode and allows for mutable state objects.</span></span>

<span data-ttu-id="beb71-114">Standardmäßig ist der Leistungsmodus aktiviert.</span><span class="sxs-lookup"><span data-stu-id="beb71-114">By default, performance mode is enabled.</span></span> <span data-ttu-id="beb71-115">Der Leistungsmodus lässt änderbare Zustands Objekte nicht zu, indem verhindert wird, dass nicht literale Ausdrücke in Zustands Objekt Definitionen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="beb71-115">Performance mode disallows mutable state objects by preventing non-literal expressions from appearing in state object definitions.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="beb71-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="beb71-116">Requirements</span></span>



| <span data-ttu-id="beb71-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="beb71-117">Requirement</span></span> | <span data-ttu-id="beb71-118">Wert</span><span class="sxs-lookup"><span data-stu-id="beb71-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="beb71-119">Header</span><span class="sxs-lookup"><span data-stu-id="beb71-119">Header</span></span><br/> | <dl> <span data-ttu-id="beb71-120"><dt>D3DCompiler. h</dt></span><span class="sxs-lookup"><span data-stu-id="beb71-120"><dt>D3DCompiler.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beb71-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="beb71-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb71-122">D3DCompiler-Konstanten</span><span class="sxs-lookup"><span data-stu-id="beb71-122">D3DCompiler Constants</span></span>](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

