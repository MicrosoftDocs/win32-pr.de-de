---
title: 'Consumestructuredbuffer:: consumerfunktion'
description: Entfernt einen Wert vom Ende des Puffers.
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- Funktions-HLSL
topic_type:
- apiref
api_name:
- Consume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d5a43c53089a7e7b19d0f1ecef5c0e5608e8ee9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104038235"
---
# <a name="consume-function"></a><span data-ttu-id="6ad4d-104">Funktion verarbeiten</span><span class="sxs-lookup"><span data-stu-id="6ad4d-104">Consume function</span></span>

<span data-ttu-id="6ad4d-105">Entfernt einen Wert vom Ende des Puffers.</span><span class="sxs-lookup"><span data-stu-id="6ad4d-105">Removes a value from the end of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ad4d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ad4d-106">Syntax</span></span>

``` syntax
T Consume(void);
```

## <a name="parameters"></a><span data-ttu-id="6ad4d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ad4d-107">Parameters</span></span>

<span data-ttu-id="6ad4d-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6ad4d-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ad4d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ad4d-109">Return value</span></span>

<span data-ttu-id="6ad4d-110">Typ: **T**</span><span class="sxs-lookup"><span data-stu-id="6ad4d-110">Type: **T**</span></span>

<span data-ttu-id="6ad4d-111">Der entfernte Wert (kann eine Struktur sein).</span><span class="sxs-lookup"><span data-stu-id="6ad4d-111">The value removed (can be a structure).</span></span>

## <a name="remarks"></a><span data-ttu-id="6ad4d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ad4d-112">Remarks</span></span>

<span data-ttu-id="6ad4d-113">"T" kann ein beliebiger Datentyp sein, einschließlich einer Struktur.</span><span class="sxs-lookup"><span data-stu-id="6ad4d-113">T can be any data type including a structure.</span></span>

<span data-ttu-id="6ad4d-114">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6ad4d-114">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6ad4d-115">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="6ad4d-115">Vertex</span></span> | <span data-ttu-id="6ad4d-116">Hülle</span><span class="sxs-lookup"><span data-stu-id="6ad4d-116">Hull</span></span> | <span data-ttu-id="6ad4d-117">Domain</span><span class="sxs-lookup"><span data-stu-id="6ad4d-117">Domain</span></span> | <span data-ttu-id="6ad4d-118">Geometrie</span><span class="sxs-lookup"><span data-stu-id="6ad4d-118">Geometry</span></span> | <span data-ttu-id="6ad4d-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="6ad4d-119">Pixel</span></span> | <span data-ttu-id="6ad4d-120">Compute</span><span class="sxs-lookup"><span data-stu-id="6ad4d-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6ad4d-121">x</span><span class="sxs-lookup"><span data-stu-id="6ad4d-121">x</span></span>      | <span data-ttu-id="6ad4d-122">x</span><span class="sxs-lookup"><span data-stu-id="6ad4d-122">x</span></span>    | <span data-ttu-id="6ad4d-123">x</span><span class="sxs-lookup"><span data-stu-id="6ad4d-123">x</span></span>      | <span data-ttu-id="6ad4d-124">x</span><span class="sxs-lookup"><span data-stu-id="6ad4d-124">x</span></span>        | <span data-ttu-id="6ad4d-125">x</span><span class="sxs-lookup"><span data-stu-id="6ad4d-125">x</span></span>     | <span data-ttu-id="6ad4d-126">x</span><span class="sxs-lookup"><span data-stu-id="6ad4d-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6ad4d-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6ad4d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ad4d-128">Consumestructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="6ad4d-128">ConsumeStructuredBuffer</span></span>](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="6ad4d-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="6ad4d-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




