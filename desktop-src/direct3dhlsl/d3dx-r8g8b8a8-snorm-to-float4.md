---
title: D3DX_R8G8B8A8_SNORM_to_FLOAT4-Funktion
description: Entpackt das DXGI- \_ Format \_ R8G8B8A8 \_ snorm-Shader-Daten in ein XMFLOAT4-Format.
ms.assetid: 2f2b9d5e-f4d0-470a-a4bb-b333d57f03e7
keywords:
- D3DX_R8G8B8A8_SNORM_to_FLOAT4-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_SNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a4153fa30f2792008ccc45bc3e16f5d404f33a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982216"
---
# <a name="d3dx_r8g8b8a8_snorm_to_float4-function"></a><span data-ttu-id="c1425-104">D3DX \_ R8G8B8A8 \_ snorm \_ zu \_ float4-Funktion</span><span class="sxs-lookup"><span data-stu-id="c1425-104">D3DX\_R8G8B8A8\_SNORM\_to\_FLOAT4 function</span></span>

<span data-ttu-id="c1425-105">Entpackt das DXGI- \_ Format \_ R8G8B8A8 \_ snorm-Shader-Daten in ein XMFLOAT4-Format.</span><span class="sxs-lookup"><span data-stu-id="c1425-105">Unpacks DXGI\_FORMAT\_R8G8B8A8\_SNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1425-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1425-106">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="c1425-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1425-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1425-108">*packedinput*</span><span class="sxs-lookup"><span data-stu-id="c1425-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="c1425-109">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="c1425-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1425-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1425-110">Return value</span></span>

<span data-ttu-id="c1425-111">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="c1425-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1425-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c1425-112">Requirements</span></span>



| <span data-ttu-id="c1425-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1425-113">Requirement</span></span> | <span data-ttu-id="c1425-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c1425-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1425-115">Header</span><span class="sxs-lookup"><span data-stu-id="c1425-115">Header</span></span><br/> | <dl> <span data-ttu-id="c1425-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="c1425-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1425-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1425-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1425-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="c1425-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="c1425-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="c1425-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





