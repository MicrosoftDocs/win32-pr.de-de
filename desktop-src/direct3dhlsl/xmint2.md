---
title: XMINT2-Struktur
description: Beschreibt einen ganzzahligen 2D-Vektor.
ms.assetid: 651f62f8-577d-4356-9bbc-0d4a9ca8fb01
keywords:
- XMINT2-Struktur (HLSL)
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
ms.openlocfilehash: 1e93e26933ad6b3829848e7e826d8d9685e9f141
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222858"
---
# <a name="xmint2-structure"></a><span data-ttu-id="2af05-104">XMINT2-Struktur</span><span class="sxs-lookup"><span data-stu-id="2af05-104">XMINT2 structure</span></span>

<span data-ttu-id="2af05-105">Beschreibt einen ganzzahligen 2D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="2af05-105">Describes an 2D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="2af05-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2af05-106">Syntax</span></span>


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
```



## <a name="members"></a><span data-ttu-id="2af05-107">Members</span><span class="sxs-lookup"><span data-stu-id="2af05-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2af05-108">**x**</span><span class="sxs-lookup"><span data-stu-id="2af05-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="2af05-109">x-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="2af05-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="2af05-110">**y**</span><span class="sxs-lookup"><span data-stu-id="2af05-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="2af05-111">y-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="2af05-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="2af05-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2af05-112">Remarks</span></span>

<span data-ttu-id="2af05-113">Diese Struktur wird in der ``D3DX\_DXGIFormatConvert.inl`` Kopfzeile im DirectX SDK (Juni 2010) für die Verwendung von C++ definiert.</span><span class="sxs-lookup"><span data-stu-id="2af05-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="2af05-114">Die neueste Version dieses Headers im nuget-Paket [Microsoft. dxsdk. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) definiert Sie nicht mehr und basiert stattdessen auf [DirectX:: XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) in directxmath.</span><span class="sxs-lookup"><span data-stu-id="2af05-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="2af05-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2af05-115">Requirements</span></span>



| <span data-ttu-id="2af05-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2af05-116">Requirement</span></span> | <span data-ttu-id="2af05-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2af05-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2af05-118">Header</span><span class="sxs-lookup"><span data-stu-id="2af05-118">Header</span></span><br/> | <dl> <span data-ttu-id="2af05-119"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="2af05-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2af05-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2af05-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2af05-121">Strukturen</span><span class="sxs-lookup"><span data-stu-id="2af05-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="2af05-122">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="2af05-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
