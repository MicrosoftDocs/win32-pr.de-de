---
title: Indirektes zeichnen und GPU-culult
description: Das D3D12ExecuteIndirect-Beispiel veranschaulicht, wie indirekte Befehle zum Zeichnen von Inhalten verwendet werden. Außerdem wird veranschaulicht, wie diese Befehle auf der GPU in einem Compute-Shader bearbeitet werden können, bevor Sie ausgegeben werden.
ms.assetid: 09F90837-D6BF-498E-8018-5C28EDD9BDC3
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b016170fbd3b675d5d5a20c1de87f24b04d4804
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548651"
---
# <a name="indirect-drawing-and-gpu-culling"></a><span data-ttu-id="3301b-104">Indirektes zeichnen und GPU-culult</span><span class="sxs-lookup"><span data-stu-id="3301b-104">Indirect drawing and GPU culling</span></span>

<span data-ttu-id="3301b-105">Das D3D12ExecuteIndirect-Beispiel veranschaulicht, wie indirekte Befehle zum Zeichnen von Inhalten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3301b-105">The D3D12ExecuteIndirect sample demonstrates how to use indirect commands to draw content.</span></span> <span data-ttu-id="3301b-106">Außerdem wird veranschaulicht, wie diese Befehle auf der GPU in einem Compute-Shader bearbeitet werden können, bevor Sie ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3301b-106">It also demonstrates how these commands can be manipulated on the GPU in a compute shader before they are issued.</span></span>

