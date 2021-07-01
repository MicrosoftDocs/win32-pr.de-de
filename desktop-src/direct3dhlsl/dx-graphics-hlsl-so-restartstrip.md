---
title: RestartStrip (DirectX HLSL Stream-Output Object)
description: Beendet den aktuellen primitiven Strip und startet einen neuen Strip. Wenn für den aktuellen Strip nicht genügend Scheitelpunkte ausgegeben werden, um die primitive Topologie zu füllen, wird das unvollständige Primitive am Ende verworfen.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aafd6407d556a6d0b4269c38192107edbc7cb1fa
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120195"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a><span data-ttu-id="5a425-104">RestartStrip (DirectX HLSL Stream-Output Object)</span><span class="sxs-lookup"><span data-stu-id="5a425-104">RestartStrip (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="5a425-105">Beendet den aktuellen primitiven Strip und startet einen neuen Strip.</span><span class="sxs-lookup"><span data-stu-id="5a425-105">Ends the current primitive strip and starts a new strip.</span></span> <span data-ttu-id="5a425-106">Wenn für den aktuellen Strip nicht genügend Scheitelpunkte ausgegeben werden, um die primitive Topologie zu füllen, wird das unvollständige Primitive am Ende verworfen.</span><span class="sxs-lookup"><span data-stu-id="5a425-106">If the current strip does not have enough vertices emitted to fill the primitive topology, the incomplete primitive at the end will be discarded.</span></span>

<span data-ttu-id="5a425-107">RestartStrip();</span><span class="sxs-lookup"><span data-stu-id="5a425-107">RestartStrip();</span></span>



 

## <a name="parameters"></a><span data-ttu-id="5a425-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a425-108">Parameters</span></span>



| <span data-ttu-id="5a425-109">Element</span><span class="sxs-lookup"><span data-stu-id="5a425-109">Item</span></span>                                                                                     | <span data-ttu-id="5a425-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a425-110">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="5a425-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**nichts**</span><span class="sxs-lookup"><span data-stu-id="5a425-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None**</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="5a425-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a425-112">Return Value</span></span>

<span data-ttu-id="5a425-113">Keine</span><span class="sxs-lookup"><span data-stu-id="5a425-113">None</span></span>

## <a name="remarks"></a><span data-ttu-id="5a425-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a425-114">Remarks</span></span>

<span data-ttu-id="5a425-115">Ein Strip cut bewirkt, dass der aktuelle Strip endet und ein neuer Strip gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5a425-115">A strip cut causes the current strip to end, and a new strip to start.</span></span> <span data-ttu-id="5a425-116">Ein Strip cut kann durch explizites Aufrufen dieser Methode oder einfach durch Rendern bis zum maximalen Indexwert (1, der für 32-Bit-Indizes 0xffffffff ist, oder 0xffff für 16-Bit-Indizes) erfolgen.</span><span class="sxs-lookup"><span data-stu-id="5a425-116">A strip cut can be done by explicitly calling this method, or just by rendering up to the maximum index value ( 1, which is 0xffffffff for 32-bit indices or 0xffff for 16-bit indices).</span></span> <span data-ttu-id="5a425-117">Jede Instanz eines indizierten instanziierten Zeichnens generiert automatisch einen Strip cut.</span><span class="sxs-lookup"><span data-stu-id="5a425-117">Each instance of an indexed-instanced draw generates a strip cut automatically.</span></span> <span data-ttu-id="5a425-118">Dies gilt auch, wenn die Topologie kein Dreiecksstreifen ist.</span><span class="sxs-lookup"><span data-stu-id="5a425-118">This is true even if the topology is not a triangle strip.</span></span>

> [!Note]  
> <span data-ttu-id="5a425-119">Unterstützung für Neustart und 1 "Magischer Wert" für einen Cut ist nur auf Geräten der [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5a425-119">Support for restart and the  1 'magic value' for a cut is only available on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 or higher devices.</span></span>

 

<span data-ttu-id="5a425-120">Die Ausgabe wird immer als Dreiecksstreifen angenommen.</span><span class="sxs-lookup"><span data-stu-id="5a425-120">The output is always assumed to be a triangle strip.</span></span> <span data-ttu-id="5a425-121">Um die Ausgabe zu einer Dreiecksliste zu machen, müssen Sie RestartStrip zwischen den einzelnen Dreiecken aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5a425-121">To make the output a triangle list, you must call RestartStrip between each triangle.</span></span> <span data-ttu-id="5a425-122">Dreiecksfächer werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5a425-122">Triangle fans are unsupported.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="5a425-123">Shader-Mindestmodell</span><span class="sxs-lookup"><span data-stu-id="5a425-123">Minimum Shader Model</span></span>

<span data-ttu-id="5a425-124">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5a425-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5a425-125">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5a425-125">Shader Model</span></span>                                              | <span data-ttu-id="5a425-126">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5a425-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5a425-127">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="5a425-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5a425-128">Ja</span><span class="sxs-lookup"><span data-stu-id="5a425-128">yes</span></span>       |
| [<span data-ttu-id="5a425-129">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a425-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5a425-130">Nein</span><span class="sxs-lookup"><span data-stu-id="5a425-130">no</span></span>        |
| [<span data-ttu-id="5a425-131">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a425-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5a425-132">Nein</span><span class="sxs-lookup"><span data-stu-id="5a425-132">no</span></span>        |
| [<span data-ttu-id="5a425-133">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a425-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5a425-134">Nein</span><span class="sxs-lookup"><span data-stu-id="5a425-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5a425-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5a425-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a425-136">Stream-Output-Objekt</span><span class="sxs-lookup"><span data-stu-id="5a425-136">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

