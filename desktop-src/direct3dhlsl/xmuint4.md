---
title: XMUINT4-Struktur
description: Beschreibt einen 4D-Ganzzahlvektor ohne Vorzeichen.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- XMUINT4-Struktur HLSL
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e424b4e5fd1c97f5aec01571d887b54dbb143b7
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549895"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="61b62-104">XMUINT4-Struktur</span><span class="sxs-lookup"><span data-stu-id="61b62-104">XMUINT4 structure</span></span>

<span data-ttu-id="61b62-105">Beschreibt einen 4D-Ganzzahlvektor ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="61b62-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="61b62-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="61b62-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a><span data-ttu-id="61b62-107">Member</span><span class="sxs-lookup"><span data-stu-id="61b62-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="61b62-108">**x**</span><span class="sxs-lookup"><span data-stu-id="61b62-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="61b62-109">x-component des Vektors.</span><span class="sxs-lookup"><span data-stu-id="61b62-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="61b62-110">**y**</span><span class="sxs-lookup"><span data-stu-id="61b62-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="61b62-111">y-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="61b62-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="61b62-112">**Z**</span><span class="sxs-lookup"><span data-stu-id="61b62-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="61b62-113">z-component des Vektors.</span><span class="sxs-lookup"><span data-stu-id="61b62-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="61b62-114">**w**</span><span class="sxs-lookup"><span data-stu-id="61b62-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="61b62-115">w-component des Vektors.</span><span class="sxs-lookup"><span data-stu-id="61b62-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a><span data-ttu-id="61b62-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="61b62-116">Remarks</span></span>

<span data-ttu-id="61b62-117">Diese Struktur wird im ``D3DX\_DXGIFormatConvert.inl`` Header im DirectX SDK (Juni 2010) für die Verwendung in C++ definiert.</span><span class="sxs-lookup"><span data-stu-id="61b62-117">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="61b62-118">Die neueste Version dieses Headers im NuGet-Paket [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) definiert ihn nicht mehr und basiert stattdessen auf [DirectX::XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) in DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="61b62-118">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) in DirectXMath instead.</span></span>




## <a name="requirements"></a><span data-ttu-id="61b62-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61b62-119">Requirements</span></span>



| <span data-ttu-id="61b62-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61b62-120">Requirement</span></span> | <span data-ttu-id="61b62-121">Wert</span><span class="sxs-lookup"><span data-stu-id="61b62-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61b62-122">Header</span><span class="sxs-lookup"><span data-stu-id="61b62-122">Header</span></span><br/> | <dl> <span data-ttu-id="61b62-123"><dt>D3DX \_ DXGIFormatConvert.inl</dt></span><span class="sxs-lookup"><span data-stu-id="61b62-123"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61b62-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61b62-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b62-125">Strukturen</span><span class="sxs-lookup"><span data-stu-id="61b62-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="61b62-126">Entpacken und Packen von DXGI \_ FORMAT für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="61b62-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>