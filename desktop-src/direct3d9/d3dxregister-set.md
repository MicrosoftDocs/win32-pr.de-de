---
description: Der Datentyp des Registers.
ms.assetid: b54530d3-4267-4b41-9a16-59d400ef3e18
title: D3DXREGISTER_SET-Enumeration (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXREGISTER_SET
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 683b13d0b386fcdbc162293455e2beb11bc1ee85
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361194"
---
# <a name="d3dxregister_set-enumeration"></a><span data-ttu-id="0f59e-103">D3DXREGISTER \_ Set-Enumeration</span><span class="sxs-lookup"><span data-stu-id="0f59e-103">D3DXREGISTER\_SET enumeration</span></span>

<span data-ttu-id="0f59e-104">Der Datentyp des Registers.</span><span class="sxs-lookup"><span data-stu-id="0f59e-104">Data type of the register.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f59e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f59e-105">Syntax</span></span>


```C++
typedef enum _D3DXREGISTER_SET { 
  D3DXRS_BOOL,
  D3DXRS_INT4,
  D3DXRS_FLOAT4,
  D3DXRS_SAMPLER,
  D3DXRS_FORCE_DWORD  = 0x7fffffff
} D3DXREGISTER_SET, *LPD3DXREGISTER_SET;
```



## <a name="constants"></a><span data-ttu-id="0f59e-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="0f59e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0f59e-107"><span id="D3DXRS_BOOL"></span><span id="d3dxrs_bool"></span>**D3DXRS \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0f59e-107"><span id="D3DXRS_BOOL"></span><span id="d3dxrs_bool"></span>**D3DXRS\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="0f59e-108">Boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="0f59e-108">Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="0f59e-109"><span id="D3DXRS_INT4"></span><span id="d3dxrs_int4"></span>**D3DXRS \_ INT4**</span><span class="sxs-lookup"><span data-stu-id="0f59e-109"><span id="D3DXRS_INT4"></span><span id="d3dxrs_int4"></span>**D3DXRS\_INT4**</span></span>
</dt> <dd>

<span data-ttu-id="0f59e-110">4D-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="0f59e-110">4D integer number.</span></span>

</dd> <dt>

<span data-ttu-id="0f59e-111"><span id="D3DXRS_FLOAT4"></span><span id="d3dxrs_float4"></span>**D3DXRS \_ float4**</span><span class="sxs-lookup"><span data-stu-id="0f59e-111"><span id="D3DXRS_FLOAT4"></span><span id="d3dxrs_float4"></span>**D3DXRS\_FLOAT4**</span></span>
</dt> <dd>

<span data-ttu-id="0f59e-112">4D-Gleit Komma Zahl.</span><span class="sxs-lookup"><span data-stu-id="0f59e-112">4D floating-point number.</span></span>

</dd> <dt>

<span data-ttu-id="0f59e-113"><span id="D3DXRS_SAMPLER"></span><span id="d3dxrs_sampler"></span>**D3DXRS- \_ Sampler**</span><span class="sxs-lookup"><span data-stu-id="0f59e-113"><span id="D3DXRS_SAMPLER"></span><span id="d3dxrs_sampler"></span>**D3DXRS\_SAMPLER**</span></span>
</dt> <dd>

<span data-ttu-id="0f59e-114">Das Register enthält 4D-Samplingdaten.</span><span class="sxs-lookup"><span data-stu-id="0f59e-114">The register contains 4D sampler data.</span></span>

</dd> <dt>

<span data-ttu-id="0f59e-115"><span id="D3DXRS_FORCE_DWORD"></span><span id="d3dxrs_force_dword"></span>**D3DXRS \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0f59e-115"><span id="D3DXRS_FORCE_DWORD"></span><span id="d3dxrs_force_dword"></span>**D3DXRS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0f59e-116">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="0f59e-116">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0f59e-117">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="0f59e-117">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0f59e-118">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f59e-118">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f59e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f59e-119">Requirements</span></span>



| <span data-ttu-id="0f59e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f59e-120">Requirement</span></span> | <span data-ttu-id="0f59e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0f59e-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f59e-122">Header</span><span class="sxs-lookup"><span data-stu-id="0f59e-122">Header</span></span><br/> | <dl> <span data-ttu-id="0f59e-123"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f59e-123"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f59e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f59e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f59e-125">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="0f59e-125">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="0f59e-126">**D3DXSHADER \_ constantinfo**</span><span class="sxs-lookup"><span data-stu-id="0f59e-126">**D3DXSHADER\_CONSTANTINFO**</span></span>](d3dxshader-constantinfo.md)
</dt> <dt>

[<span data-ttu-id="0f59e-127">**D3DXCONSTANT- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="0f59e-127">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




