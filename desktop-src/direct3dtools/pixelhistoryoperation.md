---
description: Stellt Informationen über den Pixel Verlauf dar.
MS-HAID: vspixengine.PixelHistoryOperation
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pixelhistoryoperation-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59DC72FC-3865-48D3-9F92-9BE93DCA093B
api_name:
- PixelHistoryOperation
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c02a6725f588aaa4c7d72c48d03d921503d4e6a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346402"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span data-ttu-id="d95a6-103"><span id="vspixengine.pixelhistoryoperation"></span>Pixelhistoryoperation-Struktur</span><span class="sxs-lookup"><span data-stu-id="d95a6-103"><span id="vspixengine.pixelhistoryoperation"></span>PixelHistoryOperation structure</span></span>

<span data-ttu-id="d95a6-104">Stellt Informationen über den Pixel Verlauf dar.</span><span class="sxs-lookup"><span data-stu-id="d95a6-104">Represents information about pixel history.</span></span>

## <a name="syntax"></a><span data-ttu-id="d95a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d95a6-105">Syntax</span></span>


```C++
} PixelHistoryOperation;
```

## <a name="members"></a><span data-ttu-id="d95a6-106">Member</span><span class="sxs-lookup"><span data-stu-id="d95a6-106">Members</span></span>

<span data-ttu-id="d95a6-107">**VEI**</span><span class="sxs-lookup"><span data-stu-id="d95a6-107">**eid**</span></span>  
<span data-ttu-id="d95a6-108">Die ID des Grafik Ereignisses, das diesem Vorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d95a6-108">The ID of the graphics event associated with this operation.</span></span>

<span data-ttu-id="d95a6-109">**PCP**</span><span class="sxs-lookup"><span data-stu-id="d95a6-109">**PCP**</span></span>  
<span data-ttu-id="d95a6-110">Diesem Vorgang zugeordnete gepackte Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="d95a6-110">Packed calls associated with this operation.</span></span>

<span data-ttu-id="d95a6-111">**rendertargetptr**</span><span class="sxs-lookup"><span data-stu-id="d95a6-111">**renderTargetPtr**</span></span>  
<span data-ttu-id="d95a6-112">Das Renderziel, das ursprünglich (innerhalb der erfassten Anwendung) mit diesem Vorgang zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d95a6-112">The render target originally associated (inside the captured application) with this operation.</span></span>

<span data-ttu-id="d95a6-113">**iprim**</span><span class="sxs-lookup"><span data-stu-id="d95a6-113">**iPrim**</span></span>  
<span data-ttu-id="d95a6-114">Der Index des eigentlichen primitiven, dem der Vorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d95a6-114">The index of the actual primitive associated witht his operation.</span></span>

<span data-ttu-id="d95a6-115">**numprims**</span><span class="sxs-lookup"><span data-stu-id="d95a6-115">**numPrims**</span></span>  
<span data-ttu-id="d95a6-116">Die Gesamtanzahl der diesem Vorgang zugeordneten primitiver.</span><span class="sxs-lookup"><span data-stu-id="d95a6-116">The total number of primitives associated with this operation.</span></span>

<span data-ttu-id="d95a6-117">**numvertsperprim**</span><span class="sxs-lookup"><span data-stu-id="d95a6-117">**numVertsPerPrim**</span></span>  
<span data-ttu-id="d95a6-118">Die Anzahl der Vertices pro primitiver.</span><span class="sxs-lookup"><span data-stu-id="d95a6-118">The number of vertices per primitive.</span></span>

<span data-ttu-id="d95a6-119">**iinstance**</span><span class="sxs-lookup"><span data-stu-id="d95a6-119">**iInstance**</span></span>  
<span data-ttu-id="d95a6-120">Beim Rendern von Instanzen die Instanznummer der eigentlichen Instanz, die diesem Vorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d95a6-120">When rendering instances, the instance number of the actual instance associated with this operation.</span></span>

<span data-ttu-id="d95a6-121">**iinstancecount**</span><span class="sxs-lookup"><span data-stu-id="d95a6-121">**iInstanceCount**</span></span>  
<span data-ttu-id="d95a6-122">Beim Rendern von Instanzen die Gesamtzahl der diesem Vorgang zugeordneten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="d95a6-122">When rendering instances, the total number of instances associated with this operation.</span></span>

