---
title: 'Rwbyteaddressbuffer:: Store2-Funktion'
description: Legt zwei Werte fest.
ms.assetid: 7b32c84c-9ea2-47ae-a0f3-df6d95249163
keywords:
- Store2-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Store2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 574ad7fd59921767308e980e645bac966be87709
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104038232"
---
# <a name="store2-function"></a><span data-ttu-id="0abed-104">Store2-Funktion</span><span class="sxs-lookup"><span data-stu-id="0abed-104">Store2 function</span></span>

<span data-ttu-id="0abed-105">Legt zwei Werte fest.</span><span class="sxs-lookup"><span data-stu-id="0abed-105">Sets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="0abed-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0abed-106">Syntax</span></span>

``` syntax
void Store2(
  in uint address,
  in uint2 values
);
```

## <a name="parameters"></a><span data-ttu-id="0abed-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0abed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0abed-108">*Adresse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0abed-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0abed-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="0abed-109">Type: **uint**</span></span>

<span data-ttu-id="0abed-110">Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="0abed-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="0abed-111">*Werte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0abed-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0abed-112">Typ: **uint2**</span><span class="sxs-lookup"><span data-stu-id="0abed-112">Type: **uint2**</span></span>

<span data-ttu-id="0abed-113">Zwei Eingabewerte.</span><span class="sxs-lookup"><span data-stu-id="0abed-113">Two input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0abed-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0abed-114">Return value</span></span>

<span data-ttu-id="0abed-115">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0abed-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0abed-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0abed-116">Remarks</span></span>

<span data-ttu-id="0abed-117">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="0abed-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0abed-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="0abed-118">Vertex</span></span> | <span data-ttu-id="0abed-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="0abed-119">Hull</span></span> | <span data-ttu-id="0abed-120">Domain</span><span class="sxs-lookup"><span data-stu-id="0abed-120">Domain</span></span> | <span data-ttu-id="0abed-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="0abed-121">Geometry</span></span> | <span data-ttu-id="0abed-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="0abed-122">Pixel</span></span> | <span data-ttu-id="0abed-123">Compute</span><span class="sxs-lookup"><span data-stu-id="0abed-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="0abed-124">x</span><span class="sxs-lookup"><span data-stu-id="0abed-124">x</span></span>     | <span data-ttu-id="0abed-125">x</span><span class="sxs-lookup"><span data-stu-id="0abed-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0abed-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0abed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0abed-127">Rwbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="0abed-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="0abed-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="0abed-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




