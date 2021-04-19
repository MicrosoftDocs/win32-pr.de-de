---
title: XMUINT4-Struktur
description: Beschreibt einen 4D-ganzzahligen Vektor ohne Vorzeichen.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- XMUINT4-Struktur (HLSL)
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
ms.openlocfilehash: 7e461d5b10f01f61de3fcfd721c4a6b1350c7d68
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222848"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="b61fa-104">XMUINT4-Struktur</span><span class="sxs-lookup"><span data-stu-id="b61fa-104">XMUINT4 structure</span></span>

<span data-ttu-id="b61fa-105">Beschreibt einen 4D-ganzzahligen Vektor ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="b61fa-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="b61fa-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b61fa-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="b61fa-107">Members</span><span class="sxs-lookup"><span data-stu-id="b61fa-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b61fa-108">**x**</span><span class="sxs-lookup"><span data-stu-id="b61fa-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="b61fa-109">x-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="b61fa-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="b61fa-110">**y**</span><span class="sxs-lookup"><span data-stu-id="b61fa-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="b61fa-111">y-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="b61fa-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="b61fa-112">**z**</span><span class="sxs-lookup"><span data-stu-id="b61fa-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="b61fa-113">z-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="b61fa-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="b61fa-114">**w**</span><span class="sxs-lookup"><span data-stu-id="b61fa-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="b61fa-115">w-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="b61fa-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a><span data-ttu-id="b61fa-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b61fa-116">Remarks</span></span>

<span data-ttu-id="b61fa-117">Diese Struktur wird in der ``D3DX\_DXGIFormatConvert.inl`` Kopfzeile im DirectX SDK (Juni 2010) für die Verwendung von C++ definiert.</span><span class="sxs-lookup"><span data-stu-id="b61fa-117">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="b61fa-118">Die neueste Version dieses Headers im nuget-Paket [Microsoft. dxsdk. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) definiert Sie nicht mehr und basiert stattdessen auf [DirectX:: XMUINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint4) in directxmath.</span><span class="sxs-lookup"><span data-stu-id="b61fa-118">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint4) in DirectXMath instead.</span></span>




## <a name="requirements"></a><span data-ttu-id="b61fa-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b61fa-119">Requirements</span></span>



| <span data-ttu-id="b61fa-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b61fa-120">Requirement</span></span> | <span data-ttu-id="b61fa-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b61fa-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b61fa-122">Header</span><span class="sxs-lookup"><span data-stu-id="b61fa-122">Header</span></span><br/> | <dl> <span data-ttu-id="b61fa-123"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="b61fa-123"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b61fa-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b61fa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b61fa-125">Strukturen</span><span class="sxs-lookup"><span data-stu-id="b61fa-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="b61fa-126">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="b61fa-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
