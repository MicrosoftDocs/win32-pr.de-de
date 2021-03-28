---
title: tex-PS
description: Lädt das Ziel Register mit Farbdaten (RGBA), das aus einer Textur entnommen wurde. Die Textur muss mithilfe von SetTexture an eine bestimmte Textur Phase (n) gebunden werden. Die Textur Stichprobe wird von setsamplerstate gesteuert.
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3070883b167d26cf31f7d7f388f6bd3736a4bde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948896"
---
# <a name="tex---ps"></a><span data-ttu-id="5484b-105">tex-PS</span><span class="sxs-lookup"><span data-stu-id="5484b-105">tex - ps</span></span>

<span data-ttu-id="5484b-106">Lädt das Ziel Register mit Farbdaten (RGBA), das aus einer Textur entnommen wurde.</span><span class="sxs-lookup"><span data-stu-id="5484b-106">Loads the destination register with color data (RGBA) sampled from a texture.</span></span> <span data-ttu-id="5484b-107">Die Textur muss mithilfe von [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)an eine bestimmte Textur Phase (n) gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="5484b-107">The texture must be bound to a particular texture stage (n) using [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="5484b-108">Die Textur Stichprobe wird von [**setsamplerstate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)gesteuert.</span><span class="sxs-lookup"><span data-stu-id="5484b-108">Texture sampling is controlled by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span>

## <a name="syntax"></a><span data-ttu-id="5484b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5484b-109">Syntax</span></span>



| <span data-ttu-id="5484b-110">tex-DST</span><span class="sxs-lookup"><span data-stu-id="5484b-110">tex dst</span></span> |
|---------|



 

<span data-ttu-id="5484b-111">where</span><span class="sxs-lookup"><span data-stu-id="5484b-111">where</span></span>

-   <span data-ttu-id="5484b-112">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="5484b-112">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5484b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5484b-113">Remarks</span></span>



| <span data-ttu-id="5484b-114">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="5484b-114">Pixel shader versions</span></span> | <span data-ttu-id="5484b-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="5484b-115">1\_1</span></span> | <span data-ttu-id="5484b-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="5484b-116">1\_2</span></span> | <span data-ttu-id="5484b-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5484b-117">1\_3</span></span> | <span data-ttu-id="5484b-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="5484b-118">1\_4</span></span> | <span data-ttu-id="5484b-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5484b-119">2\_0</span></span> | <span data-ttu-id="5484b-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5484b-120">2\_x</span></span> | <span data-ttu-id="5484b-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5484b-121">2\_sw</span></span> | <span data-ttu-id="5484b-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5484b-122">3\_0</span></span> | <span data-ttu-id="5484b-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5484b-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5484b-124">tels</span><span class="sxs-lookup"><span data-stu-id="5484b-124">tex</span></span>                   | <span data-ttu-id="5484b-125">x</span><span class="sxs-lookup"><span data-stu-id="5484b-125">x</span></span>    | <span data-ttu-id="5484b-126">x</span><span class="sxs-lookup"><span data-stu-id="5484b-126">x</span></span>    | <span data-ttu-id="5484b-127">x</span><span class="sxs-lookup"><span data-stu-id="5484b-127">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="5484b-128">Die Ziel Registernummer gibt die Textur Phasen Nummer an.</span><span class="sxs-lookup"><span data-stu-id="5484b-128">The destination register number specifies the texture stage number.</span></span>

<span data-ttu-id="5484b-129">Bei der Textur Stichprobe werden Texturkoordinaten verwendet, um einen Farbwert bei den angegebenen (u, v, w, q)-Koordinaten zu suchen, während die Attribute des Textur Stufen Zustands berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="5484b-129">Texture sampling uses texture coordinates to look up, or sample, a color value at the specified (u,v,w,q) coordinates while taking into account the texture stage state attributes.</span></span>

<span data-ttu-id="5484b-130">Die Texturkoordinaten Daten werden aus den vertextextur-Koordinatendaten interpoliert und einer bestimmten Textur Phase zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5484b-130">The texture coordinate data is interpolated from the vertex texture coordinate data and is associated with a specific texture stage.</span></span> <span data-ttu-id="5484b-131">Die Standard Zuordnung ist eine eins-zu-Eins-Zuordnung zwischen der Reihenfolge der Textur Stufen und der Reihenfolge der Texturkoordinaten Deklaration.</span><span class="sxs-lookup"><span data-stu-id="5484b-131">The default association is a one-to-one mapping between texture stage number and texture coordinate declaration order.</span></span> <span data-ttu-id="5484b-132">Dies bedeutet, dass der erste Satz von Texturkoordinaten, der im Scheitelpunkt Format definiert ist, standardmäßig mit Textur Phase 0 verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="5484b-132">This means that the first set of texture coordinates defined in the vertex format are by default associated with texture stage 0.</span></span>

<span data-ttu-id="5484b-133">Texturkoordinaten können jeder Phase mithilfe von zwei Techniken zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="5484b-133">Texture coordinates may be associated with any stage using two techniques.</span></span> <span data-ttu-id="5484b-134">Wenn Sie einen Scheitelpunkt-Shader oder eine Fixed-Funktions Pipeline verwenden, kann das Textur Stufen-Statusflag TSS \_ texcoordindex in [**settexturestagestate**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) verwendet werden, um Koordinaten zu einer Stufe zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5484b-134">When using a fixed function vertex shader or the fixed function pipeline, the texture stage state flag TSS\_TEXCOORDINDEX can be used in [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) to associate coordinates to a stage.</span></span> <span data-ttu-id="5484b-135">Andernfalls werden die Texturkoordinaten von den Vertex-Shader-OTN-Registern ausgegeben, wenn ein programmierbarer Vertex-Shader verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5484b-135">Otherwise, the texture coordinates are output by the vertex shader oTₙ registers when using a programmable vertex shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5484b-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5484b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5484b-137">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="5484b-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 