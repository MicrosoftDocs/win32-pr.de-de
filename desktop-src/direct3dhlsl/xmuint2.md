---
title: XMUINT2-Struktur
description: Beschreibt einen 2D-Ganzzahlvektor ohne Vorzeichen.
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- XMUINT2-Struktur – HLSL
topic_type:
- apiref
api_name:
- XMUINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71168d08b8a91e09429a6f4e004c48c699635414
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549565"
---
# <a name="xmuint2-structure"></a><span data-ttu-id="650da-104">XMUINT2-Struktur</span><span class="sxs-lookup"><span data-stu-id="650da-104">XMUINT2 structure</span></span>

<span data-ttu-id="650da-105">Beschreibt einen 2D-Ganzzahlvektor ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="650da-105">Describes an 2D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="650da-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="650da-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
```



## <a name="members"></a><span data-ttu-id="650da-107">Member</span><span class="sxs-lookup"><span data-stu-id="650da-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="650da-108">**x**</span><span class="sxs-lookup"><span data-stu-id="650da-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="650da-109">x-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="650da-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="650da-110">**y**</span><span class="sxs-lookup"><span data-stu-id="650da-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="650da-111">y-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="650da-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="650da-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="650da-112">Remarks</span></span>

<span data-ttu-id="650da-113">Diese Struktur wird im Header ``D3DX\_DXGIFormatConvert.inl`` im DirectX SDK (Juni 2010) für die Verwendung von C++ definiert.</span><span class="sxs-lookup"><span data-stu-id="650da-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="650da-114">Die neueste Version dieses Headers im NuGet-Paket [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) definiert sie nicht mehr und basiert stattdessen auf [DirectX::XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) in DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="650da-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="650da-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="650da-115">Requirements</span></span>



| <span data-ttu-id="650da-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="650da-116">Requirement</span></span> | <span data-ttu-id="650da-117">Wert</span><span class="sxs-lookup"><span data-stu-id="650da-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="650da-118">Header</span><span class="sxs-lookup"><span data-stu-id="650da-118">Header</span></span><br/> | <dl> <span data-ttu-id="650da-119"><dt>D3DX \_ DXGIFormatConvert.inl</dt></span><span class="sxs-lookup"><span data-stu-id="650da-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="650da-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="650da-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="650da-121">Strukturen</span><span class="sxs-lookup"><span data-stu-id="650da-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="650da-122">Entpacken und Packen des \_ DXGI-FORMATS für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="650da-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>