<span data-ttu-id="d95a6-123">**bassemblerstagegeneratesinstanceid**</span><span class="sxs-lookup"><span data-stu-id="d95a6-123">**bAssemblerStageGeneratesInstanceID**</span></span>  
<span data-ttu-id="d95a6-124">true, wenn der Eingabe Assembler Instanz-IDs generiert. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="d95a6-124">true if the input assembler generates instance IDs; otherwise false.</span></span>

<span data-ttu-id="d95a6-125">**flags**</span><span class="sxs-lookup"><span data-stu-id="d95a6-125">**flags**</span></span>  
<span data-ttu-id="d95a6-126">Eine Kombination von pixelhistoryflags-Werten.</span><span class="sxs-lookup"><span data-stu-id="d95a6-126">A combination of PIXELHISTORYFLAGS values.</span></span> <span data-ttu-id="d95a6-127">Weitere Informationen finden Sie unter der pixelhistoryflags-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="d95a6-127">For more information, see the PIXELHISTORYFLAGS enumeration.</span></span>

<span data-ttu-id="d95a6-128">**pvsfile**</span><span class="sxs-lookup"><span data-stu-id="d95a6-128">**pVSFile**</span></span>  
<span data-ttu-id="d95a6-129">Ein "fleptr" für den Pixel-Shader-Bytestream.</span><span class="sxs-lookup"><span data-stu-id="d95a6-129">A FILEPTR for the pixel shader byte stream.</span></span> <span data-ttu-id="d95a6-130">Dies wird zurückgegeben, um zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="d95a6-130">This is passed back in order to debug.</span></span>

<span data-ttu-id="d95a6-131">**pgsfile**</span><span class="sxs-lookup"><span data-stu-id="d95a6-131">**pGSFile**</span></span>  
<span data-ttu-id="d95a6-132">Ein "fleptr" für den Geometry-Shader-Bytestream.</span><span class="sxs-lookup"><span data-stu-id="d95a6-132">A FILEPTR for the geometry shader byte stream.</span></span> <span data-ttu-id="d95a6-133">Dies wird zurückgegeben, um zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="d95a6-133">This is passed back in order to debug.</span></span>

<span data-ttu-id="d95a6-134">**ppsfile**</span><span class="sxs-lookup"><span data-stu-id="d95a6-134">**pPSFile**</span></span>  
<span data-ttu-id="d95a6-135">Ein "fleptr" für den Pixel-Shader-Bytestream.</span><span class="sxs-lookup"><span data-stu-id="d95a6-135">A FILEPTR for the pixel shader byte stream.</span></span> <span data-ttu-id="d95a6-136">Dies wird zurückgegeben, um zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="d95a6-136">This is passed back in order to debug.</span></span>

<span data-ttu-id="d95a6-137">**phsfile**</span><span class="sxs-lookup"><span data-stu-id="d95a6-137">**pHSFile**</span></span>  
<span data-ttu-id="d95a6-138">Ein "fleptr" für den Hull-Shader-Bytestream.</span><span class="sxs-lookup"><span data-stu-id="d95a6-138">A FILEPTR for the hull shader byte stream.</span></span> <span data-ttu-id="d95a6-139">Dies wird zurückgegeben, um zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="d95a6-139">This is passed back in order to debug.</span></span>

<span data-ttu-id="d95a6-140">**pdsfile**</span><span class="sxs-lookup"><span data-stu-id="d95a6-140">**pDSFile**</span></span>  
<span data-ttu-id="d95a6-141">Ein "fleptr" für den Domänen-Shader-Bytestream.</span><span class="sxs-lookup"><span data-stu-id="d95a6-141">A FILEPTR for the domain shader byte stream.</span></span> <span data-ttu-id="d95a6-142">Dies wird zurückgegeben, um zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="d95a6-142">This is passed back in order to debug.</span></span>

