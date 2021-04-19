---
title: XMINT4-Struktur
description: Beschreibt einen 4D-ganzzahligen Vektor.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- XMINT4-Struktur (HLSL)
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
ms.openlocfilehash: d532f3a2a2332874f7b7c22f17992c22984e3f86
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222838"
---
# <a name="xmint4-structure"></a><span data-ttu-id="3db2d-104">XMINT4-Struktur</span><span class="sxs-lookup"><span data-stu-id="3db2d-104">XMINT4 structure</span></span>

<span data-ttu-id="3db2d-105">Beschreibt einen 4D-ganzzahligen Vektor.</span><span class="sxs-lookup"><span data-stu-id="3db2d-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="3db2d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3db2d-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="3db2d-107">Members</span><span class="sxs-lookup"><span data-stu-id="3db2d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3db2d-108">**x**</span><span class="sxs-lookup"><span data-stu-id="3db2d-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="3db2d-109">x-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="3db2d-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="3db2d-110">**y**</span><span class="sxs-lookup"><span data-stu-id="3db2d-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="3db2d-111">y-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="3db2d-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="3db2d-112">**z**</span><span class="sxs-lookup"><span data-stu-id="3db2d-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="3db2d-113">z-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="3db2d-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="3db2d-114">**w**</span><span class="sxs-lookup"><span data-stu-id="3db2d-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="3db2d-115">w-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="3db2d-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3db2d-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3db2d-116">Requirements</span></span>



| <span data-ttu-id="3db2d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3db2d-117">Requirement</span></span> | <span data-ttu-id="3db2d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3db2d-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3db2d-119">Header</span><span class="sxs-lookup"><span data-stu-id="3db2d-119">Header</span></span><br/> | <dl> <span data-ttu-id="3db2d-120"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="3db2d-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="remarks"></a><span data-ttu-id="3db2d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3db2d-121">Remarks</span></span>

<span data-ttu-id="3db2d-122">Diese Struktur wird in der ``D3DX\_DXGIFormatConvert.inl`` Kopfzeile im DirectX SDK (Juni 2010) für die Verwendung von C++ definiert.</span><span class="sxs-lookup"><span data-stu-id="3db2d-122">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="3db2d-123">Die neueste Version dieses Headers im nuget-Paket [Microsoft. dxsdk. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) definiert Sie nicht mehr und basiert stattdessen auf [DirectX:: XMINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint4) in directxmath.</span><span class="sxs-lookup"><span data-stu-id="3db2d-123">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint4) in DirectXMath instead.</span></span>



## <a name="see-also"></a><span data-ttu-id="3db2d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3db2d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3db2d-125">Strukturen</span><span class="sxs-lookup"><span data-stu-id="3db2d-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="3db2d-126">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="3db2d-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
