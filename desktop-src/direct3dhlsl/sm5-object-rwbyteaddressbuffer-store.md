---
title: 'Rwbyteaddressbuffer:: Store-Funktion'
description: Legt einen Wert fest.
ms.assetid: edfda955-602c-44f4-adc3-77b61c9dcd05
keywords:
- Store-Funktion HLSL
topic_type:
- apiref
api_name:
- Store
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e161e4fb64d09e41c6529954e63b2ace55207e9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104976225"
---
# <a name="store-function"></a><span data-ttu-id="74f86-104">Store-Funktion</span><span class="sxs-lookup"><span data-stu-id="74f86-104">Store function</span></span>

<span data-ttu-id="74f86-105">Legt einen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="74f86-105">Sets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="74f86-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="74f86-106">Syntax</span></span>

``` syntax
void Store(
  in uint address,
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="74f86-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="74f86-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74f86-108">*Adresse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74f86-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74f86-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="74f86-109">Type: **uint**</span></span>

<span data-ttu-id="74f86-110">Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="74f86-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="74f86-111">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74f86-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74f86-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="74f86-112">Type: **uint**</span></span>

<span data-ttu-id="74f86-113">Ein Eingabe Wert.</span><span class="sxs-lookup"><span data-stu-id="74f86-113">One input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74f86-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74f86-114">Return value</span></span>

<span data-ttu-id="74f86-115">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="74f86-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74f86-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74f86-116">Remarks</span></span>

<span data-ttu-id="74f86-117">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="74f86-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="74f86-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="74f86-118">Vertex</span></span> | <span data-ttu-id="74f86-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="74f86-119">Hull</span></span> | <span data-ttu-id="74f86-120">Domain</span><span class="sxs-lookup"><span data-stu-id="74f86-120">Domain</span></span> | <span data-ttu-id="74f86-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="74f86-121">Geometry</span></span> | <span data-ttu-id="74f86-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="74f86-122">Pixel</span></span> | <span data-ttu-id="74f86-123">Compute</span><span class="sxs-lookup"><span data-stu-id="74f86-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="74f86-124">x</span><span class="sxs-lookup"><span data-stu-id="74f86-124">x</span></span>     | <span data-ttu-id="74f86-125">x</span><span class="sxs-lookup"><span data-stu-id="74f86-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="74f86-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="74f86-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74f86-127">Rwbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="74f86-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="74f86-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="74f86-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




