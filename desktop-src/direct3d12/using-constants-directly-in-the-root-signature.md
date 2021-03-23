---
title: Direkte Verwendung von Konstanten in der Stamm Signatur
description: Anwendungen können Stamm Konstanten in der Stamm Signatur definieren, jeweils als Satz von 32-Bit-Werten. Sie werden in High Level Shading Language (HLSL) als konstanter Puffer angezeigt. Beachten Sie, dass Konstante Puffer aus historischen Gründen als Sätze von 4x32-Bit-Werten angezeigt werden.
ms.assetid: F9A2640F-D1FA-481C-BDF1-B15372E3C512
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3cd3980bede72d6e2f4b163abe11b249970eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104058"
---
# <a name="using-constants-directly-in-the-root-signature"></a><span data-ttu-id="9482e-105">Direkte Verwendung von Konstanten in der Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="9482e-105">Using Constants Directly in the Root Signature</span></span>

<span data-ttu-id="9482e-106">Anwendungen können Stamm Konstanten in der Stamm Signatur definieren, jeweils als Satz von 32-Bit-Werten.</span><span class="sxs-lookup"><span data-stu-id="9482e-106">Applications can define root constants in the root signature, each as a set of 32-bit values.</span></span> <span data-ttu-id="9482e-107">Sie werden in High Level Shading Language (HLSL) als konstanter Puffer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9482e-107">They appear in High Level Shading Language (HLSL) as a constant buffer.</span></span> <span data-ttu-id="9482e-108">Beachten Sie, dass Konstante Puffer aus historischen Gründen als Sätze von 4x32-Bit-Werten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9482e-108">Note that constant buffers for historical reasons are viewed as sets of 4x32-bit values.</span></span>

<span data-ttu-id="9482e-109">Jeder Satz von Benutzer Konstanten wird als skalares Array von 32-Bit-Werten behandelt, das dynamisch indizierbar und schreibgeschützt vom Shader ist.</span><span class="sxs-lookup"><span data-stu-id="9482e-109">Each set of user constants is treated as a scalar array of 32 -bit values, dynamically indexable and read-only from the shader.</span></span> <span data-ttu-id="9482e-110">Out-of-Bounds-Indizierung eine bestimmte Gruppe von Stamm Konstanten erzeugt nicht definierte Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="9482e-110">Out of bounds indexing a given set of root constants produces undefined results.</span></span> <span data-ttu-id="9482e-111">In HLSL können Datenstruktur Definitionen bereitgestellt werden, damit die Benutzer Konstanten Typen erhalten.</span><span class="sxs-lookup"><span data-stu-id="9482e-111">In HLSL, data structure definitions can be provided for the user constants to give them types.</span></span> <span data-ttu-id="9482e-112">Wenn die Stamm Signatur beispielsweise einen Satz von vier Stamm Konstanten definiert, kann HLSL die folgende Struktur überlagern.</span><span class="sxs-lookup"><span data-stu-id="9482e-112">For example, if the root signature defines a set of 4 root constants, HLSL can overlay the following structure on them.</span></span>

``` syntax
struct DrawConstants
{
    uint foo;
    float2 bar;
    int moo;
};
ConstantBuffer<DrawConstants> myDrawConstants : register(b1, space0);
```

<span data-ttu-id="9482e-113">Arrays sind in konstanten Puffern, die auf Stamm Konstanten zugeordnet werden, nicht zulässig, da die dynamische Indizierung im Stamm Signatur Bereich nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="9482e-113">Arrays are not permitted in constant buffers that get mapped onto root constants since dynamic indexing in the root signature space is not supported.</span></span> <span data-ttu-id="9482e-114">Beispielsweise ist es ungültig, einen Eintrag im Konstanten Puffer wie zu haben `float myArray[2];` .</span><span class="sxs-lookup"><span data-stu-id="9482e-114">For example, it is invalid to have an entry in the constant buffer like `float myArray[2];`.</span></span> <span data-ttu-id="9482e-115">Ein konstanter Puffer, der Stamm Konstanten zugeordnet ist, kann kein Array sein. Daher ist es ungültig, Stamm `cbuffer myCBArray[2]` Konstanten zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="9482e-115">A constant buffer that is mapped to root constants cannot itself be an array; therefore, it is invalid to map `cbuffer myCBArray[2]` into root constants.</span></span>

<span data-ttu-id="9482e-116">Konstanten können teilweise festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9482e-116">Constants can be partially set.</span></span> <span data-ttu-id="9482e-117">Wenn die Stamm Signatur z. b. 4 32-Bit-Werte in *roottablebindslot* 2 definiert, kann jede Teilmenge der vier Konstanten gleichzeitig festgelegt werden (die anderen verbleiben unverändert).</span><span class="sxs-lookup"><span data-stu-id="9482e-117">For example, if the root signature defines four 32-bit values at *RootTableBindSlot* 2, then any subset of the four constants can be set at a time (the others remain unchanged).</span></span> <span data-ttu-id="9482e-118">Dies kann in Paketen nützlich sein, die den Stamm Signatur Zustand erben und teilweise ändern können.</span><span class="sxs-lookup"><span data-stu-id="9482e-118">This can be useful in bundles that inherit root signature state and can partially change it.</span></span>

<span data-ttu-id="9482e-119">Beim Festlegen von Konstanten muss das Konstante Puffer Layout, das vom Shader erwartet wird, vorsichtig sein.</span><span class="sxs-lookup"><span data-stu-id="9482e-119">When setting constants be careful of the constant buffer layout expected by the shader.</span></span> <span data-ttu-id="9482e-120">Es ist möglich, dass Konstanten `vec4` z. b. an Grenzen aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="9482e-120">It is possible that constants are padded to `vec4` boundaries, for example.</span></span> <span data-ttu-id="9482e-121">Überprüfen Sie die Reflektionsinformationen aus dem HLSL-Shader, um das erwartete Layout zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9482e-121">To verify the layout expected, check the reflection information from the HLSL shader.</span></span>

<span data-ttu-id="9482e-122">Die folgenden APIs (von der [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) -Schnittstelle) dienen dem direkten Festlegen von Konstanten auf der Stamm Signatur:</span><span class="sxs-lookup"><span data-stu-id="9482e-122">The following APIs (from the [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface) are for setting constants directly on the root signature:</span></span>

-   [<span data-ttu-id="9482e-123">**SetGraphicsRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="9482e-123">**SetGraphicsRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)
-   [<span data-ttu-id="9482e-124">**SetGraphicsRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="9482e-124">**SetGraphicsRoot32BitConstants**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants)
-   [<span data-ttu-id="9482e-125">**SetComputeRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="9482e-125">**SetComputeRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [<span data-ttu-id="9482e-126">**SetComputeRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="9482e-126">**SetComputeRoot32BitConstants**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)

<span data-ttu-id="9482e-127">Weitere Informationen finden Sie auch in der Struktur der D3D12-Stamm [**\_ \_ Konstanten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .</span><span class="sxs-lookup"><span data-stu-id="9482e-127">Also, refer to the [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9482e-128">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9482e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9482e-129">Stamm Signaturen</span><span class="sxs-lookup"><span data-stu-id="9482e-129">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




