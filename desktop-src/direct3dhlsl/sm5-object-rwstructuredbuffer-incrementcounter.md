---
title: 'Rwstructuredbuffer:: incrementcounter-Funktion (httpserv. h)'
description: Erhöht den ausgeblendeten Wert des Objekts.
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- Incrementcounter-Funktion HLSL
topic_type:
- apiref
api_name:
- IncrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0002f82873de1c56ce5a7d79c9adb13bdf7ebc0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355496"
---
# <a name="incrementcounter-function"></a><span data-ttu-id="4f34a-104">Incrementcounter-Funktion</span><span class="sxs-lookup"><span data-stu-id="4f34a-104">IncrementCounter function</span></span>

<span data-ttu-id="4f34a-105">Erhöht den ausgeblendeten Wert des Objekts.</span><span class="sxs-lookup"><span data-stu-id="4f34a-105">Increments the object's hidden counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f34a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f34a-106">Syntax</span></span>

``` syntax
uint IncrementCounter(void);
```

## <a name="parameters"></a><span data-ttu-id="4f34a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f34a-107">Parameters</span></span>

<span data-ttu-id="4f34a-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4f34a-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f34a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f34a-109">Return value</span></span>

<span data-ttu-id="4f34a-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="4f34a-110">Type: **uint**</span></span>

<span data-ttu-id="4f34a-111">Der Wert des vorab inkrementierten Zählers.</span><span class="sxs-lookup"><span data-stu-id="4f34a-111">The pre-incremented counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f34a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f34a-112">Remarks</span></span>

<span data-ttu-id="4f34a-113">Für die gebundene Ansicht für ungeordnete Zugriffe muss bei der Erstellung der [**D3D11 \_ buffer \_ UAV- \_ Flag \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) -Wert festgelegt sein, damit diese Methode funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4f34a-113">The bound unordered access view must have [**D3D11\_BUFFER\_UAV\_FLAG\_COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) set during creation for this method to work.</span></span>

<span data-ttu-id="4f34a-114">Eine strukturierte Ressource kann basierend auf den Komponentennamen der Strukturen weiter indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="4f34a-114">A structured resource can be further indexed based on the component names of the structures.</span></span>

<span data-ttu-id="4f34a-115">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4f34a-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4f34a-116">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="4f34a-116">Vertex</span></span> | <span data-ttu-id="4f34a-117">Hülle</span><span class="sxs-lookup"><span data-stu-id="4f34a-117">Hull</span></span> | <span data-ttu-id="4f34a-118">Domain</span><span class="sxs-lookup"><span data-stu-id="4f34a-118">Domain</span></span> | <span data-ttu-id="4f34a-119">Geometrie</span><span class="sxs-lookup"><span data-stu-id="4f34a-119">Geometry</span></span> | <span data-ttu-id="4f34a-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="4f34a-120">Pixel</span></span> | <span data-ttu-id="4f34a-121">Compute</span><span class="sxs-lookup"><span data-stu-id="4f34a-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4f34a-122">x</span><span class="sxs-lookup"><span data-stu-id="4f34a-122">x</span></span>     | <span data-ttu-id="4f34a-123">x</span><span class="sxs-lookup"><span data-stu-id="4f34a-123">x</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="4f34a-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4f34a-124">Requirements</span></span>



| <span data-ttu-id="4f34a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f34a-125">Requirement</span></span> | <span data-ttu-id="4f34a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="4f34a-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f34a-127">Header</span><span class="sxs-lookup"><span data-stu-id="4f34a-127">Header</span></span><br/> | <dl> <span data-ttu-id="4f34a-128"><dt>Httpserv. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f34a-128"><dt>Httpserv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f34a-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4f34a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f34a-130">Rwstructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="4f34a-130">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="4f34a-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="4f34a-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