<span data-ttu-id="d95a6-143">**pcsfile**</span><span class="sxs-lookup"><span data-stu-id="d95a6-143">**pCSFile**</span></span>  
<span data-ttu-id="d95a6-144">Ein "fleptr" für den Compute-Shader-Bytestream.</span><span class="sxs-lookup"><span data-stu-id="d95a6-144">A FILEPTR for the compute shader byte stream.</span></span> <span data-ttu-id="d95a6-145">Dies wird zurückgegeben, um zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="d95a6-145">This is passed back in order to debug.</span></span>

<span data-ttu-id="d95a6-146">**Vertexshaderfile**</span><span class="sxs-lookup"><span data-stu-id="d95a6-146">**VertexShaderFile**</span></span>  
<span data-ttu-id="d95a6-147">Eine com-Zeichenfolge, die den filePath der Vertex-Shader-Quelldatei enthält.</span><span class="sxs-lookup"><span data-stu-id="d95a6-147">A COM string containing the filepath of the vertex shader source file.</span></span>

<span data-ttu-id="d95a6-148">**Pixelshaderfile**</span><span class="sxs-lookup"><span data-stu-id="d95a6-148">**PixelShaderFile**</span></span>  
<span data-ttu-id="d95a6-149">Eine com-Zeichenfolge, die den filePath der Pixelshader-Quelldatei enthält.</span><span class="sxs-lookup"><span data-stu-id="d95a6-149">A COM string containing the filepath of the pixel shader source file.</span></span>

<span data-ttu-id="d95a6-150">**Geometryshaderfile**</span><span class="sxs-lookup"><span data-stu-id="d95a6-150">**GeometryShaderFile**</span></span>  
<span data-ttu-id="d95a6-151">Eine com-Zeichenfolge, die den filePath der Geometry-Shader-Quelldatei enthält.</span><span class="sxs-lookup"><span data-stu-id="d95a6-151">A COM string containing the filepath of the geometry shader source file.</span></span>

<span data-ttu-id="d95a6-152">**Hullshaderfile**</span><span class="sxs-lookup"><span data-stu-id="d95a6-152">**HullShaderFile**</span></span>  
<span data-ttu-id="d95a6-153">Eine com-Zeichenfolge, die den filePath der Hull-Shader-Quelldatei enthält.</span><span class="sxs-lookup"><span data-stu-id="d95a6-153">A COM string containing the filepath of the hull shader source file.</span></span>

<span data-ttu-id="d95a6-154">**Domainshaderfile**</span><span class="sxs-lookup"><span data-stu-id="d95a6-154">**DomainShaderFile**</span></span>  
<span data-ttu-id="d95a6-155">Eine com-Zeichenfolge, die den filePath der Domänen-Shader-Quelldatei enthält.</span><span class="sxs-lookup"><span data-stu-id="d95a6-155">A COM string containing the filepath of the domain shader source file.</span></span>

<span data-ttu-id="d95a6-156">**psred**</span><span class="sxs-lookup"><span data-stu-id="d95a6-156">**psRed**</span></span>  
<span data-ttu-id="d95a6-157">Pixel-Shader-Ausgabe: Wert der roten Farbkomponente.</span><span class="sxs-lookup"><span data-stu-id="d95a6-157">Pixel shader output: value of red color component.</span></span>

<span data-ttu-id="d95a6-158">**psgrün**</span><span class="sxs-lookup"><span data-stu-id="d95a6-158">**psGreen**</span></span>  
<span data-ttu-id="d95a6-159">Pixel-Shader-Ausgabe: Wert der grünen Farbkomponente.</span><span class="sxs-lookup"><span data-stu-id="d95a6-159">Pixel shader output: value of green color component.</span></span>

<span data-ttu-id="d95a6-160">**psblue**</span><span class="sxs-lookup"><span data-stu-id="d95a6-160">**psBlue**</span></span>  
<span data-ttu-id="d95a6-161">Pixel-Shader-Ausgabe: Wert der blauen Farbkomponente</span><span class="sxs-lookup"><span data-stu-id="d95a6-161">Pixel shader output: value of blue color component</span></span>

<span data-ttu-id="d95a6-162">**psalpha**</span><span class="sxs-lookup"><span data-stu-id="d95a6-162">**psAlpha**</span></span>  
<span data-ttu-id="d95a6-163">Pixel-Shader-Ausgabe: Wert der Alpha Farbkomponente</span><span class="sxs-lookup"><span data-stu-id="d95a6-163">Pixel shader output: value of alpha color component</span></span>

