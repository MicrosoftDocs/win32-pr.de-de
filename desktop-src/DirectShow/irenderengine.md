---
description: 'Die Schnittstelle "" wird durch das Erstellen eines Filter Diagramms aus einer Zeitachse ein Projekt vom Typ "DirectShow-Bearbeitungs Dienste" gerendert. Des bietet zwei Komponenten, die diese Schnittstelle implementieren: die einfache Renderingengine erstellt eine unkomprimierte Ausgabe.'
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: Unenderengine-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d8c57e976fac877a02c3f3993fb3fe4d27f9033b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370811"
---
# <a name="irenderengine-interface"></a><span data-ttu-id="489f3-103">Schnittstelle ""</span><span class="sxs-lookup"><span data-stu-id="489f3-103">IRenderEngine interface</span></span>

> [!Note]  
> <span data-ttu-id="489f3-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="489f3-104">\[Deprecated.</span></span> <span data-ttu-id="489f3-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="489f3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="489f3-106">Die- `IRenderEngine` Schnittstelle rendert ein [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) -Projekt durch Erstellen eines Filter Diagramms aus einer Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="489f3-106">The `IRenderEngine` interface renders a [DirectShow Editing Services](directshow-editing-services.md) (DES) project by constructing a filter graph from a timeline.</span></span>

<span data-ttu-id="489f3-107">DES bietet zwei Komponenten, die diese Schnittstelle implementieren:</span><span class="sxs-lookup"><span data-stu-id="489f3-107">DES provides two components that implement this interface:</span></span>

-   <span data-ttu-id="489f3-108">Die *einfache Renderingengine* erstellt eine nicht komprimierte Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="489f3-108">The *basic render engine* creates uncompressed output.</span></span> <span data-ttu-id="489f3-109">Sie können die Ausgabe für die Vorschau verwenden oder Sie durch Komprimierungs Filter weiterleiten und in eine Datei schreiben.</span><span class="sxs-lookup"><span data-stu-id="489f3-109">You can use the output for preview, or route it through compression filters and write it to a file.</span></span>
-   <span data-ttu-id="489f3-110">Die *Smart-Rendering-Engine* erstellt mithilfe der *intelligenten Neukomprimierung* eine komprimierte Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="489f3-110">The *smart render engine* creates compressed output, using *smart recompression*.</span></span> <span data-ttu-id="489f3-111">Bei intelligenter Neukomprimierung wird eine Quelldatei nur dann erneut komprimiert, wenn sich ihr Format vom Ausgabeformat unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="489f3-111">With smart recompression, a source file is recompressed only if its format differs from the output format.</span></span> <span data-ttu-id="489f3-112">Eine Quelle mit einem übereinstimmenden Format wird direkt in die Ausgabedatei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="489f3-112">A source with a matching format is written directly to the output file.</span></span> <span data-ttu-id="489f3-113">Je nach Szenario kann die Renderingzeit durch intelligente Neukomprimierung erheblich verbessert werden.</span><span class="sxs-lookup"><span data-stu-id="489f3-113">Depending on the scenario, smart recompression can greatly improve rendering time.</span></span>

