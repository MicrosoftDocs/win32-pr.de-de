---
title: 'Rwstructuredbuffer:: Load (int)-Funktion'
description: 'Liest Puffer Daten. | Rwstructuredbuffer:: Load (int)-Funktion'
ms.assetid: 9CB40579-6BF8-468C-81B8-936D9940458E
keywords:
- Ladefunktion HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c20998faef8f5a018aaf95571be3c9d64730c436
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995366"
---
# <a name="rwstructuredbufferloadint-function"></a><span data-ttu-id="cf8f5-105">Rwstructuredbuffer:: Load (int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="cf8f5-105">RWStructuredBuffer::Load(int) function</span></span>

<span data-ttu-id="cf8f5-106">Liest Puffer Daten.</span><span class="sxs-lookup"><span data-stu-id="cf8f5-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf8f5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf8f5-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="cf8f5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf8f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf8f5-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf8f5-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf8f5-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="cf8f5-110">Type: **int**</span></span>

<span data-ttu-id="cf8f5-111">Der Speicherort des Puffers.</span><span class="sxs-lookup"><span data-stu-id="cf8f5-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf8f5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf8f5-112">Return value</span></span>

<span data-ttu-id="cf8f5-113">Typ:</span><span class="sxs-lookup"><span data-stu-id="cf8f5-113">Type:</span></span>

<span data-ttu-id="cf8f5-114">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**rwstructuredbuffer**](sm5-object-rwstructuredbuffer.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="cf8f5-114">The return type matches the type in the declaration for the [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf8f5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf8f5-115">Remarks</span></span>

<span data-ttu-id="cf8f5-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="cf8f5-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="cf8f5-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="cf8f5-117">Vertex</span></span> | <span data-ttu-id="cf8f5-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="cf8f5-118">Hull</span></span> | <span data-ttu-id="cf8f5-119">Domain</span><span class="sxs-lookup"><span data-stu-id="cf8f5-119">Domain</span></span> | <span data-ttu-id="cf8f5-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="cf8f5-120">Geometry</span></span> | <span data-ttu-id="cf8f5-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="cf8f5-121">Pixel</span></span> | <span data-ttu-id="cf8f5-122">Compute</span><span class="sxs-lookup"><span data-stu-id="cf8f5-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cf8f5-123">x</span><span class="sxs-lookup"><span data-stu-id="cf8f5-123">x</span></span>      | <span data-ttu-id="cf8f5-124">x</span><span class="sxs-lookup"><span data-stu-id="cf8f5-124">x</span></span>    | <span data-ttu-id="cf8f5-125">x</span><span class="sxs-lookup"><span data-stu-id="cf8f5-125">x</span></span>      | <span data-ttu-id="cf8f5-126">x</span><span class="sxs-lookup"><span data-stu-id="cf8f5-126">x</span></span>        | <span data-ttu-id="cf8f5-127">x</span><span class="sxs-lookup"><span data-stu-id="cf8f5-127">x</span></span>     | <span data-ttu-id="cf8f5-128">x</span><span class="sxs-lookup"><span data-stu-id="cf8f5-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cf8f5-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cf8f5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf8f5-130">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="cf8f5-130">Load methods</span></span>](rwstructuredbuffer-load.md)
</dt> </dl>

 

 