<span data-ttu-id="d95a6-164">**Labelpsred**</span><span class="sxs-lookup"><span data-stu-id="d95a6-164">**LabelPSRed**</span></span>  
<span data-ttu-id="d95a6-165">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der Komponente der roten Farbe der Pixel-Shader-Ausgabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d95a6-165">A COM string containing the name of the label associated with the red color component of the pixel shader output.</span></span>

<span data-ttu-id="d95a6-166">**Labelpsgreen**</span><span class="sxs-lookup"><span data-stu-id="d95a6-166">**LabelPSGreen**</span></span>  
<span data-ttu-id="d95a6-167">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der grünen Farbkomponente der Pixel-Shader-Ausgabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d95a6-167">A COM string containing the name of the label associated with the green color component of the pixel shader output.</span></span>

<span data-ttu-id="d95a6-168">**Labelpsblue**</span><span class="sxs-lookup"><span data-stu-id="d95a6-168">**LabelPSBlue**</span></span>  
<span data-ttu-id="d95a6-169">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der blauen Farbkomponente der Pixel-Shader-Ausgabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d95a6-169">A COM string containing the name of the label associated with the blue color component of the pixel shader output.</span></span>

<span data-ttu-id="d95a6-170">**Labelpsalpha**</span><span class="sxs-lookup"><span data-stu-id="d95a6-170">**LabelPSAlpha**</span></span>  
<span data-ttu-id="d95a6-171">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der Alpha Farbkomponente der Pixel-Shader-Ausgabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d95a6-171">A COM string containing the name of the label associated with the alpha color component of the pixel shader output.</span></span>

<span data-ttu-id="d95a6-172">**pixelkillreason**</span><span class="sxs-lookup"><span data-stu-id="d95a6-172">**pixelKillReason**</span></span>  
<span data-ttu-id="d95a6-173">Pixel-Shader-Ausgabe: Grund, warum die Pixel Ausgabe abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="d95a6-173">Pixel shader output: reason the pixel output was killed.</span></span>

<span data-ttu-id="d95a6-174">**Pixel-okkluded**</span><span class="sxs-lookup"><span data-stu-id="d95a6-174">**pixelOccluded**</span></span>  
<span data-ttu-id="d95a6-175">true, wenn das Pixel ausgeblendet ist. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="d95a6-175">true if the pixel is occluded; otherwise, false.</span></span>

<span data-ttu-id="d95a6-176">**mit dem Namen**</span><span class="sxs-lookup"><span data-stu-id="d95a6-176">**fbRed**</span></span>  
<span data-ttu-id="d95a6-177">Frame Puffer: Wert der roten Farbkomponente von Frame Puffer, bevor die Pixel-Shader-Ausgabe zusammengeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d95a6-177">Framebuffer: value of red color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="d95a6-178">**bgrün**</span><span class="sxs-lookup"><span data-stu-id="d95a6-178">**fbGreen**</span></span>  
<span data-ttu-id="d95a6-179">Frame Puffer: Wert der grünen Farbkomponente von Frame Puffer, bevor die Pixel-Shader-Ausgabe zusammengeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d95a6-179">Framebuffer: value of green color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="d95a6-180">**"f"**</span><span class="sxs-lookup"><span data-stu-id="d95a6-180">**fbBlue**</span></span>  
<span data-ttu-id="d95a6-181">Frame Puffer: Wert der blauen Farbkomponente von Frame Puffer, bevor die Pixel-Shader-Ausgabe zusammengeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d95a6-181">Framebuffer: value of blue color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="d95a6-182">**"f"**</span><span class="sxs-lookup"><span data-stu-id="d95a6-182">**fbAlpha**</span></span>  
<span data-ttu-id="d95a6-183">Frame Puffer: Wert der Alpha Farbkomponente von Frame Puffer, bevor die Pixel-Shader-Ausgabe zusammengeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d95a6-183">Framebuffer: value of alpha color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="d95a6-184">**Labelfgezüchtet**</span><span class="sxs-lookup"><span data-stu-id="d95a6-184">**LabelFBRed**</span></span>  
<span data-ttu-id="d95a6-185">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der roten Farbkomponente des Framebuffer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d95a6-185">A COM string containing the name of the label associated with the red color component of the framebuffer.</span></span>