<span data-ttu-id="489f3-114">Die Smart-Rendering-Engine unterstützt auch die [**ismartrenderengine**](ismartrenderengine.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="489f3-114">The smart render engine also supports the [**ISmartRenderEngine**](ismartrenderengine.md) interface.</span></span>

<span data-ttu-id="489f3-115">Obwohl eine Anwendung ein Filter Diagramm erstellen und an eine Renderingengine übergeben kann, besteht das typische Szenario darin, dass die Renderingengine das Filter Diagramm erstellt.</span><span class="sxs-lookup"><span data-stu-id="489f3-115">Although an application can create a filter graph and pass it to a render engine, the typical scenario is for the render engine to create the filter graph.</span></span> <span data-ttu-id="489f3-116">Der Aufbau des Diagramms ist ein zweistufiger Prozess.</span><span class="sxs-lookup"><span data-stu-id="489f3-116">Building the graph is a two-stage process.</span></span> <span data-ttu-id="489f3-117">Erstellen Sie zuerst das Front-End, indem Sie die Methode " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md) " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="489f3-117">First, build the front end by calling the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span> <span data-ttu-id="489f3-118">Verbinden Sie anschließend die Ausgabe Pins auf dem Front-End mit den gewünschten renderingfiltern:</span><span class="sxs-lookup"><span data-stu-id="489f3-118">Then connect the output pins on the front end to the desired rendering filters:</span></span>

-   <span data-ttu-id="489f3-119">Video-und audiorenderer für die Vorschauversion oder</span><span class="sxs-lookup"><span data-stu-id="489f3-119">Video and audio renderers for preview, or</span></span>
-   <span data-ttu-id="489f3-120">Kompressoren, Multiplexer und Datei Schreiber, um die endgültige Ausgabe zu generieren.</span><span class="sxs-lookup"><span data-stu-id="489f3-120">Compressors, multiplexers, and file writers to generate the final output.</span></span>

## <a name="members"></a><span data-ttu-id="489f3-121">Member</span><span class="sxs-lookup"><span data-stu-id="489f3-121">Members</span></span>

<span data-ttu-id="489f3-122">Die Schnittstelle " **irienderengine** " erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="489f3-122">The **IRenderEngine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="489f3-123">" **Irienderengine** " verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="489f3-123">**IRenderEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="489f3-124">Methoden</span><span class="sxs-lookup"><span data-stu-id="489f3-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="489f3-125">Methoden</span><span class="sxs-lookup"><span data-stu-id="489f3-125">Methods</span></span>

<span data-ttu-id="489f3-126">Die " **irienderengine** "-Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="489f3-126">The **IRenderEngine** interface has these methods.</span></span>



| <span data-ttu-id="489f3-127">Methode</span><span class="sxs-lookup"><span data-stu-id="489f3-127">Method</span></span>                                                                             | <span data-ttu-id="489f3-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="489f3-128">Description</span></span>                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="489f3-129">**Einzusetzen**</span><span class="sxs-lookup"><span data-stu-id="489f3-129">**Commit**</span></span>](irenderengine-commit.md)                                             | <span data-ttu-id="489f3-130">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="489f3-130">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="489f3-131">**Connectfrontend**</span><span class="sxs-lookup"><span data-stu-id="489f3-131">**ConnectFrontEnd**</span></span>](irenderengine-connectfrontend.md)                           | <span data-ttu-id="489f3-132">Erstellt das Front-End des Filter Diagramms aus der aktuellen Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="489f3-132">Builds the front end of the filter graph from the current timeline.</span></span><br/>        |
| [<span data-ttu-id="489f3-133">**Decommit**</span><span class="sxs-lookup"><span data-stu-id="489f3-133">**Decommit**</span></span>](irenderengine-decommit.md)                                         | <span data-ttu-id="489f3-134">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="489f3-134">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="489f3-135">**Dosmartrecompression**</span><span class="sxs-lookup"><span data-stu-id="489f3-135">**DoSmartRecompression**</span></span>](irenderengine-dosmartrecompression.md)                 | <span data-ttu-id="489f3-136">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="489f3-136">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="489f3-137">**Getcaps**</span><span class="sxs-lookup"><span data-stu-id="489f3-137">**GetCaps**</span></span>](irenderengine-getcaps.md)                                           | <span data-ttu-id="489f3-138">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="489f3-138">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="489f3-139">**Getfiltergraph**</span><span class="sxs-lookup"><span data-stu-id="489f3-139">**GetFilterGraph**</span></span>](irenderengine-getfiltergraph.md)                             | <span data-ttu-id="489f3-140">Ruft das Filter Diagramm ab, das von der Rendering-Engine erstellt wurde (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="489f3-140">Retrieves the filter graph that the render engine has constructed, if any.</span></span><br/> |
| [<span data-ttu-id="489f3-141">**Getgroupoutputpin**</span><span class="sxs-lookup"><span data-stu-id="489f3-141">**GetGroupOutputPin**</span></span>](irenderengine-getgroupoutputpin.md)                       | <span data-ttu-id="489f3-142">Ruft die Ausgabepin für die angegebene Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="489f3-142">Retrieves the output pin for the specified group.</span></span><br/>                          |
| [<span data-ttu-id="489f3-143">**Gettimelineobject**</span><span class="sxs-lookup"><span data-stu-id="489f3-143">**GetTimelineObject**</span></span>](irenderengine-gettimelineobject.md)                       | <span data-ttu-id="489f3-144">Ruft die Zeitachse ab, die von der Rendering-Engine zurzeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="489f3-144">Retrieves the timeline that the render engine is currently using.</span></span><br/>          |
| [<span data-ttu-id="489f3-145">**Getvendorstring**</span><span class="sxs-lookup"><span data-stu-id="489f3-145">**GetVendorString**</span></span>](irenderengine-getvendorstring.md)                           | <span data-ttu-id="489f3-146">Ruft die Hersteller Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="489f3-146">Retrieves the vendor string.</span></span><br/>                                               |
| [<span data-ttu-id="489f3-147">**Renderoutputpins**</span><span class="sxs-lookup"><span data-stu-id="489f3-147">**RenderOutputPins**</span></span>](irenderengine-renderoutputpins.md)                         | <span data-ttu-id="489f3-148">Erstellt den Preview-Teil des Filter Diagramms.</span><span class="sxs-lookup"><span data-stu-id="489f3-148">Creates the previewing portion of the filter graph.</span></span><br/>                        |
| [<span data-ttu-id="489f3-149">**Scrapit**</span><span class="sxs-lookup"><span data-stu-id="489f3-149">**ScrapIt**</span></span>](irenderengine-scrapit.md)                                           | <span data-ttu-id="489f3-150">Verwirft das Filter Diagramm der Rendering-Engine und alle zugeordneten Objekte.</span><span class="sxs-lookup"><span data-stu-id="489f3-150">Discards the render engine's filter graph and all associated objects.</span></span><br/>      |
| [<span data-ttu-id="489f3-151">**Setdynamikreconnectlevel**</span><span class="sxs-lookup"><span data-stu-id="489f3-151">**SetDynamicReconnectLevel**</span></span>](irenderengine-setdynamicreconnectlevel.md)         | <span data-ttu-id="489f3-152">Legt die Ebene der dynamischen erneuten Verbindung während des Renderings fest.</span><span class="sxs-lookup"><span data-stu-id="489f3-152">Sets the level of dynamic reconnection during rendering.</span></span><br/>                   |
| [<span data-ttu-id="489f3-153">**Setfiltergraph**</span><span class="sxs-lookup"><span data-stu-id="489f3-153">**SetFilterGraph**</span></span>](irenderengine-setfiltergraph.md)                             | <span data-ttu-id="489f3-154">Gibt ein Filter Diagramm für die zu verwendende Rendering-Engine an.</span><span class="sxs-lookup"><span data-stu-id="489f3-154">Specifies a filter graph for the render engine to use.</span></span><br/>                     |
| [<span data-ttu-id="489f3-155">**Setinterestrange**</span><span class="sxs-lookup"><span data-stu-id="489f3-155">**SetInterestRange**</span></span>](irenderengine-setinterestrange.md)                         | <span data-ttu-id="489f3-156">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="489f3-156">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="489f3-157">**SetInterestRange2**</span><span class="sxs-lookup"><span data-stu-id="489f3-157">**SetInterestRange2**</span></span>](irenderengine-setinterestrange2.md)                       | <span data-ttu-id="489f3-158">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="489f3-158">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="489f3-159">**"Strenderrange"**</span><span class="sxs-lookup"><span data-stu-id="489f3-159">**SetRenderRange**</span></span>](irenderengine-setrenderrange.md)                             | <span data-ttu-id="489f3-160">Legt den Zeitbereich fest, der gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="489f3-160">Sets the range of time to be rendered.</span></span><br/>                                     |
| [<span data-ttu-id="489f3-161">**SetRenderRange2**</span><span class="sxs-lookup"><span data-stu-id="489f3-161">**SetRenderRange2**</span></span>](irenderengine-setrenderrange2.md)                           | <span data-ttu-id="489f3-162">Legt den Zeitbereich, der gerendert werden soll, als **Double** fest.</span><span class="sxs-lookup"><span data-stu-id="489f3-162">Sets the range of time to be rendered, as a **double**.</span></span><br/>                    |
| [<span data-ttu-id="489f3-163">**Setsourceconnectcallback**</span><span class="sxs-lookup"><span data-stu-id="489f3-163">**SetSourceConnectCallback**</span></span>](irenderengine-setsourceconnectcallback.md)         | <span data-ttu-id="489f3-164">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="489f3-164">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="489f3-165">**Setsourcenamevalidation**</span><span class="sxs-lookup"><span data-stu-id="489f3-165">**SetSourceNameValidation**</span></span>](irenderengine-setsourcenamevalidation.md)           | <span data-ttu-id="489f3-166">Gibt an, wie die Renderingengine Dateinamen überprüft.</span><span class="sxs-lookup"><span data-stu-id="489f3-166">Specifies how the render engine validates file names.</span></span><br/>                      |
| [<span data-ttu-id="489f3-167">**Settimelineobject**</span><span class="sxs-lookup"><span data-stu-id="489f3-167">**SetTimelineObject**</span></span>](irenderengine-settimelineobject.md)                       | <span data-ttu-id="489f3-168">Legt die Zeitachse für die zu verwendende Rendering-Engine fest.</span><span class="sxs-lookup"><span data-stu-id="489f3-168">Sets the timeline for the render engine to use.</span></span><br/>                            |
| [<span data-ttu-id="489f3-169">**"US-smartrecompressiongraph"**</span><span class="sxs-lookup"><span data-stu-id="489f3-169">**UseInSmartRecompressionGraph**</span></span>](irenderengine-useinsmartrecompressiongraph.md) | <span data-ttu-id="489f3-170">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="489f3-170">Not supported.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="489f3-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="489f3-171">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="489f3-172">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="489f3-172">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="489f3-173">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="489f3-173">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="489f3-174">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="489f3-174">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="489f3-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="489f3-175">Requirements</span></span>



| <span data-ttu-id="489f3-176">Anforderung</span><span class="sxs-lookup"><span data-stu-id="489f3-176">Requirement</span></span> | <span data-ttu-id="489f3-177">Wert</span><span class="sxs-lookup"><span data-stu-id="489f3-177">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="489f3-178">Header</span><span class="sxs-lookup"><span data-stu-id="489f3-178">Header</span></span><br/>  | <dl> <span data-ttu-id="489f3-179"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="489f3-179"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="489f3-180">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="489f3-180">Library</span></span><br/> | <dl> <span data-ttu-id="489f3-181"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="489f3-181"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="489f3-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="489f3-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="489f3-183">Rendern eines Projekts</span><span class="sxs-lookup"><span data-stu-id="489f3-183">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 
