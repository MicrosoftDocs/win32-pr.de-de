---
title: Devicememorybarrier-Funktion
description: Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Gerätespeicher Zugriffe abgeschlossen sind.
ms.assetid: 904ab8f6-4849-4b13-8fac-3967cf66574e
keywords:
- Devicememorybarrier-Funktion HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875b780f528000d46ba31bb979072d6d462fa91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104388860"
---
# <a name="devicememorybarrier-function"></a><span data-ttu-id="6880c-104">Devicememorybarrier-Funktion</span><span class="sxs-lookup"><span data-stu-id="6880c-104">DeviceMemoryBarrier function</span></span>

<span data-ttu-id="6880c-105">Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Gerätespeicher Zugriffe abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="6880c-105">Blocks execution of all threads in a group until all device memory accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6880c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6880c-106">Syntax</span></span>

``` syntax
void DeviceMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="6880c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6880c-107">Parameters</span></span>

<span data-ttu-id="6880c-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6880c-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6880c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6880c-109">Return value</span></span>

<span data-ttu-id="6880c-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6880c-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6880c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6880c-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="6880c-112">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="6880c-112">Minimum Shader Model</span></span>

<span data-ttu-id="6880c-113">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6880c-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6880c-114">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6880c-114">Shader Model</span></span>                                                                | <span data-ttu-id="6880c-115">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="6880c-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6880c-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="6880c-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="6880c-117">ja</span><span class="sxs-lookup"><span data-stu-id="6880c-117">yes</span></span>       |



 

<span data-ttu-id="6880c-118">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6880c-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="6880c-119">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="6880c-119">Vertex</span></span> | <span data-ttu-id="6880c-120">Hülle</span><span class="sxs-lookup"><span data-stu-id="6880c-120">Hull</span></span> | <span data-ttu-id="6880c-121">Domain</span><span class="sxs-lookup"><span data-stu-id="6880c-121">Domain</span></span> | <span data-ttu-id="6880c-122">Geometrie</span><span class="sxs-lookup"><span data-stu-id="6880c-122">Geometry</span></span> | <span data-ttu-id="6880c-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="6880c-123">Pixel</span></span> | <span data-ttu-id="6880c-124">Compute</span><span class="sxs-lookup"><span data-stu-id="6880c-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6880c-125">x</span><span class="sxs-lookup"><span data-stu-id="6880c-125">x</span></span>     | <span data-ttu-id="6880c-126">x</span><span class="sxs-lookup"><span data-stu-id="6880c-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6880c-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6880c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6880c-128">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="6880c-128">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="6880c-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="6880c-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




