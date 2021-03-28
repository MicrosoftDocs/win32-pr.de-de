---
title: D3DX_R16G16_UINT_to_UINT2-Funktion
description: Entpackt das DXGI- \_ Format \_ R16G16 \_ uint-Shader-Daten in eine XMUINT2.
ms.assetid: bb24fdc4-db47-4cf3-af05-4b39c3af3701
keywords:
- D3DX_R16G16_UINT_to_UINT2-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_UINT_to_UINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2586ff8876ee10368d49b816b38f5c9c8caf7c7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354046"
---
# <a name="d3dx_r16g16_uint_to_uint2-function"></a><span data-ttu-id="d8796-104">D3DX \_ R16G16 \_ uint \_ to \_ UINT2-Funktion</span><span class="sxs-lookup"><span data-stu-id="d8796-104">D3DX\_R16G16\_UINT\_to\_UINT2 function</span></span>

<span data-ttu-id="d8796-105">Entpackt das DXGI- \_ Format \_ R16G16 \_ uint-Shader-Daten in eine XMUINT2.</span><span class="sxs-lookup"><span data-stu-id="d8796-105">Unpacks DXGI\_FORMAT\_R16G16\_UINT shader data to an XMUINT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8796-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8796-106">Syntax</span></span>

``` syntax
XMUINT2 D3DX_R16G16_UINT_to_UINT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="d8796-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8796-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8796-108">*packedinput*</span><span class="sxs-lookup"><span data-stu-id="d8796-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="d8796-109">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="d8796-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8796-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8796-110">Return value</span></span>

<span data-ttu-id="d8796-111">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="d8796-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8796-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d8796-112">Requirements</span></span>



| <span data-ttu-id="d8796-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8796-113">Requirement</span></span> | <span data-ttu-id="d8796-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d8796-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8796-115">Header</span><span class="sxs-lookup"><span data-stu-id="d8796-115">Header</span></span><br/> | <dl> <span data-ttu-id="d8796-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="d8796-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8796-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8796-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8796-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="d8796-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="d8796-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="d8796-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





