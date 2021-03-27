---
title: Checkaccessfullymapping-Funktion
description: Bestimmt, ob alle Werte aus einem Sample-, Gather-oder LOAD-Vorgang auf zugeordnete Kacheln in einer gekachelten Ressource zugreifen.
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- Checkaccessfullymapping-Funktion HLSL
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7310e0ebac496fc8f5a56ba3843b7496b8ce7c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729369"
---
# <a name="checkaccessfullymapped-function"></a><span data-ttu-id="ecd36-104">Checkaccessfullymapping-Funktion</span><span class="sxs-lookup"><span data-stu-id="ecd36-104">CheckAccessFullyMapped function</span></span>

<span data-ttu-id="ecd36-105">Bestimmt, ob alle Werte aus einem **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ecd36-105">Determines whether all values from a **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span>

## <a name="syntax"></a><span data-ttu-id="ecd36-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecd36-106">Syntax</span></span>

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a><span data-ttu-id="ecd36-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecd36-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecd36-108">*Status* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecd36-108">*status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecd36-109">Typ: **\_ nur uint**</span><span class="sxs-lookup"><span data-stu-id="ecd36-109">Type: **uint\_only**</span></span>

<span data-ttu-id="ecd36-110">Der Statuswert, der von einem **Sample**-, **Gather**-oder **Load** -Vorgang zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ecd36-110">The status value that is returned from a **Sample**, **Gather**, or **Load** operation.</span></span> <span data-ttu-id="ecd36-111">Da Sie nicht direkt auf diesen Statuswert zugreifen können, müssen Sie ihn an **checkaccessfullymapping** übergeben.</span><span class="sxs-lookup"><span data-stu-id="ecd36-111">Because you can't access this status value directly, you need to pass it to **CheckAccessFullyMapped**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecd36-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ecd36-112">Return value</span></span>

<span data-ttu-id="ecd36-113">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="ecd36-113">Type: **bool**</span></span>

<span data-ttu-id="ecd36-114">Gibt einen **booleschen** Wert zurück, der angibt, ob alle Werte aus einem **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ecd36-114">Returns a **Boolean** value that indicates whether all values from a **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ecd36-115">Gibt **true** zurück, wenn alle Werte aus dem Vorgang auf zugeordnete Kacheln zugegriffen haben. Andernfalls wird **false** zurückgegeben, wenn Werte von einer nicht zugeordneten Kachel entnommen wurden.</span><span class="sxs-lookup"><span data-stu-id="ecd36-115">Returns **TRUE** if all values from the operation accessed mapped tiles; otherwise, returns **FALSE** if any values were taken from an unmapped tile.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecd36-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ecd36-116">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="ecd36-117">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="ecd36-117">Minimum Shader Model</span></span>

<span data-ttu-id="ecd36-118">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ecd36-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ecd36-119">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="ecd36-119">Shader Model</span></span>                                                                | <span data-ttu-id="ecd36-120">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ecd36-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ecd36-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="ecd36-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="ecd36-122">ja</span><span class="sxs-lookup"><span data-stu-id="ecd36-122">yes</span></span>       |



 

<span data-ttu-id="ecd36-123">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ecd36-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="ecd36-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="ecd36-124">Vertex</span></span> | <span data-ttu-id="ecd36-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="ecd36-125">Hull</span></span> | <span data-ttu-id="ecd36-126">Domain</span><span class="sxs-lookup"><span data-stu-id="ecd36-126">Domain</span></span> | <span data-ttu-id="ecd36-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="ecd36-127">Geometry</span></span> | <span data-ttu-id="ecd36-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="ecd36-128">Pixel</span></span> | <span data-ttu-id="ecd36-129">Compute</span><span class="sxs-lookup"><span data-stu-id="ecd36-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ecd36-130">x</span><span class="sxs-lookup"><span data-stu-id="ecd36-130">x</span></span>     | <span data-ttu-id="ecd36-131">x</span><span class="sxs-lookup"><span data-stu-id="ecd36-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ecd36-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ecd36-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecd36-133">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ecd36-133">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 