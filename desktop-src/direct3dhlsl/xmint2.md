---
title: XMINT2-Struktur
description: Beschreibt einen 2D-Ganzzahlvektor.
ms.assetid: 651f62f8-577d-4356-9bbc-0d4a9ca8fb01
keywords:
- XMINT2-Struktur HLSL
topic_type:
- apiref
api_name:
- XMINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5dfe4aab8a23dbf1b7921742272b0d2b0ab2382
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549985"
---
# <a name="xmint2-structure"></a><span data-ttu-id="ec855-104">XMINT2-Struktur</span><span class="sxs-lookup"><span data-stu-id="ec855-104">XMINT2 structure</span></span>

<span data-ttu-id="ec855-105">Beschreibt einen 2D-Ganzzahlvektor.</span><span class="sxs-lookup"><span data-stu-id="ec855-105">Describes an 2D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec855-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec855-106">Syntax</span></span>


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
```



## <a name="members"></a><span data-ttu-id="ec855-107">Member</span><span class="sxs-lookup"><span data-stu-id="ec855-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ec855-108">**x**</span><span class="sxs-lookup"><span data-stu-id="ec855-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="ec855-109">x-component des Vektors.</span><span class="sxs-lookup"><span data-stu-id="ec855-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="ec855-110">**y**</span><span class="sxs-lookup"><span data-stu-id="ec855-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="ec855-111">y-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="ec855-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="ec855-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec855-112">Remarks</span></span>

<span data-ttu-id="ec855-113">Diese Struktur wird im ``D3DX\_DXGIFormatConvert.inl`` Header im DirectX SDK (Juni 2010) für die Verwendung in C++ definiert.</span><span class="sxs-lookup"><span data-stu-id="ec855-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="ec855-114">Die neueste Version dieses Headers im NuGet-Paket [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) definiert ihn nicht mehr und basiert stattdessen auf [DirectX::XMINT2](/windows/win32/api/directxmath/ns-directxmath-xmint2) in DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="ec855-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT2](/windows/win32/api/directxmath/ns-directxmath-xmint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="ec855-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec855-115">Requirements</span></span>



| <span data-ttu-id="ec855-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec855-116">Requirement</span></span> | <span data-ttu-id="ec855-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ec855-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec855-118">Header</span><span class="sxs-lookup"><span data-stu-id="ec855-118">Header</span></span><br/> | <dl> <span data-ttu-id="ec855-119"><dt>D3DX \_ DXGIFormatConvert.inl</dt></span><span class="sxs-lookup"><span data-stu-id="ec855-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec855-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec855-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec855-121">Strukturen</span><span class="sxs-lookup"><span data-stu-id="ec855-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="ec855-122">Entpacken und Packen von DXGI \_ FORMAT für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="ec855-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>