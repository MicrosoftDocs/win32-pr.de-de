---
title: 'Rwbyteaddressbuffer:: Store4-Funktion'
description: Legt vier Werte fest.
ms.assetid: 261dd270-79a7-4566-9fbd-52bd8dc3e1bf
keywords:
- Store4-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Store4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 219cd04e4f68ad6f0d16d964e6685c558fed98b1
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104389398"
---
# <a name="store4-function"></a><span data-ttu-id="d6957-104">Store4-Funktion</span><span class="sxs-lookup"><span data-stu-id="d6957-104">Store4 function</span></span>

<span data-ttu-id="d6957-105">Legt vier Werte fest.</span><span class="sxs-lookup"><span data-stu-id="d6957-105">Sets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6957-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6957-106">Syntax</span></span>

``` syntax
void Store4(
  in uint address,
  in uint4 values
);
```

## <a name="parameters"></a><span data-ttu-id="d6957-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6957-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6957-108">*Adresse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6957-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6957-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="d6957-109">Type: **uint**</span></span>

<span data-ttu-id="d6957-110">Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="d6957-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="d6957-111">*Werte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6957-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6957-112">Typ: **uint4**</span><span class="sxs-lookup"><span data-stu-id="d6957-112">Type: **uint4**</span></span>

<span data-ttu-id="d6957-113">Vier Eingabewerte.</span><span class="sxs-lookup"><span data-stu-id="d6957-113">Four input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6957-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6957-114">Return value</span></span>

<span data-ttu-id="d6957-115">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d6957-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6957-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6957-116">Remarks</span></span>

<span data-ttu-id="d6957-117">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d6957-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d6957-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="d6957-118">Vertex</span></span> | <span data-ttu-id="d6957-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="d6957-119">Hull</span></span> | <span data-ttu-id="d6957-120">Domain</span><span class="sxs-lookup"><span data-stu-id="d6957-120">Domain</span></span> | <span data-ttu-id="d6957-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="d6957-121">Geometry</span></span> | <span data-ttu-id="d6957-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="d6957-122">Pixel</span></span> | <span data-ttu-id="d6957-123">Compute</span><span class="sxs-lookup"><span data-stu-id="d6957-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d6957-124">x</span><span class="sxs-lookup"><span data-stu-id="d6957-124">x</span></span>     | <span data-ttu-id="d6957-125">x</span><span class="sxs-lookup"><span data-stu-id="d6957-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d6957-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d6957-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6957-127">Rwbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="d6957-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="d6957-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="d6957-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




