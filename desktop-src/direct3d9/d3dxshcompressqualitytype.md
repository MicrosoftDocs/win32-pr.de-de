---
description: Komprimierungs Einstellung für die kugelförmige harmonische (SH).
ms.assetid: 214d6efb-419d-4eea-8360-322885c26bc3
title: D3DXSHCOMPRESSQUALITYTYPE-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHCOMPRESSQUALITYTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d61c70317505442ca4911a13dac8566f9bd7c6fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219495"
---
# <a name="d3dxshcompressqualitytype-enumeration"></a><span data-ttu-id="37798-103">D3DXSHCOMPRESSQUALITYTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="37798-103">D3DXSHCOMPRESSQUALITYTYPE enumeration</span></span>

<span data-ttu-id="37798-104">Komprimierungs Einstellung für die kugelförmige harmonische (SH).</span><span class="sxs-lookup"><span data-stu-id="37798-104">Spherical harmonic (SH) compression setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="37798-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="37798-105">Syntax</span></span>


```C++
typedef enum D3DXSHCOMPRESSQUALITYTYPE { 
  D3DXSHCQUAL_FASTLOWQUALITY   = 1,
  D3DXSHCQUAL_SLOWHIGHQUALITY  = 2,
  D3DXSHCQUAL_FORCE_DWORD      = 0x7fffffff
} D3DXSHCOMPRESSQUALITYTYPE, *LPD3DXSHCOMPRESSQUALITYTYPE;
```



## <a name="constants"></a><span data-ttu-id="37798-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="37798-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="37798-107"><span id="D3DXSHCQUAL_FASTLOWQUALITY"></span><span id="d3dxshcqual_fastlowquality"></span>**D3DXSHCQUAL \_ fastlowquality**</span><span class="sxs-lookup"><span data-stu-id="37798-107"><span id="D3DXSHCQUAL_FASTLOWQUALITY"></span><span id="d3dxshcqual_fastlowquality"></span>**D3DXSHCQUAL\_FASTLOWQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="37798-108">Die Datenkomprimierung ist niedrig, kann jedoch schnell komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="37798-108">The data compression is low quality, but is fast to compress.</span></span>

</dd> <dt>

<span data-ttu-id="37798-109"><span id="D3DXSHCQUAL_SLOWHIGHQUALITY"></span><span id="d3dxshcqual_slowhighquality"></span>**D3DXSHCQUAL \_ slowhighquality**</span><span class="sxs-lookup"><span data-stu-id="37798-109"><span id="D3DXSHCQUAL_SLOWHIGHQUALITY"></span><span id="d3dxshcqual_slowhighquality"></span>**D3DXSHCQUAL\_SLOWHIGHQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="37798-110">Die Datenkomprimierung ist hochwertig, aber langsam zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="37798-110">The data compression is high quality, but is slow to compress.</span></span>

</dd> <dt>

<span data-ttu-id="37798-111"><span id="D3DXSHCQUAL_FORCE_DWORD"></span><span id="d3dxshcqual_force_dword"></span>**D3DXSHCQUAL \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="37798-111"><span id="D3DXSHCQUAL_FORCE_DWORD"></span><span id="d3dxshcqual_force_dword"></span>**D3DXSHCQUAL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="37798-112">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="37798-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="37798-113">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="37798-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="37798-114">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="37798-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37798-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37798-115">Requirements</span></span>



| <span data-ttu-id="37798-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37798-116">Requirement</span></span> | <span data-ttu-id="37798-117">Wert</span><span class="sxs-lookup"><span data-stu-id="37798-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37798-118">Header</span><span class="sxs-lookup"><span data-stu-id="37798-118">Header</span></span><br/> | <dl> <span data-ttu-id="37798-119"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="37798-119"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37798-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37798-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37798-121">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="37798-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




