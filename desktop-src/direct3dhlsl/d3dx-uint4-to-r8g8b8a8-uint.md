---
title: D3DX_UINT4_to_R8G8B8A8_UINT-Funktion
description: Packt den angegebenen XMUINT4 zurück in ein DXGI- \_ Format \_ R8G8B8A8 \_ uint.
ms.assetid: d4770dfc-1387-40c3-a4f8-365a1421fa3c
keywords:
- D3DX_UINT4_to_R8G8B8A8_UINT-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT4_to_R8G8B8A8_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef8128d2d1989e986d8ff11e2d7e42e85f1fbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995878"
---
# <a name="d3dx_uint4_to_r8g8b8a8_uint-function"></a><span data-ttu-id="ebd5c-104">D3DX \_ UINT4 \_ to \_ R8G8B8A8 \_ uint-Funktion</span><span class="sxs-lookup"><span data-stu-id="ebd5c-104">D3DX\_UINT4\_to\_R8G8B8A8\_UINT function</span></span>

<span data-ttu-id="ebd5c-105">Packt den angegebenen XMUINT4 zurück in ein DXGI- \_ Format \_ R8G8B8A8 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="ebd5c-105">Packs the given XMUINT4 back into a DXGI\_FORMAT\_R8G8B8A8\_UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd5c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebd5c-106">Syntax</span></span>

``` syntax
UINT D3DX_UINT4_to_R8G8B8A8_UINT(
   hlsl_precise XMUINT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="ebd5c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebd5c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebd5c-108">*unpackedinput*</span><span class="sxs-lookup"><span data-stu-id="ebd5c-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="ebd5c-109">Die zu Packungs-Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="ebd5c-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebd5c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebd5c-110">Return value</span></span>

<span data-ttu-id="ebd5c-111">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="ebd5c-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd5c-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ebd5c-112">Requirements</span></span>



| <span data-ttu-id="ebd5c-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebd5c-113">Requirement</span></span> | <span data-ttu-id="ebd5c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ebd5c-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd5c-115">Header</span><span class="sxs-lookup"><span data-stu-id="ebd5c-115">Header</span></span><br/> | <dl> <span data-ttu-id="ebd5c-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="ebd5c-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebd5c-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebd5c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd5c-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="ebd5c-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="ebd5c-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="ebd5c-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





