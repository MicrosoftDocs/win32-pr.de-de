---
title: D3DX_R8G8B8A8_SINT_to_INT4-Funktion
description: Entpackt DXGI- \_ Format \_ R8G8B8A8 \_ Sint-Shader-Daten in ein XMINT4-Format.
ms.assetid: 144bd296-02b5-4307-b785-860680db2d52
keywords:
- D3DX_R8G8B8A8_SINT_to_INT4-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_SINT_to_INT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129982db5535d91b38dc9d3630f78192c4b1fbc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132361"
---
# <a name="d3dx_r8g8b8a8_sint_to_int4-function"></a><span data-ttu-id="299c1-104">D3DX \_ R8G8B8A8 \_ Sint \_ in \_ INT4-Funktion</span><span class="sxs-lookup"><span data-stu-id="299c1-104">D3DX\_R8G8B8A8\_SINT\_to\_INT4 function</span></span>

<span data-ttu-id="299c1-105">Entpackt DXGI- \_ Format \_ R8G8B8A8 \_ Sint-Shader-Daten in ein XMINT4-Format.</span><span class="sxs-lookup"><span data-stu-id="299c1-105">Unpacks DXGI\_FORMAT\_R8G8B8A8\_SINT shader data to an XMINT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="299c1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="299c1-106">Syntax</span></span>

``` syntax
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="299c1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="299c1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="299c1-108">*packedinput*</span><span class="sxs-lookup"><span data-stu-id="299c1-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="299c1-109">Die gepackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="299c1-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="299c1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="299c1-110">Return value</span></span>

<span data-ttu-id="299c1-111">Die entpackten Shader-Daten.</span><span class="sxs-lookup"><span data-stu-id="299c1-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="299c1-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="299c1-112">Requirements</span></span>



| <span data-ttu-id="299c1-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="299c1-113">Requirement</span></span> | <span data-ttu-id="299c1-114">Wert</span><span class="sxs-lookup"><span data-stu-id="299c1-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="299c1-115">Header</span><span class="sxs-lookup"><span data-stu-id="299c1-115">Header</span></span><br/> | <dl> <span data-ttu-id="299c1-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="299c1-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="299c1-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="299c1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="299c1-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="299c1-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="299c1-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="299c1-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





