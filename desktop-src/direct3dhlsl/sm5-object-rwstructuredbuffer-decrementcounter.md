---
title: Rwstructuredbuffer::D ecrementcounter-Funktion (httpserv. h)
description: Dekremente den ausgeblendeten Wert des Objekts.
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- Decrementcounter-Funktion HLSL
topic_type:
- apiref
api_name:
- DecrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56641054bb4e9ed4b1865d00c662b0de2afa1a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982389"
---
# <a name="decrementcounter-function"></a><span data-ttu-id="86e3c-104">Decrementcounter-Funktion</span><span class="sxs-lookup"><span data-stu-id="86e3c-104">DecrementCounter function</span></span>

<span data-ttu-id="86e3c-105">Dekremente den ausgeblendeten Wert des Objekts.</span><span class="sxs-lookup"><span data-stu-id="86e3c-105">Decrements the object's hidden counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e3c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="86e3c-106">Syntax</span></span>

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a><span data-ttu-id="86e3c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="86e3c-107">Parameters</span></span>

<span data-ttu-id="86e3c-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="86e3c-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86e3c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86e3c-109">Return value</span></span>

<span data-ttu-id="86e3c-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="86e3c-110">Type: **uint**</span></span>

<span data-ttu-id="86e3c-111">Der Wert des postdekrementierten Leistungs Zählers.</span><span class="sxs-lookup"><span data-stu-id="86e3c-111">The post-decremented counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86e3c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86e3c-112">Remarks</span></span>

<span data-ttu-id="86e3c-113">Für die gebundene Ansicht für ungeordnete Zugriffe muss ein [**D3D11 \_ buffer \_ UAV- \_ Flag \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) -Wert festgelegt sein, der während der Ausführung für diese Methode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="86e3c-113">The bound unordered access view must have [**D3D11\_BUFFER\_UAV\_FLAG\_COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) set during creationfor this method to work.</span></span>

<span data-ttu-id="86e3c-114">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="86e3c-114">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="86e3c-115">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="86e3c-115">Vertex</span></span> | <span data-ttu-id="86e3c-116">Hülle</span><span class="sxs-lookup"><span data-stu-id="86e3c-116">Hull</span></span> | <span data-ttu-id="86e3c-117">Domain</span><span class="sxs-lookup"><span data-stu-id="86e3c-117">Domain</span></span> | <span data-ttu-id="86e3c-118">Geometrie</span><span class="sxs-lookup"><span data-stu-id="86e3c-118">Geometry</span></span> | <span data-ttu-id="86e3c-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="86e3c-119">Pixel</span></span> | <span data-ttu-id="86e3c-120">Compute</span><span class="sxs-lookup"><span data-stu-id="86e3c-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="86e3c-121">x</span><span class="sxs-lookup"><span data-stu-id="86e3c-121">x</span></span>     | <span data-ttu-id="86e3c-122">x</span><span class="sxs-lookup"><span data-stu-id="86e3c-122">x</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="86e3c-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="86e3c-123">Requirements</span></span>



| <span data-ttu-id="86e3c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86e3c-124">Requirement</span></span> | <span data-ttu-id="86e3c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="86e3c-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86e3c-126">Header</span><span class="sxs-lookup"><span data-stu-id="86e3c-126">Header</span></span><br/> | <dl> <span data-ttu-id="86e3c-127"><dt>Httpserv. h</dt></span><span class="sxs-lookup"><span data-stu-id="86e3c-127"><dt>Httpserv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86e3c-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="86e3c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e3c-129">Rwstructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="86e3c-129">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="86e3c-130">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="86e3c-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

