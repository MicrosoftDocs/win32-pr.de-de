---
title: 'Texture2DMSArray:: getsampleposition-Funktion'
description: 'Ruft die Position des angegebenen Beispiels ab. | Texture2DMSArray:: getsampleposition-Funktion'
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
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
ms.openlocfilehash: ea4d45ef5523c5fa4c9ef080bba6286a050aa12c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219380"
---
# <a name="texture2dmsarraygetsampleposition-function"></a><span data-ttu-id="979ec-105">Texture2DMSArray:: getsampleposition-Funktion</span><span class="sxs-lookup"><span data-stu-id="979ec-105">Texture2DMSArray::GetSamplePosition function</span></span>

<span data-ttu-id="979ec-106">Ruft die Position des angegebenen Beispiels ab.</span><span class="sxs-lookup"><span data-stu-id="979ec-106">Gets the position of the specified sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="979ec-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="979ec-107">Syntax</span></span>

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="979ec-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="979ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="979ec-109">*sampleingedex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="979ec-109">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="979ec-110">Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="979ec-110">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="979ec-111">Der null basierte Index eines Beispiel Speicher Orts.</span><span class="sxs-lookup"><span data-stu-id="979ec-111">The zero-based index of a sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="979ec-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="979ec-112">Return value</span></span>

<span data-ttu-id="979ec-113">Typ: **float2**</span><span class="sxs-lookup"><span data-stu-id="979ec-113">Type: **float2**</span></span>

<span data-ttu-id="979ec-114">Ein Beispiel Speicherort.</span><span class="sxs-lookup"><span data-stu-id="979ec-114">A sample location.</span></span>

## <a name="remarks"></a><span data-ttu-id="979ec-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="979ec-115">Remarks</span></span>

<span data-ttu-id="979ec-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="979ec-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="979ec-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="979ec-117">Vertex</span></span> | <span data-ttu-id="979ec-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="979ec-118">Hull</span></span> | <span data-ttu-id="979ec-119">Domain</span><span class="sxs-lookup"><span data-stu-id="979ec-119">Domain</span></span> | <span data-ttu-id="979ec-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="979ec-120">Geometry</span></span> | <span data-ttu-id="979ec-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="979ec-121">Pixel</span></span> | <span data-ttu-id="979ec-122">Compute</span><span class="sxs-lookup"><span data-stu-id="979ec-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="979ec-123">x</span><span class="sxs-lookup"><span data-stu-id="979ec-123">x</span></span>      | <span data-ttu-id="979ec-124">x</span><span class="sxs-lookup"><span data-stu-id="979ec-124">x</span></span>    | <span data-ttu-id="979ec-125">x</span><span class="sxs-lookup"><span data-stu-id="979ec-125">x</span></span>      | <span data-ttu-id="979ec-126">x</span><span class="sxs-lookup"><span data-stu-id="979ec-126">x</span></span>        | <span data-ttu-id="979ec-127">x</span><span class="sxs-lookup"><span data-stu-id="979ec-127">x</span></span>     | <span data-ttu-id="979ec-128">x</span><span class="sxs-lookup"><span data-stu-id="979ec-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="979ec-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="979ec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="979ec-130">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="979ec-130">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="979ec-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="979ec-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
