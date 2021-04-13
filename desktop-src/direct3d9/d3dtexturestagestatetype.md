---
description: Textur Stufen Zustände definieren MULTIMIXER-Textur Vorgänge.
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: D3DTEXTURESTAGESTATETYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURESTAGESTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0530f428c9ebf89607fa89509c65ddd336fee293
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219479"
---
# <a name="d3dtexturestagestatetype-enumeration"></a><span data-ttu-id="a7c1a-103">D3DTEXTURESTAGESTATETYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="a7c1a-103">D3DTEXTURESTAGESTATETYPE enumeration</span></span>

<span data-ttu-id="a7c1a-104">Textur Stufen Zustände definieren MULTIMIXER-Textur Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-104">Texture stage states define multi-blender texture operations.</span></span> <span data-ttu-id="a7c1a-105">Einige samplerzustände richten die Vertexverarbeitung ein, und einige richten die Pixel Verarbeitung ein.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-105">Some sampler states set up vertex processing, and some set up pixel processing.</span></span> <span data-ttu-id="a7c1a-106">Textur Stufen Zustände können mithilfe von stateblocks gespeichert und wieder hergestellt werden (siehe [Status Blöcke speichern und Wiederherstellen (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="a7c1a-106">Texture stage states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7c1a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7c1a-107">Syntax</span></span>


```C++
typedef enum D3DTEXTURESTAGESTATETYPE { 
  D3DTSS_COLOROP                = 1,
  D3DTSS_COLORARG1              = 2,
  D3DTSS_COLORARG2              = 3,
  D3DTSS_ALPHAOP                = 4,
  D3DTSS_ALPHAARG1              = 5,
  D3DTSS_ALPHAARG2              = 6,
  D3DTSS_BUMPENVMAT00           = 7,
  D3DTSS_BUMPENVMAT01           = 8,
  D3DTSS_BUMPENVMAT10           = 9,
  D3DTSS_BUMPENVMAT11           = 10,
  D3DTSS_TEXCOORDINDEX          = 11,
  D3DTSS_BUMPENVLSCALE          = 22,
  D3DTSS_BUMPENVLOFFSET         = 23,
  D3DTSS_TEXTURETRANSFORMFLAGS  = 24,
  D3DTSS_COLORARG0              = 26,
  D3DTSS_ALPHAARG0              = 27,
  D3DTSS_RESULTARG              = 28,
  D3DTSS_CONSTANT               = 32,
  D3DTSS_FORCE_DWORD            = 0x7fffffff
} D3DTEXTURESTAGESTATETYPE, *LPD3DTEXTURESTAGESTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="a7c1a-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="a7c1a-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a7c1a-109"><span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS \_ colorop**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-109"><span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS\_COLOROP**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-110">Der Textur Zustand ist ein Textur Farb Mischungs Vorgang, der durch einen Member des [**D3DTEXTUREOP**](./d3dtextureop.md) -Enumerationstyps identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-110">Texture-stage state is a texture color blending operation identified by one member of the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span> <span data-ttu-id="a7c1a-111">Der Standardwert für die erste Textur Phase (Phase 0) ist D3DTOP \_ modulate; für alle anderen Stufen lautet der Standardwert D3DTOP \_ deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-111">The default value for the first texture stage (stage 0) is D3DTOP\_MODULATE; for all other stages the default is D3DTOP\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-112"><span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS \_ COLORARG1**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-112"><span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS\_COLORARG1**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-113">Der Textur Stufen Status ist das erste Farb Argument für die Stufe, das durch eine der [D3DTA](d3dta.md)identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-113">Texture-stage state is the first color argument for the stage, identified by one of the [D3DTA](d3dta.md).</span></span> <span data-ttu-id="a7c1a-114">Das Standardargument ist D3DTA \_ Texture.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-114">The default argument is D3DTA\_TEXTURE.</span></span>

<span data-ttu-id="a7c1a-115">Geben \_ Sie D3DTA Temp an, um eine temporäre Register Farbe für Lese-oder Schreibvorgänge auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-115">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="a7c1a-116">D3DTA \_ Temp wird unterstützt, wenn die D3DPMISCCAPS \_ tssargtemp-Geräte Funktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-116">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="a7c1a-117">Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="a7c1a-117">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-118"><span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS \_ COLORARG2**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-118"><span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS\_COLORARG2**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-119">Der Textur Zustand ist das zweite Farb Argument für die Stufe, das durch [D3DTA](d3dta.md)identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-119">Texture-stage state is the second color argument for the stage, identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="a7c1a-120">Das Standardargument ist D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-120">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="a7c1a-121">Geben \_ Sie D3DTA Temp an, um eine temporäre Register Farbe für Lese-oder Schreibvorgänge auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-121">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="a7c1a-122">D3DTA \_ Temp wird unterstützt, wenn die D3DPMISCCAPS \_ tssargtemp-Geräte Funktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-122">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="a7c1a-123">Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="a7c1a-123">The default value for the register is (0.0, 0.0, 0.0, 0.0)</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-124"><span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS \_ alphaop**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-124"><span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS\_ALPHAOP**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-125">Der Textur Zustand ist ein Textur Alpha-Mischungs Vorgang, der durch einen Member des [**D3DTEXTUREOP**](./d3dtextureop.md) -Enumerationstyps identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-125">Texture-stage state is a texture alpha blending operation identified by one member of the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span> <span data-ttu-id="a7c1a-126">Der Standardwert für die erste Textur Phase (Phase 0) ist D3DTOP \_ SELECTARG1, und für alle anderen Stufen lautet der Standardwert D3DTOP \_ deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-126">The default value for the first texture stage (stage 0) is D3DTOP\_SELECTARG1, and for all other stages the default is D3DTOP\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-127"><span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS \_ ALPHAARG1**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-127"><span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS\_ALPHAARG1**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-128">Der Textur Zustand ist das erste Alpha Argument für die Stufe, das durch [D3DTA](d3dta.md)identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-128">Texture-stage state is the first alpha argument for the stage, identified by by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="a7c1a-129">Das Standardargument ist D3DTA \_ Texture.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-129">The default argument is D3DTA\_TEXTURE.</span></span> <span data-ttu-id="a7c1a-130">Wenn für diese Stufe keine Textur festgelegt ist, ist das Standardargument D3DTA \_ diffus.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-130">If no texture is set for this stage, the default argument is D3DTA\_DIFFUSE.</span></span> <span data-ttu-id="a7c1a-131">Geben \_ Sie D3DTA Temp an, um eine temporäre Register Farbe für Lese-oder Schreibvorgänge auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-131">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="a7c1a-132">D3DTA \_ Temp wird unterstützt, wenn die D3DPMISCCAPS \_ tssargtemp-Geräte Funktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-132">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="a7c1a-133">Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="a7c1a-133">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-134"><span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS \_ ALPHAARG2**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-134"><span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS\_ALPHAARG2**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-135">Der Textur Zustand ist das zweite Alpha Argument für die Stufe, das durch [D3DTA](d3dta.md)identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-135">Texture-stage state is the second alpha argument for the stage, identified by by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="a7c1a-136">Das Standardargument ist D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-136">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="a7c1a-137">Geben \_ Sie D3DTA Temp an, um eine temporäre Register Farbe für Lese-oder Schreibvorgänge auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-137">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="a7c1a-138">D3DTA \_ Temp wird unterstützt, wenn die D3DPMISCCAPS \_ tssargtemp-Geräte Funktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-138">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="a7c1a-139">Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="a7c1a-139">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-140"><span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS \_ BUMPENVMAT00**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-140"><span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS\_BUMPENVMAT00**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-141">Der Textur Zustand ist ein Gleit Komma Wert für den \[ \] \[ Koeffizienten 0 0 \] in einer Bump-mappingmatrix.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-141">Texture-stage state is a floating-point value for the \[0\]\[0\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="a7c1a-142">Der Standardwert ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-142">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-143"><span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS \_ BUMPENVMAT01**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-143"><span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS\_BUMPENVMAT01**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-144">Der Textur Zustand ist ein Gleit Komma Wert für den \[ \] \[ Koeffizienten 0 1 \] in einer Bump-mappingmatrix.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-144">Texture-stage state is a floating-point value for the \[0\]\[1\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="a7c1a-145">Der Standardwert ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-145">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-146"><span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS \_ BUMPENVMAT10**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-146"><span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS\_BUMPENVMAT10**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-147">Der Textur Zustand ist ein Gleit Komma Wert für den \[ 1 \] \[ 0 \] -Koeffizienten in einer Bump-mappingmatrix.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-147">Texture-stage state is a floating-point value for the \[1\]\[0\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="a7c1a-148">Der Standardwert ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-148">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-149"><span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS \_ BUMPENVMAT11**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-149"><span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS\_BUMPENVMAT11**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-150">Der Textur Zustand ist ein Gleit Komma Wert für den \[ 1 1- \] \[ \] Koeffizienten in einer Bump-mappingmatrix.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-150">Texture-stage state is a floating-point value for the \[1\]\[1\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="a7c1a-151">Der Standardwert ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-151">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-152"><span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS \_ texcoordindex**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-152"><span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS\_TEXCOORDINDEX**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-153">Der Index der Texturkoordinaten Menge, die mit dieser Textur Phase verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-153">Index of the texture coordinate set to use with this texture stage.</span></span> <span data-ttu-id="a7c1a-154">Sie können bis zu acht Sätze von Texturkoordinaten pro Scheitelpunkt angeben.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-154">You can specify up to eight sets of texture coordinates per vertex.</span></span> <span data-ttu-id="a7c1a-155">Wenn ein Scheitelpunkt keinen Satz von Texturkoordinaten am angegebenen Index enthält, werden standardmäßig die Koordinaten "You" und "v" (0, 0) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-155">If a vertex does not include a set of texture coordinates at the specified index, the system defaults to the u and v coordinates (0,0).</span></span>

<span data-ttu-id="a7c1a-156">Beim Rendering mithilfe von Vertex-Shadern muss der Texturkoordinaten Index jeder Phase auf den Standardwert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-156">When rendering using vertex shaders, each stage's texture coordinate index must be set to its default value.</span></span> <span data-ttu-id="a7c1a-157">Der Standard Index für jede Stufe ist gleich dem Phasen Index.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-157">The default index for each stage is equal to the stage index.</span></span> <span data-ttu-id="a7c1a-158">Legen Sie diesen Status auf den NULL basierten Index des Koordinaten Satzes für jeden Scheitelpunkt fest, den diese Textur Phase verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-158">Set this state to the zero-based index of the coordinate set for each vertex that this texture stage uses.</span></span>

<span data-ttu-id="a7c1a-159">Darüber hinaus können Anwendungen, als logisch oder mit dem Index festgelegt werden, eine der Konstanten, die Direct3D automatisch die Eingabe Texturkoordinaten für eine Textur Transformation generieren.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-159">Additionally, applications can include, as logical OR with the index being set, one of the constants to request that Direct3D automatically generate the input texture coordinates for a texture transformation.</span></span> <span data-ttu-id="a7c1a-160">Eine Liste aller Konstanten finden Sie unter [D3DTSS \_ TCI](d3dtss-tci.md).</span><span class="sxs-lookup"><span data-stu-id="a7c1a-160">For a list of all the constants, see [D3DTSS\_TCI](d3dtss-tci.md).</span></span>

<span data-ttu-id="a7c1a-161">Mit Ausnahme von D3DTSS \_ TCI \_ passthru, das in NULL aufgelöst wird, verwendet das System den Index streng, um den Textur umschließmodus zu bestimmen, wenn einer der folgenden Werte im festgelegten Index enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-161">With the exception of D3DTSS\_TCI\_PASSTHRU, which resolves to zero, if any of the following values is included with the index being set, the system uses the index strictly to determine texture wrapping mode.</span></span> <span data-ttu-id="a7c1a-162">Diese Flags sind besonders nützlich, wenn Sie die Umgebungs Zuordnung durchführen.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-162">These flags are most useful when performing environment mapping.</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-163"><span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS \_ bumpendvlscale**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-163"><span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS\_BUMPENVLSCALE**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-164">Gleit Komma-Skalierungs Wert für die Bump-Map-Beleuchtung.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-164">Floating-point scale value for bump-map luminance.</span></span> <span data-ttu-id="a7c1a-165">Der Standardwert ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-165">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-166"><span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS \_ bumpenvloffset**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-166"><span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS\_BUMPENVLOFFSET**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-167">Gleit Komma Offset Wert für die Bild-und Bild Lauf Beleuchtung.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-167">Floating-point offset value for bump-map luminance.</span></span> <span data-ttu-id="a7c1a-168">Der Standardwert ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-168">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-169"><span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS \_ texturetransformflags**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-169"><span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS\_TEXTURETRANSFORMFLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-170">Member des [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) -Enumerationstyps, der die Transformation von Texturkoordinaten für diese Textur Phase steuert.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-170">Member of the [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) enumerated type that controls the transformation of texture coordinates for this texture stage.</span></span> <span data-ttu-id="a7c1a-171">Der Standardwert ist D3DTTFF \_ deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-171">The default value is D3DTTFF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-172"><span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS \_ COLORARG0**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-172"><span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS\_COLORARG0**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-173">Einstellungen für den dritten Farb Operanden für die Ausführung von Vorgängen (multiplizieren, addieren und Linear Interpolate), die durch [D3DTA](d3dta.md)identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-173">Settings for the third color operand for triadic operations (multiply, add, and linearly interpolate), identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="a7c1a-174">Diese Einstellung wird unterstützt, wenn die \_ Gerätefunktionen D3DTEXOPCAPS MultiplyAdd oder D3DTEXOPCAPS \_ Lerp vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-174">This setting is supported if the D3DTEXOPCAPS\_MULTIPLYADD or D3DTEXOPCAPS\_LERP device capabilities are present.</span></span> <span data-ttu-id="a7c1a-175">Das Standardargument ist D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-175">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="a7c1a-176">Geben \_ Sie D3DTA Temp an, um eine temporäre Register Farbe für Lese-oder Schreibvorgänge auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-176">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="a7c1a-177">D3DTA \_ Temp wird unterstützt, wenn die D3DPMISCCAPS \_ tssargtemp-Geräte Funktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-177">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="a7c1a-178">Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="a7c1a-178">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-179"><span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS \_ ALPHAARG0**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-179"><span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS\_ALPHAARG0**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-180">Einstellungen für den Alphakanal Auswahl-Operanden für Selektor-Vorgänge (multiplizieren, addieren und Linear Interpolate), die durch [D3DTA](d3dta.md)identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-180">Settings for the alpha channel selector operand for triadic operations (multiply, add, and linearly interpolate), identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="a7c1a-181">Diese Einstellung wird unterstützt, wenn die \_ Gerätefunktionen D3DTEXOPCAPS MultiplyAdd oder D3DTEXOPCAPS \_ Lerp vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-181">This setting is supported if the D3DTEXOPCAPS\_MULTIPLYADD or D3DTEXOPCAPS\_LERP device capabilities are present.</span></span> <span data-ttu-id="a7c1a-182">Das Standardargument ist D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-182">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="a7c1a-183">Geben \_ Sie D3DTA Temp an, um eine temporäre Register Farbe für Lese-oder Schreibvorgänge auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-183">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="a7c1a-184">D3DTA \_ Temp wird unterstützt, wenn die D3DPMISCCAPS \_ tssargtemp-Geräte Funktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-184">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="a7c1a-185">Das Standardargument ist (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="a7c1a-185">The default argument is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-186"><span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS \_ resultarg**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-186"><span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS\_RESULTARG**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-187">Die Einstellung zum Auswählen des Ziels für das Ergebnis dieser Phase wird durch [D3DTA](d3dta.md)identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-187">Setting to select destination register for the result of this stage, identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="a7c1a-188">Dieser Wert kann auf D3DTA \_ Current (Standardwert) oder auf D3DTA Temp festgelegt werden. dabei handelt es sich um \_ ein einzelnes temporäres Register, das als Eingabe Argument in nachfolgende Stufen gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-188">This value can be set to D3DTA\_CURRENT (the default value) or to D3DTA\_TEMP, which is a single temporary register that can be read into subsequent stages as an input argument.</span></span> <span data-ttu-id="a7c1a-189">Die endgültige Farbe, die an den nebelmixer und den Frame Puffer übertragen wird, wird von D3DTA \_ Current übernommen, sodass der letzte aktive Textur Phasen Zustand auf den aktuellen Wert festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-189">The final color passed to the fog blender and frame buffer is taken from D3DTA\_CURRENT, so the last active texture stage state must be set to write to current.</span></span> <span data-ttu-id="a7c1a-190">Diese Einstellung wird unterstützt, wenn die D3DPMISCCAPS \_ tssargtemp-Geräte Funktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-190">This setting is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-191"><span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS- \_ Konstante**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-191"><span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS\_CONSTANT**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-192">Einstufige Konstante Farbe.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-192">Per-stage constant color.</span></span> <span data-ttu-id="a7c1a-193">Informationen dazu, ob ein Gerät eine einstufige Konstante Konstante unterstützt, finden Sie \_ in der D3DPMISCCAPS perstageconstant-Konstante in [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="a7c1a-193">To see if a device supports a per-stage constant color, see the D3DPMISCCAPS\_PERSTAGECONSTANT constant in [D3DPMISCCAPS](d3dpmisccaps.md).</span></span> <span data-ttu-id="a7c1a-194">D3DTSS- \_ Konstante wird von D3DTA- \_ Konstanten verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-194">D3DTSS\_CONSTANT is used by D3DTA\_CONSTANT.</span></span> <span data-ttu-id="a7c1a-195">Siehe [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="a7c1a-195">See [D3DTA](d3dta.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7c1a-196"><span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-196"><span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a7c1a-197">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-197">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a7c1a-198">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-198">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a7c1a-199">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-199">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7c1a-200">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7c1a-200">Remarks</span></span>

<span data-ttu-id="a7c1a-201">Member dieses Enumerationstyps werden mit den Methoden [**IDirect3DDevice9:: gettexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) und [**IDirect3DDevice9:: settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) verwendet, um Textur Zustands Werte abzurufen und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-201">Members of this enumerated type are used with the [**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) and [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) methods to retrieve and set texture state values.</span></span>

<span data-ttu-id="a7c1a-202">Der gültige Wertebereich für die \_ Matrizen der D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT01, D3DTSS \_ BUMPENVMAT10 und D3DTSS \_ BUMPENVMAT11 Bump-Mapping-Matrix ist größer als oder gleich-8,0 und kleiner als 8,0.</span><span class="sxs-lookup"><span data-stu-id="a7c1a-202">The valid range of values for the D3DTSS\_BUMPENVMAT00, D3DTSS\_BUMPENVMAT01, D3DTSS\_BUMPENVMAT10, and D3DTSS\_BUMPENVMAT11 bump-mapping matrix coefficients is greater than or equal to -8.0 and less than 8.0.</span></span> <span data-ttu-id="a7c1a-203">Dieser Bereich wird in mathematischer Notation ausgedrückt (-8.0, 8.0).</span><span class="sxs-lookup"><span data-stu-id="a7c1a-203">This range, expressed in mathematical notation is (-8.0,8.0).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7c1a-204">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7c1a-204">Requirements</span></span>



| <span data-ttu-id="a7c1a-205">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7c1a-205">Requirement</span></span> | <span data-ttu-id="a7c1a-206">Wert</span><span class="sxs-lookup"><span data-stu-id="a7c1a-206">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7c1a-207">Header</span><span class="sxs-lookup"><span data-stu-id="a7c1a-207">Header</span></span><br/> | <dl> <span data-ttu-id="a7c1a-208"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7c1a-208"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7c1a-209">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7c1a-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7c1a-210">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="a7c1a-210">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="a7c1a-211">**IDirect3DDevice9:: gettexturestagestate**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-211">**IDirect3DDevice9::GetTextureStageState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[<span data-ttu-id="a7c1a-212">**IDirect3DDevice9:: settexturestagestate**</span><span class="sxs-lookup"><span data-stu-id="a7c1a-212">**IDirect3DDevice9::SetTextureStageState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
