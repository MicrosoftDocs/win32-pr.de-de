---
title: Allmemorybarrier-Funktion
description: Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Speicherzugriffe abgeschlossen sind.
ms.assetid: 63593de6-7b92-4f29-bcd9-21c69b9defcb
keywords:
- Allmemorybarrier-Funktion HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3252389da64b74e07853069c71315b290a2ba6d5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389324"
---
# <a name="allmemorybarrier-function"></a><span data-ttu-id="567d6-104">Allmemorybarrier-Funktion</span><span class="sxs-lookup"><span data-stu-id="567d6-104">AllMemoryBarrier function</span></span>

<span data-ttu-id="567d6-105">Blockiert die Ausführung aller Threads in einer Gruppe, bis alle Speicherzugriffe abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="567d6-105">Blocks execution of all threads in a group until all memory accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="567d6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="567d6-106">Syntax</span></span>

``` syntax
void AllMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="567d6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="567d6-107">Parameters</span></span>

<span data-ttu-id="567d6-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="567d6-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="567d6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="567d6-109">Return value</span></span>

<span data-ttu-id="567d6-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="567d6-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="567d6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="567d6-111">Remarks</span></span>

<span data-ttu-id="567d6-112">Eine Arbeitsspeicher Barriere gewährleistet, dass ausstehende Speichervorgänge abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="567d6-112">A memory barrier guarantees that outstanding memory operations have completed.</span></span> <span data-ttu-id="567d6-113">Threads werden bei groupsync-Barrieren synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="567d6-113">Threads are synchronized at GroupSync barriers.</span></span> <span data-ttu-id="567d6-114">Dies kann einen Thread oder Threads blockieren, wenn Arbeitsspeicher Vorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="567d6-114">This may stall a thread or threads if memory operations are in progress.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="567d6-115">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="567d6-115">Minimum Shader Model</span></span>

<span data-ttu-id="567d6-116">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="567d6-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="567d6-117">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="567d6-117">Shader Model</span></span>                                                                | <span data-ttu-id="567d6-118">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="567d6-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="567d6-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="567d6-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="567d6-120">ja</span><span class="sxs-lookup"><span data-stu-id="567d6-120">yes</span></span>       |



 

<span data-ttu-id="567d6-121">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="567d6-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="567d6-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="567d6-122">Vertex</span></span> | <span data-ttu-id="567d6-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="567d6-123">Hull</span></span> | <span data-ttu-id="567d6-124">Domain</span><span class="sxs-lookup"><span data-stu-id="567d6-124">Domain</span></span> | <span data-ttu-id="567d6-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="567d6-125">Geometry</span></span> | <span data-ttu-id="567d6-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="567d6-126">Pixel</span></span> | <span data-ttu-id="567d6-127">Compute</span><span class="sxs-lookup"><span data-stu-id="567d6-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="567d6-128">x</span><span class="sxs-lookup"><span data-stu-id="567d6-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="567d6-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="567d6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="567d6-130">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="567d6-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="567d6-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="567d6-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




