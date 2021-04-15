---
description: Definiert die samplingtexttypen für Scheitelpunkt-Shader.
ms.assetid: 8e9923f9-6f30-45e5-a557-f26d441a534d
title: D3DSAMPLER_TEXTURE_TYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLER_TEXTURE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 337e8b25a8ec8389a6252fb48582128c601730ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394062"
---
# <a name="d3dsampler_texture_type-enumeration"></a><span data-ttu-id="e8451-103">D3DSAMPLER \_ Texture \_ Type-Enumeration</span><span class="sxs-lookup"><span data-stu-id="e8451-103">D3DSAMPLER\_TEXTURE\_TYPE enumeration</span></span>

<span data-ttu-id="e8451-104">Definiert die samplingtexttypen für Scheitelpunkt-Shader.</span><span class="sxs-lookup"><span data-stu-id="e8451-104">Defines the sampler texture types for vertex shaders.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8451-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8451-105">Syntax</span></span>


```C++
typedef enum D3DSAMPLER_TEXTURE_TYPE { 
  D3DSTT_UNKNOWN,
  D3DSTT_2D,
  D3DSTT_CUBE,
  D3DSTT_VOLUME,
  D3DSTT_FORCE_DWORD
} D3DSAMPLER_TEXTURE_TYPE, *LPD3DSAMPLER_TEXTURE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="e8451-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e8451-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e8451-107"><span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="e8451-107"><span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="e8451-108">Nicht initialisierter Wert.</span><span class="sxs-lookup"><span data-stu-id="e8451-108">Uninitialized value.</span></span> <span data-ttu-id="e8451-109">Der Wert dieses Elements ist 0 &lt; &lt; D3DSP \_ TextureType \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="e8451-109">The value of this element is 0 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="e8451-110"><span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT \_ 2D**</span><span class="sxs-lookup"><span data-stu-id="e8451-110"><span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT\_2D**</span></span>
</dt> <dd>

<span data-ttu-id="e8451-111">Deklarieren einer 2D-Textur.</span><span class="sxs-lookup"><span data-stu-id="e8451-111">Declaring a 2D texture.</span></span> <span data-ttu-id="e8451-112">Der Wert dieses Elements ist 2 &lt; &lt; D3DSP \_ TextureType \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="e8451-112">The value of this element is 2 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="e8451-113"><span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**D3DSTT- \_ Cube**</span><span class="sxs-lookup"><span data-stu-id="e8451-113"><span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**D3DSTT\_CUBE**</span></span>
</dt> <dd>

<span data-ttu-id="e8451-114">Deklarieren einer Cube-Textur.</span><span class="sxs-lookup"><span data-stu-id="e8451-114">Declaring a cube texture.</span></span> <span data-ttu-id="e8451-115">Der Wert dieses Elements ist 3 &lt; &lt; D3DSP \_ TextureType \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="e8451-115">The value of this element is 3 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="e8451-116"><span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**D3DSTT- \_ Volume**</span><span class="sxs-lookup"><span data-stu-id="e8451-116"><span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**D3DSTT\_VOLUME**</span></span>
</dt> <dd>

<span data-ttu-id="e8451-117">Deklarieren einer volumetextur.</span><span class="sxs-lookup"><span data-stu-id="e8451-117">Declaring a volume texture.</span></span> <span data-ttu-id="e8451-118">Der Wert dieses Elements ist 4 &lt; &lt; D3DSP \_ TextureType \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="e8451-118">The value of this element is 4 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="e8451-119"><span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e8451-119"><span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="e8451-120">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="e8451-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="e8451-121">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="e8451-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="e8451-122">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8451-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8451-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8451-123">Requirements</span></span>



| <span data-ttu-id="e8451-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8451-124">Requirement</span></span> | <span data-ttu-id="e8451-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e8451-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8451-126">Header</span><span class="sxs-lookup"><span data-stu-id="e8451-126">Header</span></span><br/> | <dl> <span data-ttu-id="e8451-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8451-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8451-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8451-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8451-129">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="e8451-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




