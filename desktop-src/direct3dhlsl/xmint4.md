---
title: XMINT4-Struktur
description: Beschreibt einen 4D-Ganzzahlvektor.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- XMINT4-Struktur HLSL
topic_type:
- apiref
api_name:
- XMINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead9e7da8d48025c456ae6e57b0ffe64cdb00f46
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549955"
---
# <a name="xmint4-structure"></a><span data-ttu-id="8b19c-104">XMINT4-Struktur</span><span class="sxs-lookup"><span data-stu-id="8b19c-104">XMINT4 structure</span></span>

<span data-ttu-id="8b19c-105">Beschreibt einen 4D-Ganzzahlvektor.</span><span class="sxs-lookup"><span data-stu-id="8b19c-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b19c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b19c-106">Syntax</span></span>


``` syntax
typedef struct _XMINT4 {
  INT x;
  INT {
    INT {
      INT w;
    }z;
  }y;
} XMINT4;
```



## <a name="members"></a><span data-ttu-id="8b19c-107">Member</span><span class="sxs-lookup"><span data-stu-id="8b19c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8b19c-108">**x**</span><span class="sxs-lookup"><span data-stu-id="8b19c-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="8b19c-109">x-component des Vektors.</span><span class="sxs-lookup"><span data-stu-id="8b19c-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="8b19c-110">**y**</span><span class="sxs-lookup"><span data-stu-id="8b19c-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="8b19c-111">y-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="8b19c-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="8b19c-112">**Z**</span><span class="sxs-lookup"><span data-stu-id="8b19c-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="8b19c-113">z-component des Vektors.</span><span class="sxs-lookup"><span data-stu-id="8b19c-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="8b19c-114">**w**</span><span class="sxs-lookup"><span data-stu-id="8b19c-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="8b19c-115">w-component des Vektors.</span><span class="sxs-lookup"><span data-stu-id="8b19c-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b19c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b19c-116">Requirements</span></span>



| <span data-ttu-id="8b19c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b19c-117">Requirement</span></span> | <span data-ttu-id="8b19c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8b19c-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b19c-119">Header</span><span class="sxs-lookup"><span data-stu-id="8b19c-119">Header</span></span><br/> | <dl> <span data-ttu-id="8b19c-120"><dt>D3DX \_ DXGIFormatConvert.inl</dt></span><span class="sxs-lookup"><span data-stu-id="8b19c-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="remarks"></a><span data-ttu-id="8b19c-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b19c-121">Remarks</span></span>

<span data-ttu-id="8b19c-122">Diese Struktur wird im ``D3DX\_DXGIFormatConvert.inl`` Header im DirectX SDK (Juni 2010) für die Verwendung in C++ definiert.</span><span class="sxs-lookup"><span data-stu-id="8b19c-122">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="8b19c-123">Die neueste Version dieses Headers im NuGet-Paket [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) definiert ihn nicht mehr und basiert stattdessen auf [DirectX::XMINT4](/windows/win32/api/directxmath/ns-directxmath-xmint4) in DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="8b19c-123">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT4](/windows/win32/api/directxmath/ns-directxmath-xmint4) in DirectXMath instead.</span></span>



## <a name="see-also"></a><span data-ttu-id="8b19c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b19c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b19c-125">Strukturen</span><span class="sxs-lookup"><span data-stu-id="8b19c-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="8b19c-126">Entpacken und Packen von DXGI \_ FORMAT für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="8b19c-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>