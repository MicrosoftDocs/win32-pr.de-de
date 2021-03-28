---
title: 'Rwbyteaddressbuffer:: Store3-Funktion'
description: Legt drei Werte fest.
ms.assetid: eaf12b5a-c9c6-413a-9646-3d14e7825460
keywords:
- Store3-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Store3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd27684c3adf506e086fb17f789272c6b263ab20
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313344"
---
# <a name="store3-function"></a><span data-ttu-id="46e2d-104">Store3-Funktion</span><span class="sxs-lookup"><span data-stu-id="46e2d-104">Store3 function</span></span>

<span data-ttu-id="46e2d-105">Legt drei Werte fest.</span><span class="sxs-lookup"><span data-stu-id="46e2d-105">Sets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="46e2d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="46e2d-106">Syntax</span></span>

``` syntax
void Store3(
  in uint address,
  in uint3 values
);
```

## <a name="parameters"></a><span data-ttu-id="46e2d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="46e2d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46e2d-108">*Adresse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46e2d-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e2d-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="46e2d-109">Type: **uint**</span></span>

<span data-ttu-id="46e2d-110">Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="46e2d-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="46e2d-111">*Werte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46e2d-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e2d-112">Typ: **uint3**</span><span class="sxs-lookup"><span data-stu-id="46e2d-112">Type: **uint3**</span></span>

<span data-ttu-id="46e2d-113">Drei Eingabewerte.</span><span class="sxs-lookup"><span data-stu-id="46e2d-113">Three input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46e2d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46e2d-114">Return value</span></span>

<span data-ttu-id="46e2d-115">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="46e2d-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46e2d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46e2d-116">Remarks</span></span>

<span data-ttu-id="46e2d-117">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="46e2d-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="46e2d-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="46e2d-118">Vertex</span></span> | <span data-ttu-id="46e2d-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="46e2d-119">Hull</span></span> | <span data-ttu-id="46e2d-120">Domain</span><span class="sxs-lookup"><span data-stu-id="46e2d-120">Domain</span></span> | <span data-ttu-id="46e2d-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="46e2d-121">Geometry</span></span> | <span data-ttu-id="46e2d-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="46e2d-122">Pixel</span></span> | <span data-ttu-id="46e2d-123">Compute</span><span class="sxs-lookup"><span data-stu-id="46e2d-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="46e2d-124">x</span><span class="sxs-lookup"><span data-stu-id="46e2d-124">x</span></span>     | <span data-ttu-id="46e2d-125">x</span><span class="sxs-lookup"><span data-stu-id="46e2d-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="46e2d-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="46e2d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e2d-127">Rwbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="46e2d-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="46e2d-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="46e2d-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




