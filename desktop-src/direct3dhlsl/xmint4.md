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
ms.openlocfilehash: 302d820428fafb1561bd38850c4f75240ce9094f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355377"
---
# <a name="xmint4-structure"></a><span data-ttu-id="b4eee-104">XMINT4-Struktur</span><span class="sxs-lookup"><span data-stu-id="b4eee-104">XMINT4 structure</span></span>

<span data-ttu-id="b4eee-105">Beschreibt einen 4D-ganzzahligen Vektor.</span><span class="sxs-lookup"><span data-stu-id="b4eee-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4eee-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4eee-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="b4eee-107">Member</span><span class="sxs-lookup"><span data-stu-id="b4eee-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4eee-108">**x**</span><span class="sxs-lookup"><span data-stu-id="b4eee-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="b4eee-109">x-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="b4eee-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="b4eee-110">**y**</span><span class="sxs-lookup"><span data-stu-id="b4eee-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="b4eee-111">y-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="b4eee-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="b4eee-112">**z**</span><span class="sxs-lookup"><span data-stu-id="b4eee-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="b4eee-113">z-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="b4eee-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="b4eee-114">**w**</span><span class="sxs-lookup"><span data-stu-id="b4eee-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="b4eee-115">w-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="b4eee-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4eee-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b4eee-116">Requirements</span></span>



| <span data-ttu-id="b4eee-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4eee-117">Requirement</span></span> | <span data-ttu-id="b4eee-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b4eee-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4eee-119">Header</span><span class="sxs-lookup"><span data-stu-id="b4eee-119">Header</span></span><br/> | <dl> <span data-ttu-id="b4eee-120"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="b4eee-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4eee-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b4eee-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4eee-122">Strukturen</span><span class="sxs-lookup"><span data-stu-id="b4eee-122">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="b4eee-123">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="b4eee-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





