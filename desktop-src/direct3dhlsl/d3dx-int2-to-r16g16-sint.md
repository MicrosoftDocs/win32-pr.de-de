---
title: D3DX_INT2_to_R16G16_SINT-Funktion
description: Packt den angegebenen XMINT2 zurück in ein DXGI- \_ Format \_ R16G16 \_ Sint.
ms.assetid: dc37e8a3-31d4-4af6-9bc3-9aa5062c066a
keywords:
- D3DX_INT2_to_R16G16_SINT-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_INT2_to_R16G16_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97d60ba29b2451dea973b4ec0453f3a4df2ecdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982532"
---
# <a name="d3dx_int2_to_r16g16_sint-function"></a><span data-ttu-id="1a157-104">D3DX \_ int2 \_ to \_ R16G16 \_ Sint-Funktion</span><span class="sxs-lookup"><span data-stu-id="1a157-104">D3DX\_INT2\_to\_R16G16\_SINT function</span></span>

<span data-ttu-id="1a157-105">Packt den angegebenen XMINT2 zurück in ein DXGI- \_ Format \_ R16G16 \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="1a157-105">Packs the given XMINT2 back into a DXGI\_FORMAT\_R16G16\_SINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a157-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a157-106">Syntax</span></span>

``` syntax
UINT D3DX_INT2_to_R16G16_SINT(
   hlsl_precise XMINT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="1a157-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a157-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a157-108">*unpackedinput*</span><span class="sxs-lookup"><span data-stu-id="1a157-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="1a157-109">Die zu Packungs-Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="1a157-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a157-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a157-110">Return value</span></span>

<span data-ttu-id="1a157-111">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="1a157-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a157-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1a157-112">Requirements</span></span>



| <span data-ttu-id="1a157-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a157-113">Requirement</span></span> | <span data-ttu-id="1a157-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1a157-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a157-115">Header</span><span class="sxs-lookup"><span data-stu-id="1a157-115">Header</span></span><br/> | <dl> <span data-ttu-id="1a157-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="1a157-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a157-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a157-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a157-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="1a157-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="1a157-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="1a157-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





