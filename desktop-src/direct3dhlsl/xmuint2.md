---
title: XMUINT2-Struktur
description: Beschreibt einen 2D-ganzzahligen Vektor ohne Vorzeichen.
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- XMUINT2-Struktur (HLSL)
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
ms.openlocfilehash: 73d14bd43ec3b75a2bf503b7d742b6c69881475b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982095"
---
# <a name="xmuint2-structure"></a><span data-ttu-id="c1335-104">XMUINT2-Struktur</span><span class="sxs-lookup"><span data-stu-id="c1335-104">XMUINT2 structure</span></span>

<span data-ttu-id="c1335-105">Beschreibt einen 2D-ganzzahligen Vektor ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c1335-105">Describes an 2D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1335-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1335-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
```



## <a name="members"></a><span data-ttu-id="c1335-107">Member</span><span class="sxs-lookup"><span data-stu-id="c1335-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1335-108">**x**</span><span class="sxs-lookup"><span data-stu-id="c1335-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="c1335-109">x-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="c1335-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="c1335-110">**y**</span><span class="sxs-lookup"><span data-stu-id="c1335-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="c1335-111">y-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="c1335-111">y-component of the vector.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1335-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c1335-112">Requirements</span></span>



| <span data-ttu-id="c1335-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1335-113">Requirement</span></span> | <span data-ttu-id="c1335-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c1335-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1335-115">Header</span><span class="sxs-lookup"><span data-stu-id="c1335-115">Header</span></span><br/> | <dl> <span data-ttu-id="c1335-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="c1335-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1335-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c1335-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1335-118">Strukturen</span><span class="sxs-lookup"><span data-stu-id="c1335-118">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="c1335-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="c1335-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





