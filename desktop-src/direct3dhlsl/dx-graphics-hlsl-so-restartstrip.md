---
title: Restartstrip (DirectX HLSL Stream-Output-Objekt)
description: Beendet den aktuellen primitiven Strip und startet einen neuen Strip. Wenn für den aktuellen Strip nicht genügend Scheitel Punkte ausgegeben werden, um die primitive Topologie auszufüllen, wird der unvollständige primitive am Ende verworfen.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16b31bbd1e2f72ce6b31a0c079f7ec5739aba87a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993423"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a><span data-ttu-id="3998a-104">Restartstrip (DirectX HLSL Stream-Output-Objekt)</span><span class="sxs-lookup"><span data-stu-id="3998a-104">RestartStrip (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="3998a-105">Beendet den aktuellen primitiven Strip und startet einen neuen Strip.</span><span class="sxs-lookup"><span data-stu-id="3998a-105">Ends the current primitive strip and starts a new strip.</span></span> <span data-ttu-id="3998a-106">Wenn für den aktuellen Strip nicht genügend Scheitel Punkte ausgegeben werden, um die primitive Topologie auszufüllen, wird der unvollständige primitive am Ende verworfen.</span><span class="sxs-lookup"><span data-stu-id="3998a-106">If the current strip does not have enough vertices emitted to fill the primitive topology, the incomplete primitive at the end will be discarded.</span></span>



|                 |
|-----------------|
| <span data-ttu-id="3998a-107">Restartstrip ();</span><span class="sxs-lookup"><span data-stu-id="3998a-107">RestartStrip();</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="3998a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3998a-108">Parameters</span></span>



| <span data-ttu-id="3998a-109">Element</span><span class="sxs-lookup"><span data-stu-id="3998a-109">Item</span></span>                                                                                     | <span data-ttu-id="3998a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3998a-110">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="3998a-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Gar**</span><span class="sxs-lookup"><span data-stu-id="3998a-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None**</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="3998a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3998a-112">Return Value</span></span>

<span data-ttu-id="3998a-113">Keine</span><span class="sxs-lookup"><span data-stu-id="3998a-113">None</span></span>

## <a name="remarks"></a><span data-ttu-id="3998a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3998a-114">Remarks</span></span>

<span data-ttu-id="3998a-115">Ein Strip-Cut bewirkt, dass der aktuelle Bereich endet und ein neuer Bereich gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3998a-115">A strip cut causes the current strip to end, and a new strip to start.</span></span> <span data-ttu-id="3998a-116">Ein Bereichs Ausschnitt kann durch explizites Aufrufen dieser Methode oder durch Rendering bis zum maximalen Indexwert (1, 0xFFFFFFFF für 32-Bit-Indizes oder 0xFFFF für 16-Bit-Indizes) durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3998a-116">A strip cut can be done by explicitly calling this method, or just by rendering up to the maximum index value ( 1, which is 0xffffffff for 32-bit indices or 0xffff for 16-bit indices).</span></span> <span data-ttu-id="3998a-117">Jede Instanz einer indizierten, instanzierten Zeichnung generiert automatisch einen Bereichs Ausschnitt.</span><span class="sxs-lookup"><span data-stu-id="3998a-117">Each instance of an indexed-instanced draw generates a strip cut automatically.</span></span> <span data-ttu-id="3998a-118">Dies gilt auch dann, wenn es sich bei der Topologie nicht um einen Dreiecks Streifen handelt.</span><span class="sxs-lookup"><span data-stu-id="3998a-118">This is true even if the topology is not a triangle strip.</span></span>

> [!Note]  
> <span data-ttu-id="3998a-119">Die Unterstützung für den Neustart und der 1 "Magic Value" for a Cut sind nur auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3998a-119">Support for restart and the  1 'magic value' for a cut is only available on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 or higher devices.</span></span>

 

<span data-ttu-id="3998a-120">Es wird immer angenommen, dass es sich um einen Dreiecks Streifen handelt.</span><span class="sxs-lookup"><span data-stu-id="3998a-120">The output is always assumed to be a triangle strip.</span></span> <span data-ttu-id="3998a-121">Um die Ausgabe zu einer Dreiecks Liste zu machen, müssen Sie restartstrip zwischen jedem Dreieck aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3998a-121">To make the output a triangle list, you must call RestartStrip between each triangle.</span></span> <span data-ttu-id="3998a-122">Dreiecks Lüfter werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3998a-122">Triangle fans are unsupported.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="3998a-123">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="3998a-123">Minimum Shader Model</span></span>

<span data-ttu-id="3998a-124">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3998a-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3998a-125">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="3998a-125">Shader Model</span></span>                                              | <span data-ttu-id="3998a-126">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="3998a-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3998a-127">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="3998a-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3998a-128">ja</span><span class="sxs-lookup"><span data-stu-id="3998a-128">yes</span></span>       |
| [<span data-ttu-id="3998a-129">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3998a-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3998a-130">nein</span><span class="sxs-lookup"><span data-stu-id="3998a-130">no</span></span>        |
| [<span data-ttu-id="3998a-131">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3998a-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3998a-132">nein</span><span class="sxs-lookup"><span data-stu-id="3998a-132">no</span></span>        |
| [<span data-ttu-id="3998a-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3998a-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3998a-134">nein</span><span class="sxs-lookup"><span data-stu-id="3998a-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3998a-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3998a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3998a-136">Stream-Output-Objekt</span><span class="sxs-lookup"><span data-stu-id="3998a-136">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

