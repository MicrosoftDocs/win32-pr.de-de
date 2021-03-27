---
title: D3DX_SaturateSigned_FLOAT-Funktion
description: Ruft einen mit Vorzeichen signierten Wert aus dem angegebenen float ab.
ms.assetid: 2737ea61-5dbf-4451-bb4f-436e6ea95db6
keywords:
- D3DX_SaturateSigned_FLOAT-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_SaturateSigned_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e6ccf5cf941b1abd3577efa5899b8d827e24e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219584"
---
# <a name="d3dx_saturatesigned_float-function"></a><span data-ttu-id="b7d89-104">D3DX- \_ Funktion (sätatesigned) \_</span><span class="sxs-lookup"><span data-stu-id="b7d89-104">D3DX\_SaturateSigned\_FLOAT function</span></span>

<span data-ttu-id="b7d89-105">Ruft einen mit Vorzeichen signierten Wert aus dem angegebenen float ab.</span><span class="sxs-lookup"><span data-stu-id="b7d89-105">Retrieves a signed saturated value from the given FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d89-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7d89-106">Syntax</span></span>

``` syntax
 D3DX_SaturateSigned_FLOAT(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="b7d89-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7d89-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7d89-108">*\_Ramelow*</span><span class="sxs-lookup"><span data-stu-id="b7d89-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="b7d89-109">Der zu sätgende Wert.</span><span class="sxs-lookup"><span data-stu-id="b7d89-109">The value to saturate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7d89-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7d89-110">Return value</span></span>

<span data-ttu-id="b7d89-111">Der satte Wert mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="b7d89-111">The signed saturated value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d89-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b7d89-112">Requirements</span></span>



| <span data-ttu-id="b7d89-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7d89-113">Requirement</span></span> | <span data-ttu-id="b7d89-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b7d89-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d89-115">Header</span><span class="sxs-lookup"><span data-stu-id="b7d89-115">Header</span></span><br/> | <dl> <span data-ttu-id="b7d89-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="b7d89-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7d89-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7d89-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d89-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="b7d89-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="b7d89-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="b7d89-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





