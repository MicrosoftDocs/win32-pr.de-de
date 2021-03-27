---
title: D3DX_R16G16_SINT_to_INT2-Funktion
description: Entpackt DXGI- \_ Format \_ R16G16 \_ Sint-Shader-Daten in ein XMINT2-Format.
ms.assetid: 0aad1581-5fd8-43c0-828d-51ef9eb82a74
keywords:
- D3DX_R16G16_SINT_to_INT2-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_SINT_to_INT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9e14e935b49e1fa0c982551696e8d38a076a5bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996154"
---
# <a name="d3dx_r16g16_sint_to_int2-function"></a><span data-ttu-id="3120d-104">D3DX \_ R16G16 \_ Sint \_ in \_ int2-Funktion</span><span class="sxs-lookup"><span data-stu-id="3120d-104">D3DX\_R16G16\_SINT\_to\_INT2 function</span></span>

<span data-ttu-id="3120d-105">Entpackt DXGI- \_ Format \_ R16G16 \_ Sint-Shader-Daten in ein XMINT2-Format.</span><span class="sxs-lookup"><span data-stu-id="3120d-105">Unpacks DXGI\_FORMAT\_R16G16\_SINT shader data to an XMINT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="3120d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3120d-106">Syntax</span></span>

``` syntax
XMINT2 D3DX_R16G16_SINT_to_INT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="3120d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3120d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3120d-108">*packedinput*</span><span class="sxs-lookup"><span data-stu-id="3120d-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="3120d-109">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="3120d-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3120d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3120d-110">Return value</span></span>

<span data-ttu-id="3120d-111">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="3120d-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="3120d-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3120d-112">Requirements</span></span>



| <span data-ttu-id="3120d-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3120d-113">Requirement</span></span> | <span data-ttu-id="3120d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="3120d-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3120d-115">Header</span><span class="sxs-lookup"><span data-stu-id="3120d-115">Header</span></span><br/> | <dl> <span data-ttu-id="3120d-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="3120d-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3120d-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3120d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3120d-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="3120d-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="3120d-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="3120d-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





