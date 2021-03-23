---
title: Prädikation übersprungen
description: Das-Prädikat ist ein Feature, mit dem die GPU anstelle der CPU feststellen kann, ob ein Objekt nicht gezeichnet, kopiert oder versendet werden soll.
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a18df35c94fbd6b2b6f449585dfdcd4028bf2e9
ms.sourcegitcommit: 9dadca1a0d77cb2a372e5a941ec707f9d77b354d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2020
ms.locfileid: "104548725"
---
# <a name="predication"></a><span data-ttu-id="17a2a-103">Prädikation übersprungen</span><span class="sxs-lookup"><span data-stu-id="17a2a-103">Predication</span></span>

<span data-ttu-id="17a2a-104">Das-Prädikat ist ein Feature, mit dem die GPU anstelle der CPU feststellen kann, ob ein Objekt nicht gezeichnet, kopiert oder versendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="17a2a-104">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy, or dispatch an object.</span></span>

-   [<span data-ttu-id="17a2a-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="17a2a-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="17a2a-106">Setprediation</span><span class="sxs-lookup"><span data-stu-id="17a2a-106">SetPredication</span></span>](#setpredication)
-   [<span data-ttu-id="17a2a-107">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="17a2a-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="17a2a-108">Überblick</span><span class="sxs-lookup"><span data-stu-id="17a2a-108">Overview</span></span>

<span data-ttu-id="17a2a-109">Die typische Verwendung von Prädikaten ist die Okklusion. Wenn ein Begrenzungsfeld gezeichnet wird, das verdeckt wird, gibt es offensichtlich keinen Punkt, an dem das Objekt selbst gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="17a2a-109">The typical use of predication is with occlusion; if a bounding box is drawn and is occluded, there is obviously no point in drawing the object itself.</span></span> <span data-ttu-id="17a2a-110">In dieser Situation kann das Zeichnen des Objekts "predicated" lauten, wodurch die Entfernung aus dem tatsächlichen Rendering durch die GPU ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="17a2a-110">In this situation, the drawing of the object can be "predicated", enabling its removal from actual rendering by the GPU.</span></span>

<span data-ttu-id="17a2a-111">Zunächst erscheint dies möglicherweise auf dem Standard tiefen Test plus einem frühen tiefen Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="17a2a-111">At first, this might seem redudant over and above the standard depth test plus an early depth pass.</span></span> <span data-ttu-id="17a2a-112">Mit dem Prädikat kann jedoch der Aufwand des Draw-Befehls Zustands selbst und der rasterisierung entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="17a2a-112">But predication can remove the overhead of the draw command state itself, plus the rasterization.</span></span> <span data-ttu-id="17a2a-113">Während ein frühes tiefen Durchlauf unnötige Pixel entfernt, kann er weiterhin Scheitelpunkt-, Hull-, Domänen-und Geometry-Shader ausführen und den Eingabe Assembler, den tesselator und den Rasterizer für die Fixed-Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="17a2a-113">While an early depth pass removes unnecessary pixels, it can still execute vertex, hull, domain, and geometry shaders, and invoke the fixed-function input assembler, tesselator, and rasterizer.</span></span> <span data-ttu-id="17a2a-114">Durch das Zeichnen eines einfachen Begrenzungs Rahmens oder eines ähnlichen umgebenden Volumes &mdash; , das einfacher zu verarbeiten und zu verkleinern ist als das reale Modell, &mdash; vermeiden Sie unnötige rasterisierung und Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="17a2a-114">By drawing a simple bounding box or similar bounding volume&mdash;which is simpler to process and rasterize than the real model&mdash;you avoid unnecessary rasterization and processing.</span></span>

<span data-ttu-id="17a2a-115">Im Gegensatz zu Direct3D 11 wird das Prädikat von Abfragen entkoppelt und in Direct3D 12 erweitert, um einer Anwendung das Prädikat von Objekten basierend auf den Argumenten zu ermöglichen, für die der App-Entwickler möglicherweise entscheidet (nicht nur für die oksion).</span><span class="sxs-lookup"><span data-stu-id="17a2a-115">Unlike Direct3D 11, predication is decoupled from queries, and is expanded in Direct3D 12 to enable an application to predicate objects based on any reasoning the app developer may decide on (not just occlusion).</span></span>

## <a name="setpredication"></a><span data-ttu-id="17a2a-116">Setprediation</span><span class="sxs-lookup"><span data-stu-id="17a2a-116">SetPredication</span></span>

<span data-ttu-id="17a2a-117">Das Prädikat kann basierend auf dem Wert von 64-Bits innerhalb eines Puffers festgelegt werden (siehe [**D3D12 \_ \_ prediationop**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).</span><span class="sxs-lookup"><span data-stu-id="17a2a-117">Predication can be set based on the value of 64-bits within a buffer (refer to [**D3D12\_PREDICATION\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).</span></span>

<span data-ttu-id="17a2a-118">Wenn die GPU einen [**setprediationbefehl**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) ausführt, wird der Wert im Puffer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17a2a-118">When the GPU executes a [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) command it snaps the value in the buffer.</span></span> <span data-ttu-id="17a2a-119">Zukünftige Änderungen an den Daten im Puffer wirken sich nicht rückwirkend auf den prädikationszustand aus.</span><span class="sxs-lookup"><span data-stu-id="17a2a-119">Future changes to the data in the buffer do not retroactively affect the predication state.</span></span>

<span data-ttu-id="17a2a-120">Wenn der Eingabeparameter Puffer NULL ist, wird das Prädikat deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="17a2a-120">If the input parameter Buffer is NULL, then predication is disabled.</span></span>

<span data-ttu-id="17a2a-121">Prädikationshinweise sind nicht in der Direct3D 12-API vorhanden. und ein Prädikat ist in den Befehlslisten direkt, COMPUTE und Copy zulässig.</span><span class="sxs-lookup"><span data-stu-id="17a2a-121">Predication hints are not present in the Direct3D 12 API; and predication is allowed on direct, compute, and copy command lists.</span></span> <span data-ttu-id="17a2a-122">Der Quell Puffer kann einen beliebigen heaptyp aufweisen (Standard, Upload, Read Back, Custom).</span><span class="sxs-lookup"><span data-stu-id="17a2a-122">The source buffer can be in any heap type (default, upload, readback, custom).</span></span>

<span data-ttu-id="17a2a-123">Die Core-Laufzeit überprüft Folgendes:</span><span class="sxs-lookup"><span data-stu-id="17a2a-123">The core runtime will validate the following:</span></span>

-   <span data-ttu-id="17a2a-124">*Alignedbufferoffset* ist ein Vielfaches von 8 Bytes.</span><span class="sxs-lookup"><span data-stu-id="17a2a-124">*AlignedBufferOffset* is a multiple of 8 bytes</span></span>
-   <span data-ttu-id="17a2a-125">Die Ressource ist ein Puffer.</span><span class="sxs-lookup"><span data-stu-id="17a2a-125">The resource is a buffer</span></span>
-   <span data-ttu-id="17a2a-126">Der Vorgang ist ein gültiger Member der-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="17a2a-126">The operation is a valid member of the enumeration</span></span>
-   <span data-ttu-id="17a2a-127">" [**Setprediation**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) " kann nicht innerhalb eines Pakets aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="17a2a-127">[**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) cannot be called from within a bundle</span></span>
-   <span data-ttu-id="17a2a-128">Der Befehls Auflistungstyp unterstützt das Prädikat.</span><span class="sxs-lookup"><span data-stu-id="17a2a-128">The command list type supports predication</span></span>
-   <span data-ttu-id="17a2a-129">Der Offset überschreitet die Puffergröße nicht.</span><span class="sxs-lookup"><span data-stu-id="17a2a-129">The offset does not exceed the buffer size</span></span>

<span data-ttu-id="17a2a-130">Die debugschicht gibt einen Fehler aus, wenn sich der Quell Puffer nicht im [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) befindet (der mit [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)und einfach einem Alias)-Zustand ist.</span><span class="sxs-lookup"><span data-stu-id="17a2a-130">The debug layer will issue an error if the source buffer is not in the [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (which is the same as [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states), and simply an alias) state.</span></span>

<span data-ttu-id="17a2a-131">Die folgenden Vorgänge können als Prädikat festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="17a2a-131">The set of operations which can be predicated are:</span></span>

-   [<span data-ttu-id="17a2a-132">**Drawinstanzierte**</span><span class="sxs-lookup"><span data-stu-id="17a2a-132">**DrawInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)
-   [<span data-ttu-id="17a2a-133">**Drawindexedinstangeleitet**</span><span class="sxs-lookup"><span data-stu-id="17a2a-133">**DrawIndexedInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)
-   [<span data-ttu-id="17a2a-134">**Dispatch**</span><span class="sxs-lookup"><span data-stu-id="17a2a-134">**Dispatch**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [<span data-ttu-id="17a2a-135">**Copytextureregion**</span><span class="sxs-lookup"><span data-stu-id="17a2a-135">**CopyTextureRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="17a2a-136">**Copybufferregion**</span><span class="sxs-lookup"><span data-stu-id="17a2a-136">**CopyBufferRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="17a2a-137">**Copyresource**</span><span class="sxs-lookup"><span data-stu-id="17a2a-137">**CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="17a2a-138">**Copytiles**</span><span class="sxs-lookup"><span data-stu-id="17a2a-138">**CopyTiles**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="17a2a-139">**Resolvesubresource**</span><span class="sxs-lookup"><span data-stu-id="17a2a-139">**ResolveSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [<span data-ttu-id="17a2a-140">**ClearDepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="17a2a-140">**ClearDepthStencilView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [<span data-ttu-id="17a2a-141">**ClearRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="17a2a-141">**ClearRenderTargetView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [<span data-ttu-id="17a2a-142">**Clearunorderedaccessviewuint**</span><span class="sxs-lookup"><span data-stu-id="17a2a-142">**ClearUnorderedAccessViewUint**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="17a2a-143">**Clearunorderedaccessviewfloat**</span><span class="sxs-lookup"><span data-stu-id="17a2a-143">**ClearUnorderedAccessViewFloat**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [<span data-ttu-id="17a2a-144">**Executin Direct**</span><span class="sxs-lookup"><span data-stu-id="17a2a-144">**ExecuteIndirect**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)

<span data-ttu-id="17a2a-145">[**Executebundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) ist nicht selbst vorgegeben.</span><span class="sxs-lookup"><span data-stu-id="17a2a-145">[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) is not predicated itself.</span></span> <span data-ttu-id="17a2a-146">Stattdessen werden die einzelnen Vorgänge aus der Liste oben, die auf der Seite des Bündels enthalten sind, als Prädikat festgestellt.</span><span class="sxs-lookup"><span data-stu-id="17a2a-146">Instead, individual operations from the list above which are contained in side of the bundle are predicated.</span></span>

<span data-ttu-id="17a2a-147">Die ID3D12GraphicsCommandList-Methoden [**resolvequerydata**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**beginquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) und [**endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) sind nicht als Prädikat festgelegt.</span><span class="sxs-lookup"><span data-stu-id="17a2a-147">The ID3D12GraphicsCommandList methods [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) and [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) are not predicated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17a2a-148">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="17a2a-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17a2a-149">Zähler und Abfragen</span><span class="sxs-lookup"><span data-stu-id="17a2a-149">Counters and Queries</span></span>](counters-and-queries.md)
</dt> <dt>

[<span data-ttu-id="17a2a-150">Leistungsmessung</span><span class="sxs-lookup"><span data-stu-id="17a2a-150">Performance Measurement</span></span>](performance-measurement.md)
</dt> <dt>

[<span data-ttu-id="17a2a-151">Exemplarische Vorgehensweise für prediationqueries</span><span class="sxs-lookup"><span data-stu-id="17a2a-151">Predication queries walk-through</span></span>](predication-queries.md)
</dt> </dl>

 

 




