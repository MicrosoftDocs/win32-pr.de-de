---
description: Definiert den Speicherort, an dem für Beleuchtungsberechnungen auf eine Farb-oder Farbkomponente zugegriffen werden muss.
ms.assetid: 76061d47-a31c-4008-aa8d-a0464dd3423f
title: D3DMATERIALCOLORSOURCE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIALCOLORSOURCE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8877eece8e33c6508768b22c989e992cf8178823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354379"
---
# <a name="d3dmaterialcolorsource-enumeration"></a><span data-ttu-id="eb1cf-103">D3DMATERIALCOLORSOURCE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="eb1cf-103">D3DMATERIALCOLORSOURCE enumeration</span></span>

<span data-ttu-id="eb1cf-104">Definiert den Speicherort, an dem für Beleuchtungsberechnungen auf eine Farb-oder Farbkomponente zugegriffen werden muss.</span><span class="sxs-lookup"><span data-stu-id="eb1cf-104">Defines the location at which a color or color component must be accessed for lighting calculations.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb1cf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb1cf-105">Syntax</span></span>


```C++
typedef enum D3DMATERIALCOLORSOURCE { 
  D3DMCS_MATERIAL     = 0,
  D3DMCS_COLOR1       = 1,
  D3DMCS_COLOR2       = 2,
  D3DMCS_FORCE_DWORD  = 0x7fffffff
} D3DMATERIALCOLORSOURCE, *LPD3DMATERIALCOLORSOURCE;
```



## <a name="constants"></a><span data-ttu-id="eb1cf-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="eb1cf-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="eb1cf-107"><span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**D3DMCS \_ Material**</span><span class="sxs-lookup"><span data-stu-id="eb1cf-107"><span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**D3DMCS\_MATERIAL**</span></span>
</dt> <dd>

<span data-ttu-id="eb1cf-108">Verwenden Sie die Farbe aus dem aktuellen Material.</span><span class="sxs-lookup"><span data-stu-id="eb1cf-108">Use the color from the current material.</span></span>

</dd> <dt>

<span data-ttu-id="eb1cf-109"><span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS \_ COLOR1**</span><span class="sxs-lookup"><span data-stu-id="eb1cf-109"><span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS\_COLOR1**</span></span>
</dt> <dd>

<span data-ttu-id="eb1cf-110">Verwenden Sie die diffuse Scheitelpunkt Farbe.</span><span class="sxs-lookup"><span data-stu-id="eb1cf-110">Use the diffuse vertex color.</span></span>

</dd> <dt>

<span data-ttu-id="eb1cf-111"><span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS \_ COLOR2**</span><span class="sxs-lookup"><span data-stu-id="eb1cf-111"><span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS\_COLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="eb1cf-112">Verwenden Sie die Glanz Farbe des Scheitel Punkts.</span><span class="sxs-lookup"><span data-stu-id="eb1cf-112">Use the specular vertex color.</span></span>

</dd> <dt>

<span data-ttu-id="eb1cf-113"><span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="eb1cf-113"><span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="eb1cf-114">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="eb1cf-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="eb1cf-115">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="eb1cf-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="eb1cf-116">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb1cf-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb1cf-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb1cf-117">Remarks</span></span>

<span data-ttu-id="eb1cf-118">Diese Flags werden verwendet, um den Wert der folgenden Rendering-Zustände im [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) -enumerierten Typ festzulegen.</span><span class="sxs-lookup"><span data-stu-id="eb1cf-118">These flags are used to set the value of the following render states in the [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type.</span></span>

-   <span data-ttu-id="eb1cf-119">D3DRS \_ AmbientMaterialSource</span><span class="sxs-lookup"><span data-stu-id="eb1cf-119">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="eb1cf-120">D3DRS \_ DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="eb1cf-120">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="eb1cf-121">D3DRS \_ emissivematerialsource</span><span class="sxs-lookup"><span data-stu-id="eb1cf-121">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>
-   <span data-ttu-id="eb1cf-122">D3DRS \_ SpecularMaterialSource</span><span class="sxs-lookup"><span data-stu-id="eb1cf-122">D3DRS\_SPECULARMATERIALSOURCE</span></span>

## <a name="requirements"></a><span data-ttu-id="eb1cf-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb1cf-123">Requirements</span></span>



| <span data-ttu-id="eb1cf-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb1cf-124">Requirement</span></span> | <span data-ttu-id="eb1cf-125">Wert</span><span class="sxs-lookup"><span data-stu-id="eb1cf-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb1cf-126">Header</span><span class="sxs-lookup"><span data-stu-id="eb1cf-126">Header</span></span><br/> | <dl> <span data-ttu-id="eb1cf-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb1cf-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb1cf-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb1cf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb1cf-129">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="eb1cf-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="eb1cf-130">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="eb1cf-130">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
