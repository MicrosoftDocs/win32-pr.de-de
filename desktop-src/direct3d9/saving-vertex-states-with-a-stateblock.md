---
description: Ein Zustands Block kann verwendet werden, um nur den Scheitelpunkt Zustand zu erfassen (siehe Status Blöcke speichern und Wiederherstellen (Direct3D 9)).
ms.assetid: cb898228-dc45-4a2a-a82e-8d64523e9b85
title: Speichern von Scheitelpunkt Zuständen mit einem stateblock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c6bc7fd291a2609ef60709f05a04fe8d27f8eb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342970"
---
# <a name="saving-vertex-states-with-a-stateblock-direct3d-9"></a><span data-ttu-id="90967-103">Speichern von Scheitelpunkt Zuständen mit einem stateblock (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="90967-103">Saving Vertex States With a StateBlock (Direct3D 9)</span></span>

<span data-ttu-id="90967-104">Ein Zustands Block kann verwendet werden, um nur den Scheitelpunkt Zustand zu erfassen (siehe [Status Blöcke speichern und Wiederherstellen (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="90967-104">A state block can be used to capture only vertex state (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span> <span data-ttu-id="90967-105">Der folgende Zustand ist der Scheitelpunkt Status:</span><span class="sxs-lookup"><span data-stu-id="90967-105">The following state is vertex state:</span></span>

-   <span data-ttu-id="90967-106">Vertex-Rendering-Zustand (siehe [vertexpipeline: Rendering State](#vertex-pipeline-render-state)).</span><span class="sxs-lookup"><span data-stu-id="90967-106">Vertex render state (see [Vertex Pipeline: Render State](#vertex-pipeline-render-state)).</span></span>
-   <span data-ttu-id="90967-107">Vertex-samplerstatus (siehe [Scheitelpunkt Pipeline: samplerzustand](#vertex-pipeline-sampler-state)).</span><span class="sxs-lookup"><span data-stu-id="90967-107">Vertex sampler state (see [Vertex Pipeline: Sampler State](#vertex-pipeline-sampler-state)).</span></span>
-   <span data-ttu-id="90967-108">Vertextexturzustand (siehe [vertexpipeline: Textur Zustand](#vertex-pipeline-texture-state)).</span><span class="sxs-lookup"><span data-stu-id="90967-108">Vertex texture state (see [Vertex Pipeline: Texture State](#vertex-pipeline-texture-state)).</span></span>
-   <span data-ttu-id="90967-109">Die npatchmodussegmente aus [**IDirect3DDevice9:: setnpatchmode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="90967-109">The NPatch mode segments from [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>
-   <span data-ttu-id="90967-110">Jedes Licht aus [**IDirect3DDevice9:: setlight**](/windows/desktop/api), und gibt an, ob das Licht mit [**IDirect3DDevice9:: lightenable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="90967-110">Each light from [**IDirect3DDevice9::SetLight**](/windows/desktop/api), as well as whether or not the light is enabled with [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>
-   <span data-ttu-id="90967-111">Der aktuelle Scheitelpunkt-Shader und jede der Vertex-shaderkonstanten.</span><span class="sxs-lookup"><span data-stu-id="90967-111">The current vertex shader and each of the vertex shader constants.</span></span>
-   <span data-ttu-id="90967-112">Speichern Sie für jeden Vertex-Stream den unter Teiler-Wert von [**IDirect3DDevice9:: setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span><span class="sxs-lookup"><span data-stu-id="90967-112">For each vertex stream, store the divider value from [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span></span>
-   <span data-ttu-id="90967-113">Die aktuelle Scheitelpunkt Deklaration.</span><span class="sxs-lookup"><span data-stu-id="90967-113">The current vertex declaration.</span></span>

<span data-ttu-id="90967-114">Um den Scheitelpunkt Zustand mit einem Zustands Block zu erfassen, geben Sie D3DSBT \_ vertexstate beim Aufrufen von [**IDirect3DDevice9:: createstateblock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)an.</span><span class="sxs-lookup"><span data-stu-id="90967-114">To capture vertex state with a state block, specify D3DSBT\_VERTEXSTATE when calling [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span></span>

## <a name="vertex-pipeline-render-state"></a><span data-ttu-id="90967-115">Scheitelpunkt Pipeline: Rendering-Status</span><span class="sxs-lookup"><span data-stu-id="90967-115">Vertex Pipeline: Render State</span></span>

<span data-ttu-id="90967-116">Renderzustände von Geräten wirken sich auf das Verhalten von fast jedem Teil der Pipeline aus.</span><span class="sxs-lookup"><span data-stu-id="90967-116">Device render states affect the behavior of almost every part of the pipeline.</span></span> <span data-ttu-id="90967-117">Renderzustände werden durch Aufrufen von [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90967-117">Render states are set by calling [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span>

<span data-ttu-id="90967-118">In der folgenden Tabelle sind alle Rendering-Zustände enthalten, die den Scheitelpunkt Status einrichten:</span><span class="sxs-lookup"><span data-stu-id="90967-118">The following table includes all render states that set-up vertex state:</span></span>



| <span data-ttu-id="90967-119">Rendering-Zustände</span><span class="sxs-lookup"><span data-stu-id="90967-119">Render States</span></span>                           | <span data-ttu-id="90967-120">Standardwert</span><span class="sxs-lookup"><span data-stu-id="90967-120">Default Value</span></span>          |
|-----------------------------------------|------------------------|
| <span data-ttu-id="90967-121">D3DRS \_ CullMode</span><span class="sxs-lookup"><span data-stu-id="90967-121">D3DRS\_CULLMODE</span></span>                         | <span data-ttu-id="90967-122">D3DCULL \_ CCW</span><span class="sxs-lookup"><span data-stu-id="90967-122">D3DCULL\_CCW</span></span>           |
| <span data-ttu-id="90967-123">D3DRS \_ fogcolor</span><span class="sxs-lookup"><span data-stu-id="90967-123">D3DRS\_FOGCOLOR</span></span>                         | <span data-ttu-id="90967-124">0</span><span class="sxs-lookup"><span data-stu-id="90967-124">0</span></span>                      |
| <span data-ttu-id="90967-125">D3DRS \_ fogtablemode</span><span class="sxs-lookup"><span data-stu-id="90967-125">D3DRS\_FOGTABLEMODE</span></span>                     | <span data-ttu-id="90967-126">D3DFOG \_ None</span><span class="sxs-lookup"><span data-stu-id="90967-126">D3DFOG\_NONE</span></span>           |
| <span data-ttu-id="90967-127">D3DRS \_ fogstart</span><span class="sxs-lookup"><span data-stu-id="90967-127">D3DRS\_FOGSTART</span></span>                         | <span data-ttu-id="90967-128">0</span><span class="sxs-lookup"><span data-stu-id="90967-128">0</span></span>                      |
| <span data-ttu-id="90967-129">D3DRS \_ fogend</span><span class="sxs-lookup"><span data-stu-id="90967-129">D3DRS\_FOGEND</span></span>                           | <span data-ttu-id="90967-130">1</span><span class="sxs-lookup"><span data-stu-id="90967-130">1</span></span>                      |
| <span data-ttu-id="90967-131">D3DRS- \_ fogdensity</span><span class="sxs-lookup"><span data-stu-id="90967-131">D3DRS\_FOGDENSITY</span></span>                       | <span data-ttu-id="90967-132">1</span><span class="sxs-lookup"><span data-stu-id="90967-132">1</span></span>                      |
| <span data-ttu-id="90967-133">D3DRS \_ RANGEFOGENABLE</span><span class="sxs-lookup"><span data-stu-id="90967-133">D3DRS\_RANGEFOGENABLE</span></span>                   | <span data-ttu-id="90967-134">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="90967-134">**FALSE**</span></span>              |
| <span data-ttu-id="90967-135">D3DRS \_ AMBIENT</span><span class="sxs-lookup"><span data-stu-id="90967-135">D3DRS\_AMBIENT</span></span>                          | <span data-ttu-id="90967-136">0</span><span class="sxs-lookup"><span data-stu-id="90967-136">0</span></span>                      |
| <span data-ttu-id="90967-137">D3DRS \_ ColorVertex</span><span class="sxs-lookup"><span data-stu-id="90967-137">D3DRS\_COLORVERTEX</span></span>                      | <span data-ttu-id="90967-138">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="90967-138">**TRUE**</span></span>               |
| <span data-ttu-id="90967-139">D3DRS \_ fogvertexmode</span><span class="sxs-lookup"><span data-stu-id="90967-139">D3DRS\_FOGVERTEXMODE</span></span>                    | <span data-ttu-id="90967-140">D3DFOG \_ None</span><span class="sxs-lookup"><span data-stu-id="90967-140">D3DFOG\_NONE</span></span>           |
| <span data-ttu-id="90967-141">D3DRS \_ Clipping</span><span class="sxs-lookup"><span data-stu-id="90967-141">D3DRS\_CLIPPING</span></span>                         | <span data-ttu-id="90967-142">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="90967-142">**TRUE**</span></span>               |
| <span data-ttu-id="90967-143">D3DRS- \_ Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="90967-143">D3DRS\_LIGHTING</span></span>                         | <span data-ttu-id="90967-144">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="90967-144">**TRUE**</span></span>               |
| <span data-ttu-id="90967-145">D3DRS \_ localviewer</span><span class="sxs-lookup"><span data-stu-id="90967-145">D3DRS\_LOCALVIEWER</span></span>                      | <span data-ttu-id="90967-146">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="90967-146">**TRUE**</span></span>               |
| <span data-ttu-id="90967-147">D3DRS \_ emissivematerialsource</span><span class="sxs-lookup"><span data-stu-id="90967-147">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>           | <span data-ttu-id="90967-148">D3DMCS \_ Material</span><span class="sxs-lookup"><span data-stu-id="90967-148">D3DMCS\_MATERIAL</span></span>       |
| <span data-ttu-id="90967-149">D3DRS \_ AmbientMaterialSource</span><span class="sxs-lookup"><span data-stu-id="90967-149">D3DRS\_AMBIENTMATERIALSOURCE</span></span>            | <span data-ttu-id="90967-150">D3DMCS \_ Material</span><span class="sxs-lookup"><span data-stu-id="90967-150">D3DMCS\_MATERIAL</span></span>       |
| <span data-ttu-id="90967-151">D3DRS \_ DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="90967-151">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>            | <span data-ttu-id="90967-152">D3DMCS \_ COLOR1</span><span class="sxs-lookup"><span data-stu-id="90967-152">D3DMCS\_COLOR1</span></span>         |
| <span data-ttu-id="90967-153">D3DRS \_ SpecularMaterialSource</span><span class="sxs-lookup"><span data-stu-id="90967-153">D3DRS\_SPECULARMATERIALSOURCE</span></span>           | <span data-ttu-id="90967-154">D3DMCS \_ COLOR2</span><span class="sxs-lookup"><span data-stu-id="90967-154">D3DMCS\_COLOR2</span></span>         |
| <span data-ttu-id="90967-155">D3DRS \_ vertexblend</span><span class="sxs-lookup"><span data-stu-id="90967-155">D3DRS\_VERTEXBLEND</span></span>                      | <span data-ttu-id="90967-156">D3DVBF \_ Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="90967-156">D3DVBF\_DISABLE</span></span>        |
| <span data-ttu-id="90967-157">D3DRS \_ clipplaneenable</span><span class="sxs-lookup"><span data-stu-id="90967-157">D3DRS\_CLIPPLANEENABLE</span></span>                  | <span data-ttu-id="90967-158">0</span><span class="sxs-lookup"><span data-stu-id="90967-158">0</span></span>                      |
| <span data-ttu-id="90967-159">D3DRS \_ pointsize</span><span class="sxs-lookup"><span data-stu-id="90967-159">D3DRS\_POINTSIZE</span></span>                        | <span data-ttu-id="90967-160">Treiber abhängig</span><span class="sxs-lookup"><span data-stu-id="90967-160">Driver dependent</span></span>       |
| <span data-ttu-id="90967-161">D3DRS \_ pointsize \_ Min</span><span class="sxs-lookup"><span data-stu-id="90967-161">D3DRS\_POINTSIZE\_MIN</span></span>                   | <span data-ttu-id="90967-162">1</span><span class="sxs-lookup"><span data-stu-id="90967-162">1</span></span>                      |
| <span data-ttu-id="90967-163">D3DRS \_ pointspriteenable</span><span class="sxs-lookup"><span data-stu-id="90967-163">D3DRS\_POINTSPRITEENABLE</span></span>                | <span data-ttu-id="90967-164">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="90967-164">**FALSE**</span></span>              |
| <span data-ttu-id="90967-165">D3DRS \_ pointscaleenable</span><span class="sxs-lookup"><span data-stu-id="90967-165">D3DRS\_POINTSCALEENABLE</span></span>                 | <span data-ttu-id="90967-166">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="90967-166">**FALSE**</span></span>              |
| <span data-ttu-id="90967-167">D3DRS \_ pointscale \_ A</span><span class="sxs-lookup"><span data-stu-id="90967-167">D3DRS\_POINTSCALE\_A</span></span>                    | <span data-ttu-id="90967-168">1</span><span class="sxs-lookup"><span data-stu-id="90967-168">1</span></span>                      |
| <span data-ttu-id="90967-169">D3DRS \_ pointscale \_ B</span><span class="sxs-lookup"><span data-stu-id="90967-169">D3DRS\_POINTSCALE\_B</span></span>                    | <span data-ttu-id="90967-170">0</span><span class="sxs-lookup"><span data-stu-id="90967-170">0</span></span>                      |
| <span data-ttu-id="90967-171">D3DRS \_ pointscale \_ C</span><span class="sxs-lookup"><span data-stu-id="90967-171">D3DRS\_POINTSCALE\_C</span></span>                    | <span data-ttu-id="90967-172">0</span><span class="sxs-lookup"><span data-stu-id="90967-172">0</span></span>                      |
| <span data-ttu-id="90967-173">D3DRS \_ multisampleantialias</span><span class="sxs-lookup"><span data-stu-id="90967-173">D3DRS\_MULTISAMPLEANTIALIAS</span></span>             | <span data-ttu-id="90967-174">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="90967-174">**TRUE**</span></span>               |
| <span data-ttu-id="90967-175">D3DRS \_ multisamplemask</span><span class="sxs-lookup"><span data-stu-id="90967-175">D3DRS\_MULTISAMPLEMASK</span></span>                  | <span data-ttu-id="90967-176">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="90967-176">0xffffffff</span></span>             |
| <span data-ttu-id="90967-177">D3DRS \_ patchedgestyle</span><span class="sxs-lookup"><span data-stu-id="90967-177">D3DRS\_PATCHEDGESTYLE</span></span>                   | <span data-ttu-id="90967-178">D3DPATCHEDGE \_ diskret</span><span class="sxs-lookup"><span data-stu-id="90967-178">D3DPATCHEDGE\_DISCRETE</span></span> |
| <span data-ttu-id="90967-179">D3DRS \_ pointsize \_ Max</span><span class="sxs-lookup"><span data-stu-id="90967-179">D3DRS\_POINTSIZE\_MAX</span></span>                   | <span data-ttu-id="90967-180">1</span><span class="sxs-lookup"><span data-stu-id="90967-180">1</span></span>                      |
| <span data-ttu-id="90967-181">D3DRS \_ indexedvertexblendenable</span><span class="sxs-lookup"><span data-stu-id="90967-181">D3DRS\_INDEXEDVERTEXBLENDENABLE</span></span>         | <span data-ttu-id="90967-182">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="90967-182">**FALSE**</span></span>              |
| <span data-ttu-id="90967-183">D3DRS \_ tweumfactor</span><span class="sxs-lookup"><span data-stu-id="90967-183">D3DRS\_TWEENFACTOR</span></span>                      | <span data-ttu-id="90967-184">0</span><span class="sxs-lookup"><span data-stu-id="90967-184">0</span></span>                      |
| <span data-ttu-id="90967-185">D3DRS \_ positiondegree</span><span class="sxs-lookup"><span data-stu-id="90967-185">D3DRS\_POSITIONDEGREE</span></span>                   | <span data-ttu-id="90967-186">D3DDEGREE \_ kubisch</span><span class="sxs-lookup"><span data-stu-id="90967-186">D3DDEGREE\_CUBIC</span></span>       |
| <span data-ttu-id="90967-187">D3DRS \_ normaldegree</span><span class="sxs-lookup"><span data-stu-id="90967-187">D3DRS\_NORMALDEGREE</span></span>                     | <span data-ttu-id="90967-188">D3DDEGREE \_ linear</span><span class="sxs-lookup"><span data-stu-id="90967-188">D3DDEGREE\_LINEAR</span></span>      |
| <span data-ttu-id="90967-189">D3DRS \_ mintmeellationlevel</span><span class="sxs-lookup"><span data-stu-id="90967-189">D3DRS\_MINTESSELLATIONLEVEL</span></span>             | <span data-ttu-id="90967-190">1</span><span class="sxs-lookup"><span data-stu-id="90967-190">1</span></span>                      |
| <span data-ttu-id="90967-191">D3DRS \_ maxtmeellationlevel</span><span class="sxs-lookup"><span data-stu-id="90967-191">D3DRS\_MAXTESSELLATIONLEVEL</span></span>             | <span data-ttu-id="90967-192">1</span><span class="sxs-lookup"><span data-stu-id="90967-192">1</span></span>                      |
| <span data-ttu-id="90967-193">D3DRS \_ adaptivetess \_ X</span><span class="sxs-lookup"><span data-stu-id="90967-193">D3DRS\_ADAPTIVETESS\_X</span></span>                  | <span data-ttu-id="90967-194">0</span><span class="sxs-lookup"><span data-stu-id="90967-194">0</span></span>                      |
| <span data-ttu-id="90967-195">D3DRS \_ adaptivetess \_ Y</span><span class="sxs-lookup"><span data-stu-id="90967-195">D3DRS\_ADAPTIVETESS\_Y</span></span>                  | <span data-ttu-id="90967-196">0</span><span class="sxs-lookup"><span data-stu-id="90967-196">0</span></span>                      |
| <span data-ttu-id="90967-197">D3DRS \_ adaptivetess \_ Z</span><span class="sxs-lookup"><span data-stu-id="90967-197">D3DRS\_ADAPTIVETESS\_Z</span></span>                  | <span data-ttu-id="90967-198">1</span><span class="sxs-lookup"><span data-stu-id="90967-198">1</span></span>                      |
| <span data-ttu-id="90967-199">D3DRS \_ adaptivetess \_ W</span><span class="sxs-lookup"><span data-stu-id="90967-199">D3DRS\_ADAPTIVETESS\_W</span></span>                  | <span data-ttu-id="90967-200">0</span><span class="sxs-lookup"><span data-stu-id="90967-200">0</span></span>                      |
| <span data-ttu-id="90967-201">D3DRS \_ enableadaptivetess-"/></span><span class="sxs-lookup"><span data-stu-id="90967-201">D3DRS\_ENABLEADAPTIVETESSELLATION"/></span></span> | <span data-ttu-id="90967-202">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="90967-202">**FALSE**</span></span>              |



 

## <a name="vertex-pipeline-sampler-state"></a><span data-ttu-id="90967-203">Scheitelpunkt Pipeline: samplerstatus</span><span class="sxs-lookup"><span data-stu-id="90967-203">Vertex Pipeline: Sampler State</span></span>

<span data-ttu-id="90967-204">Samplerzustände Steuern samplingbezogene Themen, wie z. b. das Filtern, das ticken und den textemodi</span><span class="sxs-lookup"><span data-stu-id="90967-204">Sampler states control sampling related topics such as filtering, tiling, and texture coordinate address modes.</span></span> <span data-ttu-id="90967-205">Verwenden Sie [**IDirect3DDevice9:: setsamplerstate, um den samplerzustand**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) einzurichten (einschließlich der in der Mosaik Einheit zum Beispiel für Verschiebungs Zuordnungen verwendeten).</span><span class="sxs-lookup"><span data-stu-id="90967-205">Use [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) to set up the sampler state (including the one used in the tessellator unit to sample displacement maps).</span></span> <span data-ttu-id="90967-206">Die samplerzustände wurden mit dem \_ Präfix "D3DSAMP" umbenannt, um die Kompilierzeit-Fehlererkennung beim Portieren aus DirectX 8 zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="90967-206">The sampler states have been renamed with a "D3DSAMP\_" prefix to enable compile time error detection when porting from DirectX 8.</span></span>

<span data-ttu-id="90967-207">In der folgenden Tabelle sind alle samplerzustände enthalten, die den Scheitelpunkt Status einrichten:</span><span class="sxs-lookup"><span data-stu-id="90967-207">The following table includes all sampler states that set-up vertex state:</span></span>



| <span data-ttu-id="90967-208">Samplerzustände</span><span class="sxs-lookup"><span data-stu-id="90967-208">Sampler States</span></span>      | <span data-ttu-id="90967-209">Standardwert</span><span class="sxs-lookup"><span data-stu-id="90967-209">Default Value</span></span> |
|---------------------|---------------|
| <span data-ttu-id="90967-210">D3DSAMP \_ dmapoffset</span><span class="sxs-lookup"><span data-stu-id="90967-210">D3DSAMP\_DMAPOFFSET</span></span> | <span data-ttu-id="90967-211">256</span><span class="sxs-lookup"><span data-stu-id="90967-211">256</span></span>           |



 

## <a name="vertex-pipeline-texture-state"></a><span data-ttu-id="90967-212">Scheitelpunkt Pipeline: Textur Zustand</span><span class="sxs-lookup"><span data-stu-id="90967-212">Vertex Pipeline: Texture State</span></span>

<span data-ttu-id="90967-213">Textur Zustände steuern Textur Mischungs Vorgänge des Multitextur-Blender.</span><span class="sxs-lookup"><span data-stu-id="90967-213">Texture states control texture blending operations of the multi-texture blender.</span></span> <span data-ttu-id="90967-214">Verwenden Sie [**IDirect3DDevice9:: settexturestagestate**](/windows/desktop/api) zum Einrichten von Textur Zuständen.</span><span class="sxs-lookup"><span data-stu-id="90967-214">Use [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api) to set-up texture states.</span></span> <span data-ttu-id="90967-215">Verwenden Sie [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) , um eine Textur einer Samplingphase zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="90967-215">Use [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) to associate a texture with a sampler stage.</span></span>

<span data-ttu-id="90967-216">In der folgenden Tabelle sind alle Textur Zustände enthalten, die den Scheitelpunkt Status einrichten:</span><span class="sxs-lookup"><span data-stu-id="90967-216">The following table includes all the texture states that set-up vertex state:</span></span>



| <span data-ttu-id="90967-217">Textur Zustände</span><span class="sxs-lookup"><span data-stu-id="90967-217">Texture States</span></span>                | <span data-ttu-id="90967-218">Standardwert</span><span class="sxs-lookup"><span data-stu-id="90967-218">Default Value</span></span>    |
|-------------------------------|------------------|
| <span data-ttu-id="90967-219">D3DTSS \_ texcoordindex</span><span class="sxs-lookup"><span data-stu-id="90967-219">D3DTSS\_TEXCOORDINDEX</span></span>         | <span data-ttu-id="90967-220">0</span><span class="sxs-lookup"><span data-stu-id="90967-220">0</span></span>                |
| <span data-ttu-id="90967-221">D3DTSS \_ texturetransformflags</span><span class="sxs-lookup"><span data-stu-id="90967-221">D3DTSS\_TEXTURETRANSFORMFLAGS</span></span> | <span data-ttu-id="90967-222">D3DTTFF \_ Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="90967-222">D3DTTFF\_DISABLE</span></span> |



 

<span data-ttu-id="90967-223">D3DTSS \_ texcoordindex ist ein Status der Vertex-Verarbeitung fester Funktionen.</span><span class="sxs-lookup"><span data-stu-id="90967-223">D3DTSS\_TEXCOORDINDEX is a fixed function vertex processing state.</span></span> <span data-ttu-id="90967-224">Wenn ein programmierbarer Vertex-Shader verwendet wird, wird dieser Zustand ignoriert.</span><span class="sxs-lookup"><span data-stu-id="90967-224">If a programmable vertex shader is used, this state is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90967-225">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90967-225">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90967-226">Status Blöcke speichern und Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="90967-226">State Blocks Save and Restore State</span></span>](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