<span data-ttu-id="d95a6-186">**Labelfbgrün**</span><span class="sxs-lookup"><span data-stu-id="d95a6-186">**LabelFBGreen**</span></span>  
<span data-ttu-id="d95a6-187">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der grünen Farbkomponente des Framebuffer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d95a6-187">A COM string containing the name of the label associated with the green color component of the framebuffer.</span></span>

<span data-ttu-id="d95a6-188">**Labelfbblue**</span><span class="sxs-lookup"><span data-stu-id="d95a6-188">**LabelFBBlue**</span></span>  
<span data-ttu-id="d95a6-189">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der blauen Farbkomponente des Framebuffer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d95a6-189">A COM string containing the name of the label associated with the blue color component of the framebuffer.</span></span>

<span data-ttu-id="d95a6-190">**Labelfbalpha**</span><span class="sxs-lookup"><span data-stu-id="d95a6-190">**LabelFBAlpha**</span></span>  
<span data-ttu-id="d95a6-191">Eine com-Zeichenfolge mit dem Namen der Bezeichnung, die der Alpha Farbkomponente des Framebuffer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d95a6-191">A COM string containing the name of the label associated with the alpha color component of the framebuffer.</span></span>

<span data-ttu-id="d95a6-192">**Topologie**</span><span class="sxs-lookup"><span data-stu-id="d95a6-192">**topology**</span></span>  
<span data-ttu-id="d95a6-193">Die Vertex-Topologie der Draw-Aufrufe (Dreiecks Liste, Dreiecks Streifen usw.).</span><span class="sxs-lookup"><span data-stu-id="d95a6-193">The vertex topology of the draw calls (triangle list, triangle strip, etc).</span></span>

<span data-ttu-id="d95a6-194">**Vertices**</span><span class="sxs-lookup"><span data-stu-id="d95a6-194">**vertices**</span></span>  
<span data-ttu-id="d95a6-195">Eine com-Zeichenfolge, die den Scheitelpunkt Puffer enthält, beginnend bei diesem primitiven.</span><span class="sxs-lookup"><span data-stu-id="d95a6-195">A COM string containing the vertex buffer starting at this primitive.</span></span> <span data-ttu-id="d95a6-196">Der Vertex-Puffer folgt dem Eingabe Layout-Format, das in der Pipeline Stufe angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d95a6-196">The vertex buffer follows the input layout format specified in the pipeline stage.</span></span>

<span data-ttu-id="d95a6-197">**vertexsize**</span><span class="sxs-lookup"><span data-stu-id="d95a6-197">**vertexSize**</span></span>  
<span data-ttu-id="d95a6-198">Die Größe eines einzelnen Scheitel Punkts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d95a6-198">The size of a single vertex in bytes.</span></span>

<span data-ttu-id="d95a6-199">**Input Layout**</span><span class="sxs-lookup"><span data-stu-id="d95a6-199">**InputLayout**</span></span>  
<span data-ttu-id="d95a6-200">Eine com-Zeichenfolge, die eine Sequenz von inputlayoutstruct-Strukturen enthält, die dem Draw-Befehl zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d95a6-200">A COM string containing a sequence of InputLayoutStruct structures associated with the draw call.</span></span>

<span data-ttu-id="d95a6-201">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d95a6-201">**HResult**</span></span>  
<span data-ttu-id="d95a6-202">Das DirectX HRESULT.</span><span class="sxs-lookup"><span data-stu-id="d95a6-202">The DirectX Hresult.</span></span> <span data-ttu-id="d95a6-203">Im Fall eines Problems kann dies zum Anzeigen des Fehlers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d95a6-203">In the event of a problem this can be used to display the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d95a6-204">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d95a6-204">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d95a6-205">Header</span><span class="sxs-lookup"><span data-stu-id="d95a6-205">Header</span></span></p></td><td><span data-ttu-id="d95a6-206">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d95a6-206">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