-   [<span data-ttu-id="3301b-107">Definieren der indirekten Befehle</span><span class="sxs-lookup"><span data-stu-id="3301b-107">Define the indirect commands</span></span>](#define-the-indirect-commands)
-   [<span data-ttu-id="3301b-108">Erstellen einer Grafik und einer COMPUTE-Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="3301b-108">Create a graphics and compute root signature</span></span>](#create-a-graphics-and-compute-root-signature)
-   [<span data-ttu-id="3301b-109">Erstellen einer Shader-Ressourcen Ansicht (SRV) für den Compute-Shader</span><span class="sxs-lookup"><span data-stu-id="3301b-109">Create a shader resource view (SRV) for the compute shader</span></span>](#create-a-shader-resource-view-srv-for-the-compute-shader)
-   [<span data-ttu-id="3301b-110">Erstellen der indirekten Befehls Puffer</span><span class="sxs-lookup"><span data-stu-id="3301b-110">Create the indirect command buffers</span></span>](#create-the-indirect-command-buffers)
-   [<span data-ttu-id="3301b-111">Erstellen der COMPUTE-UAVs</span><span class="sxs-lookup"><span data-stu-id="3301b-111">Create the compute UAVs</span></span>](#create-the-compute-uavs)
-   [<span data-ttu-id="3301b-112">Zeichnen des Frames</span><span class="sxs-lookup"><span data-stu-id="3301b-112">Drawing the frame</span></span>](#drawing-the-frame)
-   [<span data-ttu-id="3301b-113">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="3301b-113">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="3301b-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3301b-114">Related topics</span></span>](#related-topics)

<span data-ttu-id="3301b-115">Im Beispiel wird ein Befehls Puffer erstellt, in dem 1024 Draw-Aufrufe beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3301b-115">The sample creates a command buffer that describes 1024 draw calls.</span></span> <span data-ttu-id="3301b-116">Jeder zeichnen-Befehl rendert ein Dreieck mit einer zufälligen Farbe, Position und Geschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="3301b-116">Each draw call renders a triangle with a random color, position, and velocity.</span></span> <span data-ttu-id="3301b-117">Die Dreiecke werden endlos auf dem Bildschirm animiert.</span><span class="sxs-lookup"><span data-stu-id="3301b-117">The triangles animate endlessly across the screen.</span></span> <span data-ttu-id="3301b-118">In diesem Beispiel gibt es zwei Modi.</span><span class="sxs-lookup"><span data-stu-id="3301b-118">There are two modes in this sample.</span></span> <span data-ttu-id="3301b-119">Im ersten Modus überprüft ein Compute-Shader die indirekten Befehle und entscheidet, ob dieser Befehl einer unsortierten Zugriffs Ansicht (UAV) hinzugefügt werden soll, in der beschrieben wird, welche Befehle ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3301b-119">In the first mode, a compute shader inspects the indirect commands and decides whether or not to add that command to an unordered access view (UAV) describing which commands that should be executed.</span></span> <span data-ttu-id="3301b-120">Im zweiten Modus werden alle Befehle einfach ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3301b-120">In the second mode, all commands are simply executed.</span></span> <span data-ttu-id="3301b-121">Durch Drücken der Leertaste wird zwischen den Modi gewechselt.</span><span class="sxs-lookup"><span data-stu-id="3301b-121">Pressing the spacebar will toggle between modes.</span></span>

## <a name="define-the-indirect-commands"></a><span data-ttu-id="3301b-122">Definieren der indirekten Befehle</span><span class="sxs-lookup"><span data-stu-id="3301b-122">Define the indirect commands</span></span>

<span data-ttu-id="3301b-123">Wir beginnen damit, zu definieren, wie die indirekten Befehle aussehen sollten.</span><span class="sxs-lookup"><span data-stu-id="3301b-123">We start out by defining what the indirect commands should look like.</span></span> <span data-ttu-id="3301b-124">In diesem Beispiel werden die folgenden Befehle ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="3301b-124">In this sample the commands we want to execute are to:</span></span>

<dl> 1. <span data-ttu-id="3301b-125">Aktualisieren Sie die Konstante Puffer Ansicht (CBV).</span><span class="sxs-lookup"><span data-stu-id="3301b-125">Update the constant buffer view (CBV).</span></span>  
2. <span data-ttu-id="3301b-126">Zeichnen Sie das Dreieck.</span><span class="sxs-lookup"><span data-stu-id="3301b-126">Draw the triangle.</span></span>  
</dl>

<span data-ttu-id="3301b-127">Diese Zeichnungs Befehle werden durch die folgende Struktur in der **D3D12ExecuteIndirect** -Klassendefinition dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3301b-127">These drawing commands are represented by the following structure in the **D3D12ExecuteIndirect** class definition.</span></span> <span data-ttu-id="3301b-128">Befehle werden sequenziell in der Reihenfolge ausgeführt, in der Sie in dieser Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3301b-128">Commands are executed sequentially in the order they are defined in this structure.</span></span>

``` syntax
  
// Data structure to match the command signature used for ExecuteIndirect.
struct IndirectCommand
{
       D3D12_GPU_VIRTUAL_ADDRESS cbv;
       D3D12_DRAW_ARGUMENTS drawArguments;
};
```



| <span data-ttu-id="3301b-129">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="3301b-129">Call flow</span></span>                                              | <span data-ttu-id="3301b-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="3301b-130">Parameters</span></span> |
|--------------------------------------------------------|------------|
| <span data-ttu-id="3301b-131">D3D12 \_ GPU \_ Virtual \_ Address (einfach eine UINT64)</span><span class="sxs-lookup"><span data-stu-id="3301b-131">D3D12\_GPU\_VIRTUAL\_ADDRESS (simply a UINT64)</span></span>         |            |
| [<span data-ttu-id="3301b-132">**D3D12 \_ Zeichnen von \_ Argumenten**</span><span class="sxs-lookup"><span data-stu-id="3301b-132">**D3D12\_DRAW\_ARGUMENTS**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments) |            |



 

<span data-ttu-id="3301b-133">Um die Datenstruktur zu begleiten, wird auch eine Befehls Signatur erstellt, die die GPU anweist, wie die an die [**executeindirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) -API weiter gegebenen Daten interpretiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3301b-133">To accompany the data structure, a command signature is also created which instructs the GPU how to interpret the data passed in to the [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) API.</span></span> <span data-ttu-id="3301b-134">Dieser und der größte Teil des folgenden Codes werden der **loadassets** -Methode hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3301b-134">This, and the most of the following code, is added to the **LoadAssets** method.</span></span>

``` syntax
// Create the command signature used for indirect drawing.
{
       // Each command consists of a CBV update and a DrawInstanced call.
       D3D12_INDIRECT_ARGUMENT_DESC argumentDescs[2] = {};
       argumentDescs[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT_BUFFER_VIEW;
       argumentDescs[0].ConstantBufferView.RootParameterIndex = Cbv;
       argumentDescs[1].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW;

       D3D12_COMMAND_SIGNATURE_DESC commandSignatureDesc = {};
       commandSignatureDesc.pArgumentDescs = argumentDescs;
       commandSignatureDesc.NumArgumentDescs = _countof(argumentDescs);
       commandSignatureDesc.ByteStride = sizeof(IndirectCommand);

       ThrowIfFailed(m_device->CreateCommandSignature(&commandSignatureDesc, m_rootSignature.Get(), IID_PPV_ARGS(&m_commandSignature)));
}
```



| <span data-ttu-id="3301b-135">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="3301b-135">Call flow</span></span>                                                               | <span data-ttu-id="3301b-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="3301b-136">Parameters</span></span>                                                              |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="3301b-137">**D3D12 \_ indirektes \_ Argument \_ Entsc**</span><span class="sxs-lookup"><span data-stu-id="3301b-137">**D3D12\_INDIRECT\_ARGUMENT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) | [<span data-ttu-id="3301b-138">**D3D12 \_ indirekter \_ \_ Argumenttyp**</span><span class="sxs-lookup"><span data-stu-id="3301b-138">**D3D12\_INDIRECT\_ARGUMENT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type) |
| [<span data-ttu-id="3301b-139">**D3D12 \_ Befehls \_ Signatur \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="3301b-139">**D3D12\_COMMAND\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc) |                                                                         |
| [<span data-ttu-id="3301b-140">**"Kreatecommandsignature"**</span><span class="sxs-lookup"><span data-stu-id="3301b-140">**CreateCommandSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)   |                                                                         |



 

## <a name="create-a-graphics-and-compute-root-signature"></a><span data-ttu-id="3301b-141">Erstellen einer Grafik und einer COMPUTE-Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="3301b-141">Create a graphics and compute root signature</span></span>

<span data-ttu-id="3301b-142">Außerdem erstellen wir sowohl eine Grafik als auch eine COMPUTE-Stamm Signatur.</span><span class="sxs-lookup"><span data-stu-id="3301b-142">We also create both a graphics and a compute root signature.</span></span> <span data-ttu-id="3301b-143">Die Grafik Stamm Signatur definiert lediglich eine root CBV.</span><span class="sxs-lookup"><span data-stu-id="3301b-143">The graphics root signature just defines a root CBV.</span></span> <span data-ttu-id="3301b-144">Beachten Sie, dass wir den Index dieses Root-Parameters [**im \_ indirekten \_ Argument \_ DESC D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) (siehe oben) zuordnen, wenn die Befehls Signatur definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3301b-144">Note that we map the index of this root parameter in the [**D3D12\_INDIRECT\_ARGUMENT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) (shown above) when the command signature is defined.</span></span> <span data-ttu-id="3301b-145">Die computestammsignatur definiert Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3301b-145">The compute root signature defines:</span></span>

-   <span data-ttu-id="3301b-146">Eine gängige Deskriptortabelle mit drei Slots (zwei SRV und eine UAV):</span><span class="sxs-lookup"><span data-stu-id="3301b-146">A common descriptor table with three slots (two SRV’s and one UAV):</span></span>
    -   <span data-ttu-id="3301b-147">Ein SRV macht die Konstanten Puffer für den Compute-Shader verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3301b-147">One SRV exposes the constant buffers to the compute shader</span></span>
    -   <span data-ttu-id="3301b-148">Ein SRV macht den Befehls Puffer für den Compute-Shader verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3301b-148">One SRV exposes the command buffer to the compute shader</span></span>
    -   <span data-ttu-id="3301b-149">In der UAV speichert der COMPUTE-Shader die Befehle für die sichtbaren Dreiecke.</span><span class="sxs-lookup"><span data-stu-id="3301b-149">The UAV is where the compute shader saves the commands for the visible triangles</span></span>
-   <span data-ttu-id="3301b-150">Vier Stamm Konstanten:</span><span class="sxs-lookup"><span data-stu-id="3301b-150">Four root constants:</span></span>
    -   <span data-ttu-id="3301b-151">Halbe Breite einer Seite des Dreiecks</span><span class="sxs-lookup"><span data-stu-id="3301b-151">Half the width of one side of the triangle</span></span>
    -   <span data-ttu-id="3301b-152">Die z-Position der Dreieck Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="3301b-152">The z position of the triangle vertices</span></span>
    -   <span data-ttu-id="3301b-153">Der Offset +/-x der cullinger-Ebene im homogenen Raum \[ -1, 1\]</span><span class="sxs-lookup"><span data-stu-id="3301b-153">The +/- x offset of the culling plane in homogenous space \[-1,1\]</span></span>
    -   <span data-ttu-id="3301b-154">Die Anzahl der indirekten Befehle im Befehls Puffer.</span><span class="sxs-lookup"><span data-stu-id="3301b-154">The number of indirect commands in the command buffer</span></span>

``` syntax
// Create the root signatures.
{
       CD3DX12_ROOT_PARAMETER rootParameters[GraphicsRootParametersCount];
       rootParameters[Cbv].InitAsConstantBufferView(0, 0, D3D12_SHADER_VISIBILITY_VERTEX);

       CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
       rootSignatureDesc.Init(_countof(rootParameters), rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

       ComPtr<ID3DBlob> signature;
       ComPtr<ID3DBlob> error;
       ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
       ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));

       // Create compute signature.
       CD3DX12_DESCRIPTOR_RANGE ranges[2];
       ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 2, 0);
       ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_UAV, 1, 0);

       CD3DX12_ROOT_PARAMETER computeRootParameters[ComputeRootParametersCount];
       computeRootParameters[SrvUavTable].InitAsDescriptorTable(2, ranges);
       computeRootParameters[RootConstants].InitAsConstants(4, 0);

       CD3DX12_ROOT_SIGNATURE_DESC computeRootSignatureDesc;
       computeRootSignatureDesc.Init(_countof(computeRootParameters), computeRootParameters);

       ThrowIfFailed(D3D12SerializeRootSignature(&computeRootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
       ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_computeRootSignature)));
}
```



| <span data-ttu-id="3301b-155">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="3301b-155">Call flow</span></span>                                                             | <span data-ttu-id="3301b-156">Parameter</span><span class="sxs-lookup"><span data-stu-id="3301b-156">Parameters</span></span>                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="3301b-157">**CD3DX12 \_ root- \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="3301b-157">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="3301b-158">**D3D12- \_ Shader- \_ Sichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="3301b-158">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="3301b-159">**CD3DX12 \_ Stamm \_ Signatur \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="3301b-159">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="3301b-160">**D3D12 \_ root \_ Signature- \_ Flags**</span><span class="sxs-lookup"><span data-stu-id="3301b-160">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="3301b-161">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3301b-161">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="3301b-162">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="3301b-162">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="3301b-163">**D3D \_ Stamm \_ Signatur \_ Version**</span><span class="sxs-lookup"><span data-stu-id="3301b-163">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="3301b-164">**"Kreaterootsignature"**</span><span class="sxs-lookup"><span data-stu-id="3301b-164">**CreateRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [<span data-ttu-id="3301b-165">**CD3DX12- \_ \_ Deskriptorbereich**</span><span class="sxs-lookup"><span data-stu-id="3301b-165">**CD3DX12\_DESCRIPTOR\_RANGE**</span></span>](cd3dx12-descriptor-range.md)        | [<span data-ttu-id="3301b-166">**D3D12- \_ \_ deskriptorbereichstyp \_**</span><span class="sxs-lookup"><span data-stu-id="3301b-166">**D3D12\_DESCRIPTOR\_RANGE\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [<span data-ttu-id="3301b-167">**CD3DX12 \_ root- \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="3301b-167">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="3301b-168">**D3D12- \_ Shader- \_ Sichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="3301b-168">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="3301b-169">**CD3DX12 \_ Stamm \_ Signatur \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="3301b-169">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="3301b-170">**D3D12 \_ root \_ Signature- \_ Flags**</span><span class="sxs-lookup"><span data-stu-id="3301b-170">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="3301b-171">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3301b-171">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="3301b-172">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="3301b-172">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="3301b-173">**D3D \_ Stamm \_ Signatur \_ Version**</span><span class="sxs-lookup"><span data-stu-id="3301b-173">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="3301b-174">**"Kreaterootsignature"**</span><span class="sxs-lookup"><span data-stu-id="3301b-174">**CreateRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-a-shader-resource-view-srv-for-the-compute-shader"></a><span data-ttu-id="3301b-175">Erstellen einer Shader-Ressourcen Ansicht (SRV) für den Compute-Shader</span><span class="sxs-lookup"><span data-stu-id="3301b-175">Create a shader resource view (SRV) for the compute shader</span></span>

<span data-ttu-id="3301b-176">Nachdem Sie die Pipeline Zustands Objekte, Vertex-Puffer, eine tiefen Schablone und die Konstanten Puffer erstellt haben, erstellt das Beispiel eine Shader-Ressourcen Ansicht (SRV) des Konstanten Puffers, sodass der COMPUTE-Shader auf die Daten im Konstanten Puffer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="3301b-176">After creating the pipeline state objects, vertex buffers, a depth stencil, and the constant buffers, the sample then creates a shader resource view (SRV) of the constant buffer so that the compute shader can access the data in the constant buffer.</span></span>

``` syntax
// Create shader resource views (SRV) of the constant buffers for the
// compute shader to read from.
       D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
       srvDesc.Format = DXGI_FORMAT_UNKNOWN;
       srvDesc.ViewDimension = D3D12_SRV_DIMENSION_BUFFER;
       srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
       srvDesc.Buffer.NumElements = TriangleCount;
       srvDesc.Buffer.StructureByteStride = sizeof(ConstantBufferData);
       srvDesc.Buffer.Flags = D3D12_BUFFER_SRV_FLAG_NONE;

       CD3DX12_CPU_DESCRIPTOR_HANDLE cbvSrvHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), CbvSrvOffset, m_cbvSrvUavDescriptorSize);
       for (UINT frame = 0; frame < FrameCount; frame++)
       {
              srvDesc.Buffer.FirstElement = frame * TriangleCount;
              m_device->CreateShaderResourceView(m_constantBuffer.Get(), &srvDesc, cbvSrvHandle);
              cbvSrvHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
       }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3301b-177">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="3301b-177">Call flow</span></span></th>
<th><span data-ttu-id="3301b-178">Parameter</span><span class="sxs-lookup"><span data-stu-id="3301b-178">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3301b-179"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-179"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="3301b-180"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-180"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="3301b-181">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-181">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br /><span data-ttu-id="3301b-182">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="3301b-182">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3301b-183"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-183"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="3301b-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>Getcpudescriptor Lenker forheapstart</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>"Kreateshaderresourceview"</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="create-the-indirect-command-buffers"></a><span data-ttu-id="3301b-186">Erstellen der indirekten Befehls Puffer</span><span class="sxs-lookup"><span data-stu-id="3301b-186">Create the indirect command buffers</span></span>

<span data-ttu-id="3301b-187">Anschließend erstellen wir die indirekten Befehls Puffer und definieren ihren Inhalt mit dem folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="3301b-187">We then create the indirect command buffers and define their content using the following code.</span></span> <span data-ttu-id="3301b-188">Wir zeichnen die gleichen Dreiecks Scheitel Punkte 1024-mal, zeigen aber auf einen anderen Konstanten Puffer Speicherort mit jedem Zeichnen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="3301b-188">We draw the same triangle vertices 1024 times, but point to a different constant buffer location with each draw call.</span></span>

``` syntax
       D3D12_GPU_VIRTUAL_ADDRESS gpuAddress = m_constantBuffer->GetGPUVirtualAddress();
       UINT commandIndex = 0;

       for (UINT frame = 0; frame < FrameCount; frame++)
       {
              for (UINT n = 0; n < TriangleCount; n++)
              {
                    commands[commandIndex].cbv = gpuAddress;
                    commands[commandIndex].drawArguments.VertexCountPerInstance = 3;
                    commands[commandIndex].drawArguments.InstanceCount = 1;
                    commands[commandIndex].drawArguments.StartVertexLocation = 0;
                    commands[commandIndex].drawArguments.StartInstanceLocation = 0;

                    commandIndex++;
                    gpuAddress += sizeof(ConstantBufferData);
              }
       }
```



| <span data-ttu-id="3301b-189">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="3301b-189">Call flow</span></span>                    | <span data-ttu-id="3301b-190">Parameter</span><span class="sxs-lookup"><span data-stu-id="3301b-190">Parameters</span></span>                                                          |
|------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="3301b-191">\_Virtuelle GPU \_ - \_ Adresse D3D12</span><span class="sxs-lookup"><span data-stu-id="3301b-191">D3D12\_GPU\_VIRTUAL\_ADDRESS</span></span> | [<span data-ttu-id="3301b-192">**Getgpuvirtualaddress**</span><span class="sxs-lookup"><span data-stu-id="3301b-192">**GetGPUVirtualAddress**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress) |



 

<span data-ttu-id="3301b-193">Nachdem Sie die Befehls Puffer in die GPU hochgeladen haben, erstellen wir auch einen SRV, von dem aus der COMPUTE-Shader gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3301b-193">After uploading the command buffers to the GPU, we also create an SRV of them for the compute shader to read from.</span></span> <span data-ttu-id="3301b-194">Dies ähnelt dem SRV, das durch den konstanten Puffer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3301b-194">This is very similar to the SRV created of the constant buffer.</span></span>

``` syntax
// Create SRVs for the command buffers.
       D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
       srvDesc.Format = DXGI_FORMAT_UNKNOWN;
       srvDesc.ViewDimension = D3D12_SRV_DIMENSION_BUFFER;
       srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
       srvDesc.Buffer.NumElements = TriangleCount;
       srvDesc.Buffer.StructureByteStride = sizeof(IndirectCommand);
       srvDesc.Buffer.Flags = D3D12_BUFFER_SRV_FLAG_NONE;

       CD3DX12_CPU_DESCRIPTOR_HANDLE commandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), CommandsOffset, m_cbvSrvUavDescriptorSize);
       for (UINT frame = 0; frame < FrameCount; frame++)
       {
              srvDesc.Buffer.FirstElement = frame * TriangleCount;
              m_device->CreateShaderResourceView(m_commandBuffer.Get(), &srvDesc, commandsHandle);
              commandsHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
       }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3301b-195">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="3301b-195">Call flow</span></span></th>
<th><span data-ttu-id="3301b-196">Parameter</span><span class="sxs-lookup"><span data-stu-id="3301b-196">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3301b-197"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-197"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="3301b-198"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-198"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="3301b-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br /><span data-ttu-id="3301b-200">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="3301b-200">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br /><span data-ttu-id="3301b-201">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags"><strong>D3D12_BUFFER_SRV_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-201">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags"><strong>D3D12_BUFFER_SRV_FLAG</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3301b-202"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-202"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="3301b-203"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>Getcpudescriptor Lenker forheapstart</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-203"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-204"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>"Kreateshaderresourceview"</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-204"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="create-the-compute-uavs"></a><span data-ttu-id="3301b-205">Erstellen der COMPUTE-UAVs</span><span class="sxs-lookup"><span data-stu-id="3301b-205">Create the compute UAVs</span></span>

<span data-ttu-id="3301b-206">Wir müssen die UAVs erstellen, in denen die Ergebnisse der computearbeit gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3301b-206">We need to create the UAVs that will store the results of the compute work.</span></span> <span data-ttu-id="3301b-207">Wenn ein Dreieck vom Compute-Shader als sichtbar für das Renderziel angesehen wird, wird es an diese UAV angefügt und dann von der [**executeindirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) -API verwendet.</span><span class="sxs-lookup"><span data-stu-id="3301b-207">When a triangle is deemed by the compute shader to be visible to the render target, it will be appended to this UAV and then consumed by the [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) API.</span></span>

``` syntax
CD3DX12_CPU_DESCRIPTOR_HANDLE processedCommandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), ProcessedCommandsOffset, m_cbvSrvUavDescriptorSize);
for (UINT frame = 0; frame < FrameCount; frame++)
{
       // Allocate a buffer large enough to hold all of the indirect commands
       // for a single frame as well as a UAV counter.
       commandBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(CommandBufferSizePerFrame + sizeof(UINT), D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS);
       CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
       ThrowIfFailed(m_device->CreateCommittedResource(
             &heapProps,
             D3D12_HEAP_FLAG_NONE,
             &commandBufferDesc,
             D3D12_RESOURCE_STATE_COPY_DEST,
             nullptr,
             IID_PPV_ARGS(&m_processedCommandBuffers[frame])));

       D3D12_UNORDERED_ACCESS_VIEW_DESC uavDesc = {};
       uavDesc.Format = DXGI_FORMAT_UNKNOWN;
       uavDesc.ViewDimension = D3D12_UAV_DIMENSION_BUFFER;
       uavDesc.Buffer.FirstElement = 0;
       uavDesc.Buffer.NumElements = TriangleCount;
       uavDesc.Buffer.StructureByteStride = sizeof(IndirectCommand);
       uavDesc.Buffer.CounterOffsetInBytes = CommandBufferSizePerFrame;
       uavDesc.Buffer.Flags = D3D12_BUFFER_UAV_FLAG_NONE;

       m_device->CreateUnorderedAccessView(
             m_processedCommandBuffers[frame].Get(),
             m_processedCommandBuffers[frame].Get(),
             &uavDesc,
             processedCommandsHandle);

       processedCommandsHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
}
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3301b-208">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="3301b-208">Call flow</span></span></th>
<th><span data-ttu-id="3301b-209">Parameter</span><span class="sxs-lookup"><span data-stu-id="3301b-209">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3301b-210"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-210"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="3301b-211"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>Getcpudescriptor Lenker forheapstart</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-211"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3301b-212"><a href="cd3dx12-resource-desc.md"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-212"><a href="cd3dx12-resource-desc.md"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span></td>
<td><span data-ttu-id="3301b-213"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-213"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>"Kreatecommittedresource"</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="3301b-215"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-215"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="3301b-216">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-216">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="3301b-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="3301b-218">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-218">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3301b-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc"><strong>D3D12_UNORDERED_ACCESS_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc"><strong>D3D12_UNORDERED_ACCESS_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="3301b-220"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-220"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="3301b-221">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_uav_dimension"><strong>D3D12_UAV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-221">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_uav_dimension"><strong>D3D12_UAV_DIMENSION</strong></a></span></span><br /><span data-ttu-id="3301b-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags"><strong>D3D12_BUFFER_UAV_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags"><strong>D3D12_BUFFER_UAV_FLAGS</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview"><strong>"Kreateunorderedaccessview"</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview"><strong>CreateUnorderedAccessView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="drawing-the-frame"></a><span data-ttu-id="3301b-224">Zeichnen des Frames</span><span class="sxs-lookup"><span data-stu-id="3301b-224">Drawing the frame</span></span>

<span data-ttu-id="3301b-225">Wenn Sie den Frame zeichnen und sich im Modus befinden, wenn der COMPUTE-Shader aufgerufen wird und indirekte Befehle von der GPU verarbeitet werden, verteilen [**wir diese Aufgabe zunächst, um**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch) den Befehls Puffer für [**executeindirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="3301b-225">When it comes time to draw the frame, if we are in the mode when the compute shader is being invoked and indirect commands are being processed by the GPU, we will first [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch) that work to populate our command buffer for [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect).</span></span> <span data-ttu-id="3301b-226">Die folgenden Code Ausschnitte werden der Methode " **populatecommandlists** " hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3301b-226">The following code snippets are added to the **PopulateCommandLists** method.</span></span>

``` syntax
// Record the compute commands that will cull triangles and prevent them from being processed by the vertex shader.
if (m_enableCulling)
{
       UINT frameDescriptorOffset = m_frameIndex * CbvSrvUavDescriptorCountPerFrame;
       D3D12_GPU_DESCRIPTOR_HANDLE cbvSrvUavHandle = m_cbvSrvUavHeap->GetGPUDescriptorHandleForHeapStart();

       m_computeCommandList->SetComputeRootSignature(m_computeRootSignature.Get());

       ID3D12DescriptorHeap* ppHeaps[] = { m_cbvSrvUavHeap.Get() };
       m_computeCommandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

       m_computeCommandList->SetComputeRootDescriptorTable(
              SrvUavTable,
              CD3DX12_GPU_DESCRIPTOR_HANDLE(cbvSrvUavHandle, CbvSrvOffset + frameDescriptorOffset, m_cbvSrvUavDescriptorSize));

       m_computeCommandList->SetComputeRoot32BitConstants(RootConstants, 4, reinterpret_cast<void*>(&m_csRootConstants), 0);

       // Reset the UAV counter for this frame.
       m_computeCommandList->CopyBufferRegion(m_processedCommandBuffers[m_frameIndex].Get(), CommandBufferSizePerFrame, m_processedCommandBufferCounterReset.Get(), 0, sizeof(UINT));

       D3D12_RESOURCE_BARRIER barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_processedCommandBuffers[m_frameIndex].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_UNORDERED_ACCESS);
       m_computeCommandList->ResourceBarrier(1, &barrier);

       m_computeCommandList->Dispatch(static_cast<UINT>(ceil(TriangleCount / float(ComputeThreadBlockSize))), 1, 1);
}

ThrowIfFailed(m_computeCommandList->Close());
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3301b-227">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="3301b-227">Call flow</span></span></th>
<th><span data-ttu-id="3301b-228">Parameter</span><span class="sxs-lookup"><span data-stu-id="3301b-228">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3301b-229"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle"><strong>D3D12_GPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-229"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle"><strong>D3D12_GPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="3301b-230"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>Getgpudescriptor Lenker forheapstart</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-230"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3301b-231"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature"><strong>Setcomputerootsignature</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-231"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature"><strong>SetComputeRootSignature</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-232"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-232"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3301b-233"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>Setdescriptorheaps</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-233"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-234"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable"><strong>Setcomputerootdescriptor Table</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-234"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable"><strong>SetComputeRootDescriptorTable</strong></a></span></span></td>
<td><span data-ttu-id="3301b-235"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-235"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3301b-236"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants"><strong>SetComputeRoot32BitConstants</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-236"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants"><strong>SetComputeRoot32BitConstants</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-237"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion"><strong>Copybufferregion</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-237"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion"><strong>CopyBufferRegion</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3301b-238"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-238"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span></span></td>
<td><dl><span data-ttu-id="3301b-239"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-239"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="3301b-240">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-240">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-241"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>Resourcebarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-241"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3301b-242"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch"><strong>Dispatch</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-242"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch"><strong>Dispatch</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-243"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Schließen</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-243"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Close</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="3301b-244">Anschließend führen wir die Befehle entweder in der UAV (mit aktiviertem GPU-culch) oder im vollständigen Befehls Puffer aus (deaktivierte GPU-culch).</span><span class="sxs-lookup"><span data-stu-id="3301b-244">Then we will execute the commands in either the UAV (GPU culling enabled) or the full command buffer (GPU culling disabled).</span></span>

``` syntax
// Record the rendering commands.
{
       // Set necessary state.
       m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

       ID3D12DescriptorHeap* ppHeaps[] = { m_cbvSrvUavHeap.Get() };
       m_commandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

       m_commandList->RSSetViewports(1, &m_viewport);
       m_commandList->RSSetScissorRects(1, m_enableCulling ? &m_cullingScissorRect : &m_scissorRect);

       // Indicate that the command buffer will be used for indirect drawing
       // and that the back buffer will be used as a render target.
       D3D12_RESOURCE_BARRIER barriers[2] = {
              CD3DX12_RESOURCE_BARRIER::Transition(
                    m_enableCulling ? m_processedCommandBuffers[m_frameIndex].Get() : m_commandBuffer.Get(),
                    m_enableCulling ? D3D12_RESOURCE_STATE_UNORDERED_ACCESS : D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE,
                    D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT),
              CD3DX12_RESOURCE_BARRIER::Transition(
                    m_renderTargets[m_frameIndex].Get(),
                    D3D12_RESOURCE_STATE_PRESENT,
                    D3D12_RESOURCE_STATE_RENDER_TARGET)
       };

       m_commandList->ResourceBarrier(_countof(barriers), barriers);

       CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
       CD3DX12_CPU_DESCRIPTOR_HANDLE dsvHandle(m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
       m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, &dsvHandle);

       // Record commands.
       const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
       m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
       m_commandList->ClearDepthStencilView(dsvHandle, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

       m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP);
       m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);

       if (m_enableCulling)
       {
              // Draw the triangles that have not been culled.
              m_commandList->ExecuteIndirect(
                    m_commandSignature.Get(),
                    TriangleCount,
                    m_processedCommandBuffers[m_frameIndex].Get(),
                    0,
                    m_processedCommandBuffers[m_frameIndex].Get(),
                    CommandBufferSizePerFrame);
       }
       else
       {
              // Draw all of the triangles.
              m_commandList->ExecuteIndirect(
                    m_commandSignature.Get(),
                    TriangleCount,
                    m_commandBuffer.Get(),
                    CommandBufferSizePerFrame * m_frameIndex,
                    nullptr,
                    0);
       }

       // Indicate that the command buffer may be used by the compute shader
       // and that the back buffer will now be used to present.
       barriers[0].Transition.StateBefore = D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT;
       barriers[0].Transition.StateAfter = m_enableCulling ? D3D12_RESOURCE_STATE_COPY_DEST : D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE;
       barriers[1].Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
       barriers[1].Transition.StateAfter = D3D12_RESOURCE_STATE_PRESENT;

       m_commandList->ResourceBarrier(_countof(barriers), barriers);

       ThrowIfFailed(m_commandList->Close());
}
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3301b-245">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="3301b-245">Call flow</span></span></th>
<th><span data-ttu-id="3301b-246">Parameter</span><span class="sxs-lookup"><span data-stu-id="3301b-246">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3301b-247"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature"><strong>Setgraphicsrootsignature</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-247"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature"><strong>SetGraphicsRootSignature</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3301b-248"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-248"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-249"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>Setdescriptorheaps</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-249"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3301b-250"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports"><strong>Rssetviewports</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-250"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports"><strong>RSSetViewports</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-251"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects"><strong>Rssezcissorrects</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-251"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects"><strong>RSSetScissorRects</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3301b-252"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-252"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span></span></td>
<td><dl><span data-ttu-id="3301b-253"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-253"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="3301b-254">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-254">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-255"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>Resourcebarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-255"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3301b-256"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-256"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="3301b-257"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>Getcpudescriptor Lenker forheapstart</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-257"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-258"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets"><strong>Omantrendertargets</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-258"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets"><strong>OMSetRenderTargets</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3301b-259"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview"><strong>ClearRenderTargetView</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-259"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview"><strong>ClearRenderTargetView</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-260"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview"><strong>ClearDepthStencilView</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-260"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview"><strong>ClearDepthStencilView</strong></a></span></span></td>
<td><span data-ttu-id="3301b-261"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_clear_flags"><strong>D3D12_CLEAR_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-261"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_clear_flags"><strong>D3D12_CLEAR_FLAGS</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3301b-262"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>Iasetprimitivetopology</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-262"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span></span></td>
<td><span data-ttu-id="3301b-263"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-263"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-264"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>Iasetvertexbuffers</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-264"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3301b-265"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect"><strong>Executin Direct</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-265"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect"><strong>ExecuteIndirect</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3301b-266"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>Resourcebarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-266"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><span data-ttu-id="3301b-267"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-267"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3301b-268"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Schließen</strong></a></span><span class="sxs-lookup"><span data-stu-id="3301b-268"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Close</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="3301b-269">Wenn wir uns im GPU-culchmodus befinden, wird die Grafik Befehls Warteschlange gewartet, bis die computearbeit beendet ist, bevor die indirekten Befehle ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3301b-269">If we are in GPU culling mode, we will have the graphics command queue wait for the compute work to complete before it begins executing the indirect commands.</span></span> <span data-ttu-id="3301b-270">In der **onrendering** -Methode wird der folgende Code Ausschnitt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3301b-270">In the **OnRender** method the following snippet is added.</span></span>

``` syntax
// Execute the compute work.
if (m_enableCulling)
{
       ID3D12CommandList* ppCommandLists[] = { m_computeCommandList.Get() };
       m_computeCommandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);
       m_computeCommandQueue->Signal(m_computeFence.Get(), m_fenceValues[m_frameIndex]);

       // Execute the rendering work only when the compute work is complete.
       m_commandQueue->Wait(m_computeFence.Get(), m_fenceValues[m_frameIndex]);
}

// Execute the rendering work.
ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);
```



| <span data-ttu-id="3301b-271">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="3301b-271">Call flow</span></span>                                                             | <span data-ttu-id="3301b-272">Parameter</span><span class="sxs-lookup"><span data-stu-id="3301b-272">Parameters</span></span> |
|-----------------------------------------------------------------------|------------|
| [<span data-ttu-id="3301b-273">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="3301b-273">**ID3D12CommandList**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                        |            |
| [<span data-ttu-id="3301b-274">**Executecommandlists**</span><span class="sxs-lookup"><span data-stu-id="3301b-274">**ExecuteCommandLists**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) |            |
| [<span data-ttu-id="3301b-275">**Aussendet**</span><span class="sxs-lookup"><span data-stu-id="3301b-275">**Signal**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                           |            |
| [<span data-ttu-id="3301b-276">**Wait**</span><span class="sxs-lookup"><span data-stu-id="3301b-276">**Wait**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                               |            |
| [<span data-ttu-id="3301b-277">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="3301b-277">**ID3D12CommandList**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                        |            |
| [<span data-ttu-id="3301b-278">**Executecommandlists**</span><span class="sxs-lookup"><span data-stu-id="3301b-278">**ExecuteCommandLists**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) |            |



 

## <a name="run-the-sample"></a><span data-ttu-id="3301b-279">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="3301b-279">Run the sample</span></span>

<span data-ttu-id="3301b-280">Das Beispiel mit GPU-primitiver kulalisierung.</span><span class="sxs-lookup"><span data-stu-id="3301b-280">The sample with GPU primitive culling.</span></span>

![Screenshot des indirekten execdi-Beispiels mit GPU-culult](images/executeindirect-withculling.png)

<span data-ttu-id="3301b-282">Das Beispiel ohne GPU-primitive-kulalisierung.</span><span class="sxs-lookup"><span data-stu-id="3301b-282">The sample without GPU primitive culling.</span></span>

![Screenshot des indirekten execdi-Beispiels ohne GPU-culult](images/executeindirect-withoutculling.png)

## <a name="related-topics"></a><span data-ttu-id="3301b-284">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3301b-284">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3301b-285">D3D12-Code Exemplarische Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="3301b-285">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="3301b-286">Video-Tutorials zu DirectX Advanced Learning: Ausführen indirekter und asynchroner GPU-Berechnungen</span><span class="sxs-lookup"><span data-stu-id="3301b-286">DirectX advanced learning video tutorials : Execute Indirect and Async GPU culling</span></span>](https://www.youtube.com/watch?v=fKD-VKJeeds)
</dt> <dt>

[<span data-ttu-id="3301b-287">Indirektes zeichnen</span><span class="sxs-lookup"><span data-stu-id="3301b-287">Indirect Drawing</span></span>](indirect-drawing.md)
</dt> </dl>

 

 
