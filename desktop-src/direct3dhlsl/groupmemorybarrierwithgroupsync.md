---
title: Groupmemorybarrierwithgroupsync-Funktion
description: Blockiert die Ausführung aller Threads in einer Gruppe, bis alle freigegebenen Gruppen Zugriffe abgeschlossen sind und alle Threads in der Gruppe diesen Befehl erreicht haben.
ms.assetid: 64dd78e1-c597-4bd0-8a9b-592123178de5
keywords:
- Groupmemorybarrierwithgroupsync-Funktion HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07798bb8ad6bd9c4cdfa14bfa57d97818dbd6962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104976185"
---
# <a name="groupmemorybarrierwithgroupsync-function"></a><span data-ttu-id="42c75-104">Groupmemorybarrierwithgroupsync-Funktion</span><span class="sxs-lookup"><span data-stu-id="42c75-104">GroupMemoryBarrierWithGroupSync function</span></span>

<span data-ttu-id="42c75-105">Blockiert die Ausführung aller Threads in einer Gruppe, bis alle freigegebenen Gruppen Zugriffe abgeschlossen sind und alle Threads in der Gruppe diesen Befehl erreicht haben.</span><span class="sxs-lookup"><span data-stu-id="42c75-105">Blocks execution of all threads in a group until all group shared accesses have been completed and all threads in the group have reached this call.</span></span>

## <a name="syntax"></a><span data-ttu-id="42c75-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="42c75-106">Syntax</span></span>

``` syntax
void GroupMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a><span data-ttu-id="42c75-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="42c75-107">Parameters</span></span>

<span data-ttu-id="42c75-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="42c75-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="42c75-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42c75-109">Return value</span></span>

<span data-ttu-id="42c75-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="42c75-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42c75-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42c75-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="42c75-112">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="42c75-112">Minimum Shader Model</span></span>

<span data-ttu-id="42c75-113">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42c75-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="42c75-114">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="42c75-114">Shader Model</span></span>                                                                | <span data-ttu-id="42c75-115">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="42c75-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="42c75-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="42c75-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="42c75-117">ja</span><span class="sxs-lookup"><span data-stu-id="42c75-117">yes</span></span>       |



 

<span data-ttu-id="42c75-118">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="42c75-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="42c75-119">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="42c75-119">Vertex</span></span> | <span data-ttu-id="42c75-120">Hülle</span><span class="sxs-lookup"><span data-stu-id="42c75-120">Hull</span></span> | <span data-ttu-id="42c75-121">Domain</span><span class="sxs-lookup"><span data-stu-id="42c75-121">Domain</span></span> | <span data-ttu-id="42c75-122">Geometrie</span><span class="sxs-lookup"><span data-stu-id="42c75-122">Geometry</span></span> | <span data-ttu-id="42c75-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="42c75-123">Pixel</span></span> | <span data-ttu-id="42c75-124">Compute</span><span class="sxs-lookup"><span data-stu-id="42c75-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="42c75-125">x</span><span class="sxs-lookup"><span data-stu-id="42c75-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="42c75-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="42c75-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42c75-127">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="42c75-127">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="42c75-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="42c75-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




