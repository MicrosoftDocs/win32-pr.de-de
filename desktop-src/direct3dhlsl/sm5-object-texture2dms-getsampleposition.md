---
title: 'Texture2DMS:: getsampleposition-Funktion'
description: Gibt die Beispiel Position für den bereitgestellten Beispiel Index zurück.
ms.assetid: b7821112-9b40-4302-b5c1-03bab531a0ab
keywords:
- Getsampleposition-Funktion HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 532411e333023ff61df0b7f9fbf0336dc11d1586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517324"
---
# <a name="texture2dmsgetsampleposition-function"></a><span data-ttu-id="4a35c-104">Texture2DMS:: getsampleposition-Funktion</span><span class="sxs-lookup"><span data-stu-id="4a35c-104">Texture2DMS::GetSamplePosition function</span></span>

<span data-ttu-id="4a35c-105">Gibt die Beispiel Position für den bereitgestellten Beispiel Index zurück.</span><span class="sxs-lookup"><span data-stu-id="4a35c-105">Returns the sample position for the sample index provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a35c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a35c-106">Syntax</span></span>

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="4a35c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a35c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a35c-108">*sampleingedex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a35c-108">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a35c-109">Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4a35c-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4a35c-110">Der null basierte Index eines Beispiel Speicher Orts.</span><span class="sxs-lookup"><span data-stu-id="4a35c-110">The zero-based index of a sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a35c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a35c-111">Return value</span></span>

<span data-ttu-id="4a35c-112">Typ: **float2**</span><span class="sxs-lookup"><span data-stu-id="4a35c-112">Type: **float2**</span></span>

<span data-ttu-id="4a35c-113">Ein Beispiel Speicherort.</span><span class="sxs-lookup"><span data-stu-id="4a35c-113">A sample location.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a35c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a35c-114">Remarks</span></span>

<span data-ttu-id="4a35c-115">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4a35c-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4a35c-116">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="4a35c-116">Vertex</span></span> | <span data-ttu-id="4a35c-117">Hülle</span><span class="sxs-lookup"><span data-stu-id="4a35c-117">Hull</span></span> | <span data-ttu-id="4a35c-118">Domain</span><span class="sxs-lookup"><span data-stu-id="4a35c-118">Domain</span></span> | <span data-ttu-id="4a35c-119">Geometrie</span><span class="sxs-lookup"><span data-stu-id="4a35c-119">Geometry</span></span> | <span data-ttu-id="4a35c-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="4a35c-120">Pixel</span></span> | <span data-ttu-id="4a35c-121">Compute</span><span class="sxs-lookup"><span data-stu-id="4a35c-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4a35c-122">x</span><span class="sxs-lookup"><span data-stu-id="4a35c-122">x</span></span>      | <span data-ttu-id="4a35c-123">x</span><span class="sxs-lookup"><span data-stu-id="4a35c-123">x</span></span>    | <span data-ttu-id="4a35c-124">x</span><span class="sxs-lookup"><span data-stu-id="4a35c-124">x</span></span>      | <span data-ttu-id="4a35c-125">x</span><span class="sxs-lookup"><span data-stu-id="4a35c-125">x</span></span>        | <span data-ttu-id="4a35c-126">x</span><span class="sxs-lookup"><span data-stu-id="4a35c-126">x</span></span>     | <span data-ttu-id="4a35c-127">x</span><span class="sxs-lookup"><span data-stu-id="4a35c-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4a35c-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4a35c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a35c-129">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="4a35c-129">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="4a35c-130">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="4a35c-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
