---
title: D3DX_Saturate_FLOAT-Funktion
description: Ruft den gesättigten Wert des angegebenen Float-Werts ab.
ms.assetid: 659df450-3535-44eb-b867-89529369f903
keywords:
- D3DX_Saturate_FLOAT-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_Saturate_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3deabf5140d4f3f3bdfc2d6cce52f32385987ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870143"
---
# <a name="d3dx_saturate_float-function"></a><span data-ttu-id="70eff-104">D3DX-Funktion für Gleit Komma Zahl \_ \_</span><span class="sxs-lookup"><span data-stu-id="70eff-104">D3DX\_Saturate\_FLOAT function</span></span>

<span data-ttu-id="70eff-105">Ruft den gesättigten Wert des angegebenen Float-Werts ab.</span><span class="sxs-lookup"><span data-stu-id="70eff-105">Retrieves the saturated value of the given FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="70eff-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="70eff-106">Syntax</span></span>

``` syntax
FLOAT D3DX_Saturate_FLOAT(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="70eff-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="70eff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70eff-108">*\_Ramelow*</span><span class="sxs-lookup"><span data-stu-id="70eff-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="70eff-109">Der zu sätgende Wert.</span><span class="sxs-lookup"><span data-stu-id="70eff-109">The value to saturate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70eff-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70eff-110">Return value</span></span>

<span data-ttu-id="70eff-111">Der satte Wert.</span><span class="sxs-lookup"><span data-stu-id="70eff-111">The saturated value.</span></span>

## <a name="requirements"></a><span data-ttu-id="70eff-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="70eff-112">Requirements</span></span>



| <span data-ttu-id="70eff-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70eff-113">Requirement</span></span> | <span data-ttu-id="70eff-114">Wert</span><span class="sxs-lookup"><span data-stu-id="70eff-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70eff-115">Header</span><span class="sxs-lookup"><span data-stu-id="70eff-115">Header</span></span><br/> | <dl> <span data-ttu-id="70eff-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="70eff-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70eff-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70eff-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70eff-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="70eff-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="70eff-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="70eff-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





