---
title: D3DX_R16G16_FLOAT_to_FLOAT2-Funktion
description: Entpackt DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB-Shader-Daten in eine XMFLOAT2.
ms.assetid: 6c57dc86-d034-4b54-8572-44ac3738beb9
keywords:
- D3DX_R16G16_FLOAT_to_FLOAT2-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_FLOAT_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fb721e59a63415f98216b6e3f81a92e7598f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132393"
---
# <a name="d3dx_r16g16_float_to_float2-function"></a><span data-ttu-id="7a010-104">D3DX \_ R16G16 \_ float \_ to \_ FLOAT2-Funktion</span><span class="sxs-lookup"><span data-stu-id="7a010-104">D3DX\_R16G16\_FLOAT\_to\_FLOAT2 function</span></span>

<span data-ttu-id="7a010-105">Entpackt DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB-Shader-Daten in eine XMFLOAT2.</span><span class="sxs-lookup"><span data-stu-id="7a010-105">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB shader data to an XMFLOAT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a010-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a010-106">Syntax</span></span>

``` syntax
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="7a010-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a010-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a010-108">*packedinput*</span><span class="sxs-lookup"><span data-stu-id="7a010-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="7a010-109">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="7a010-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a010-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a010-110">Return value</span></span>

<span data-ttu-id="7a010-111">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="7a010-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a010-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7a010-112">Requirements</span></span>



| <span data-ttu-id="7a010-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a010-113">Requirement</span></span> | <span data-ttu-id="7a010-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7a010-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a010-115">Header</span><span class="sxs-lookup"><span data-stu-id="7a010-115">Header</span></span><br/> | <dl> <span data-ttu-id="7a010-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="7a010-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a010-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a010-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a010-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="7a010-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="7a010-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="7a010-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





