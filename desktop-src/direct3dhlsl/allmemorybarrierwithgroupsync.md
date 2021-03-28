---
title: Allmemorybarrierwithgroupsync-Funktion
description: Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Speicherzugriffe abgeschlossen sind und alle Threads in der Gruppe diesen-Befehl erreicht haben.
ms.assetid: 831830e7-19ce-41d0-b555-44a083b67cdc
keywords:
- Allmemorybarrierwithgroupsync-Funktion HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1fc005545485b7f894729ab6c7d7975acfd5b6d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038142"
---
# <a name="allmemorybarrierwithgroupsync-function"></a><span data-ttu-id="2228b-104">Allmemorybarrierwithgroupsync-Funktion</span><span class="sxs-lookup"><span data-stu-id="2228b-104">AllMemoryBarrierWithGroupSync function</span></span>

<span data-ttu-id="2228b-105">Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Speicherzugriffe abgeschlossen sind und alle Threads in der Gruppe diesen-Befehl erreicht haben.</span><span class="sxs-lookup"><span data-stu-id="2228b-105">Blocks execution of all threads in a group until all memory accesses have been completed and all threads in the group have reached this call.</span></span>

## <a name="syntax"></a><span data-ttu-id="2228b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2228b-106">Syntax</span></span>

``` syntax
void AllMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a><span data-ttu-id="2228b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2228b-107">Parameters</span></span>

<span data-ttu-id="2228b-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2228b-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2228b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2228b-109">Return value</span></span>

<span data-ttu-id="2228b-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2228b-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2228b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2228b-111">Remarks</span></span>

<span data-ttu-id="2228b-112">Eine Arbeitsspeicher Barriere gewährleistet, dass ausstehende Speichervorgänge abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="2228b-112">A memory barrier guarantees that outstanding memory operations have completed.</span></span> <span data-ttu-id="2228b-113">Threads werden bei groupsync-Barrieren synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="2228b-113">Threads are synchronized at GroupSync barriers.</span></span> <span data-ttu-id="2228b-114">Dies kann einen Thread oder Threads blockieren, wenn Arbeitsspeicher Vorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2228b-114">This may stall a thread or threads if memory operations are in progress.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="2228b-115">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="2228b-115">Minimum Shader Model</span></span>

<span data-ttu-id="2228b-116">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2228b-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2228b-117">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="2228b-117">Shader Model</span></span>                                                                | <span data-ttu-id="2228b-118">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="2228b-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="2228b-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="2228b-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="2228b-120">ja</span><span class="sxs-lookup"><span data-stu-id="2228b-120">yes</span></span>       |



 

<span data-ttu-id="2228b-121">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2228b-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2228b-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="2228b-122">Vertex</span></span> | <span data-ttu-id="2228b-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="2228b-123">Hull</span></span> | <span data-ttu-id="2228b-124">Domain</span><span class="sxs-lookup"><span data-stu-id="2228b-124">Domain</span></span> | <span data-ttu-id="2228b-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="2228b-125">Geometry</span></span> | <span data-ttu-id="2228b-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="2228b-126">Pixel</span></span> | <span data-ttu-id="2228b-127">Compute</span><span class="sxs-lookup"><span data-stu-id="2228b-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="2228b-128">x</span><span class="sxs-lookup"><span data-stu-id="2228b-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2228b-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2228b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2228b-130">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2228b-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="2228b-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="2228b-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




