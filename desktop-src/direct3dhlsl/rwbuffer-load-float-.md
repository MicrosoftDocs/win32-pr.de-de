---
title: 'Rwbuffer:: Load (int)-Funktion'
description: 'Liest Puffer Daten. | Rwbuffer:: Load (int)-Funktion'
ms.assetid: 3066E244-DE56-4F0D-8443-018B9EFEC1FF
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
ms.openlocfilehash: 561f055990bbca683bf9c55b5805b8d3c55b3272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761691"
---
# <a name="rwbufferloadint-function"></a><span data-ttu-id="5b78c-105">Rwbuffer:: Load (int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="5b78c-105">RWBuffer::Load(int) function</span></span>

<span data-ttu-id="5b78c-106">Liest Puffer Daten.</span><span class="sxs-lookup"><span data-stu-id="5b78c-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b78c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b78c-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="5b78c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b78c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b78c-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b78c-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b78c-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="5b78c-110">Type: **int**</span></span>

<span data-ttu-id="5b78c-111">Der Speicherort des Puffers.</span><span class="sxs-lookup"><span data-stu-id="5b78c-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b78c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b78c-112">Return value</span></span>

<span data-ttu-id="5b78c-113">Typ:</span><span class="sxs-lookup"><span data-stu-id="5b78c-113">Type:</span></span>

<span data-ttu-id="5b78c-114">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**rwbuffer**](sm5-object-rwbuffer.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5b78c-114">The return type matches the type in the declaration for the [**RWBuffer**](sm5-object-rwbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b78c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b78c-115">Remarks</span></span>

<span data-ttu-id="5b78c-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5b78c-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5b78c-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="5b78c-117">Vertex</span></span> | <span data-ttu-id="5b78c-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="5b78c-118">Hull</span></span> | <span data-ttu-id="5b78c-119">Domain</span><span class="sxs-lookup"><span data-stu-id="5b78c-119">Domain</span></span> | <span data-ttu-id="5b78c-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="5b78c-120">Geometry</span></span> | <span data-ttu-id="5b78c-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="5b78c-121">Pixel</span></span> | <span data-ttu-id="5b78c-122">Compute</span><span class="sxs-lookup"><span data-stu-id="5b78c-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5b78c-123">x</span><span class="sxs-lookup"><span data-stu-id="5b78c-123">x</span></span>      | <span data-ttu-id="5b78c-124">x</span><span class="sxs-lookup"><span data-stu-id="5b78c-124">x</span></span>    | <span data-ttu-id="5b78c-125">x</span><span class="sxs-lookup"><span data-stu-id="5b78c-125">x</span></span>      | <span data-ttu-id="5b78c-126">x</span><span class="sxs-lookup"><span data-stu-id="5b78c-126">x</span></span>        | <span data-ttu-id="5b78c-127">x</span><span class="sxs-lookup"><span data-stu-id="5b78c-127">x</span></span>     | <span data-ttu-id="5b78c-128">x</span><span class="sxs-lookup"><span data-stu-id="5b78c-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5b78c-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5b78c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b78c-130">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="5b78c-130">Load methods</span></span>](rwbuffer-load.md)
</dt> </dl>

 

 




