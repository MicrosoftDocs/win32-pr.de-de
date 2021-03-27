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
ms.openlocfilehash: 9f0b02ffe64e7b4c4479723b4e36abd87f6bd03b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982096"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="feef2-104">XMUINT4-Struktur</span><span class="sxs-lookup"><span data-stu-id="feef2-104">XMUINT4 structure</span></span>

<span data-ttu-id="feef2-105">Beschreibt einen 4D-ganzzahligen Vektor ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="feef2-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="feef2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="feef2-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="feef2-107">Member</span><span class="sxs-lookup"><span data-stu-id="feef2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="feef2-108">**x**</span><span class="sxs-lookup"><span data-stu-id="feef2-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="feef2-109">x-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="feef2-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="feef2-110">**y**</span><span class="sxs-lookup"><span data-stu-id="feef2-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="feef2-111">y-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="feef2-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="feef2-112">**z**</span><span class="sxs-lookup"><span data-stu-id="feef2-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="feef2-113">z-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="feef2-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="feef2-114">**w**</span><span class="sxs-lookup"><span data-stu-id="feef2-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="feef2-115">w-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="feef2-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="feef2-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="feef2-116">Requirements</span></span>



| <span data-ttu-id="feef2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="feef2-117">Requirement</span></span> | <span data-ttu-id="feef2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="feef2-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feef2-119">Header</span><span class="sxs-lookup"><span data-stu-id="feef2-119">Header</span></span><br/> | <dl> <span data-ttu-id="feef2-120"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="feef2-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feef2-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="feef2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feef2-122">Strukturen</span><span class="sxs-lookup"><span data-stu-id="feef2-122">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="feef2-123">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="feef2-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





