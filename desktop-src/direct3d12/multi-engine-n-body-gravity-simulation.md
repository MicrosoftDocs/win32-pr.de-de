---
title: N-Text-Schwerkraft Simulation mit mehreren Modulen
description: Das D3D12nBodyGravity-Beispiel veranschaulicht, wie Compute-Arbeit asynchron ausgeführt wird.
ms.assetid: B20C5575-0616-43F7-9AC9-5F802E5597B5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60782519de6f655882717c4ea657668129a6ce3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548661"
---
# <a name="multi-engine-n-body-gravity-simulation"></a><span data-ttu-id="76835-103">N-Text-Schwerkraft Simulation mit mehreren Modulen</span><span class="sxs-lookup"><span data-stu-id="76835-103">Multi-engine n-body gravity simulation</span></span>

<span data-ttu-id="76835-104">Das **D3D12nBodyGravity** -Beispiel veranschaulicht, wie Compute-Arbeit asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76835-104">The **D3D12nBodyGravity** sample demonstrates how to do compute work asynchronously.</span></span> <span data-ttu-id="76835-105">Das Beispiel startet eine Reihe von Threads, die jeweils über eine COMPUTE-Befehls Warteschlange verfügen, und plant Compute-Arbeit auf der GPU, die eine n-Text-Schwerkraft Simulation ausführt.</span><span class="sxs-lookup"><span data-stu-id="76835-105">The sample spins up a number of threads each with a compute command queue and schedules compute work on the GPU that performs an n-body gravity simulation.</span></span> <span data-ttu-id="76835-106">Jeder Thread arbeitet mit zwei Puffer, die sich aus der Position und den Geschwindigkeitsdaten zusammen befinden.</span><span class="sxs-lookup"><span data-stu-id="76835-106">Each thread operates on two buffers full of position and velocity data.</span></span> <span data-ttu-id="76835-107">Bei jeder Iterationen liest der COMPUTE-Shader die aktuellen Positions-und Geschwindigkeitsdaten aus einem Puffer und schreibt die nächste Iterationen in den anderen Puffer.</span><span class="sxs-lookup"><span data-stu-id="76835-107">With each iteration, the compute shader reads the current position and velocity data from one buffer and writes the next iteration into the other buffer.</span></span> <span data-ttu-id="76835-108">Wenn die Iterationen abgeschlossen sind, tauscht der COMPUTE-Shader aus, welcher Puffer der SRV zum Lesen von Positions-/Velocity-Daten ist. dabei handelt es sich um die UAV zum Schreiben von Positions-/Velocity-Updates durch Ändern des Ressourcen Zustands für jeden Puffer.</span><span class="sxs-lookup"><span data-stu-id="76835-108">When the iteration completes, the compute shader swaps which buffer is the SRV for reading position/velocity data and which is the UAV for writing position/velocity updates by changing the resource state on each buffer.</span></span>

-   [<span data-ttu-id="76835-109">Erstellen der Stamm Signaturen</span><span class="sxs-lookup"><span data-stu-id="76835-109">Create the root signatures</span></span>](#create-the-root-signatures)
-   [<span data-ttu-id="76835-110">Erstellen der SRV-und UAV-Puffer</span><span class="sxs-lookup"><span data-stu-id="76835-110">Create the SRV and UAV buffers</span></span>](#create-the-srv-and-uav-buffers)
-   [<span data-ttu-id="76835-111">Erstellen der CBV-und Vertex-Puffer</span><span class="sxs-lookup"><span data-stu-id="76835-111">Create the CBV and vertex buffers</span></span>](#create-the-cbv-and-vertex-buffers)
-   [<span data-ttu-id="76835-112">Synchronisieren der Rendering-und Compute-Threads</span><span class="sxs-lookup"><span data-stu-id="76835-112">Synchronize the rendering and compute threads</span></span>](#synchronize-the-rendering-and-compute-threads)
-   [<span data-ttu-id="76835-113">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="76835-113">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="76835-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="76835-114">Related topics</span></span>](#related-topics)

## <a name="create-the-root-signatures"></a><span data-ttu-id="76835-115">Erstellen der Stamm Signaturen</span><span class="sxs-lookup"><span data-stu-id="76835-115">Create the root signatures</span></span>

<span data-ttu-id="76835-116">Wir beginnen damit, in der **loadassets** -Methode sowohl eine Grafik als auch eine COMPUTE-Stamm Signatur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="76835-116">We start out by creating both a graphics and a compute root signature, in the **LoadAssets** method.</span></span> <span data-ttu-id="76835-117">Beide Stamm Signaturen haben eine CBV (root Constant Buffer View) und eine Tabelle der Tabelle "Shader Resource View" (SRV).</span><span class="sxs-lookup"><span data-stu-id="76835-117">Both root signatures have a root constant buffer view (CBV) and a shader resource view (SRV) descriptor table.</span></span> <span data-ttu-id="76835-118">Die COMPUTE-Stamm Signatur verfügt auch über eine benutzerdefinierte UAV-Deskriptortabelle (ungeordnete Zugriffs Ansicht).</span><span class="sxs-lookup"><span data-stu-id="76835-118">The compute root signature also has an unordered access view (UAV) descriptor table.</span></span>

``` syntax
 // Create the root signatures.
       {
              CD3DX12_DESCRIPTOR_RANGE ranges[2];
              ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 1, 0);
              ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_UAV, 1, 0);

              CD3DX12_ROOT_PARAMETER rootParameters[RootParametersCount];
              rootParameters[RootParameterCB].InitAsConstantBufferView(0, 0, D3D12_SHADER_VISIBILITY_ALL);
              rootParameters[RootParameterSRV].InitAsDescriptorTable(1, &ranges[0], D3D12_SHADER_VISIBILITY_VERTEX);
              rootParameters[RootParameterUAV].InitAsDescriptorTable(1, &ranges[1], D3D12_SHADER_VISIBILITY_ALL);

              // The rendering pipeline does not need the UAV parameter.
              CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
              rootSignatureDesc.Init(_countof(rootParameters) - 1, rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

              ComPtr<ID3DBlob> signature;
              ComPtr<ID3DBlob> error;
              ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));

              // Create compute signature. Must change visibility for the SRV.
              rootParameters[RootParameterSRV].ShaderVisibility = D3D12_SHADER_VISIBILITY_ALL;

              CD3DX12_ROOT_SIGNATURE_DESC computeRootSignatureDesc(_countof(rootParameters), rootParameters, 0, nullptr);
              ThrowIfFailed(D3D12SerializeRootSignature(&computeRootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));

              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_computeRootSignature)));
       }
```



| <span data-ttu-id="76835-119">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="76835-119">Call flow</span></span>                                                             | <span data-ttu-id="76835-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="76835-120">Parameters</span></span>                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="76835-121">**CD3DX12- \_ \_ Deskriptorbereich**</span><span class="sxs-lookup"><span data-stu-id="76835-121">**CD3DX12\_DESCRIPTOR\_RANGE**</span></span>](cd3dx12-descriptor-range.md)        | [<span data-ttu-id="76835-122">**D3D12- \_ \_ deskriptorbereichstyp \_**</span><span class="sxs-lookup"><span data-stu-id="76835-122">**D3D12\_DESCRIPTOR\_RANGE\_TYPE**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [<span data-ttu-id="76835-123">**CD3DX12 \_ root- \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="76835-123">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="76835-124">**D3D12- \_ Shader- \_ Sichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="76835-124">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="76835-125">**CD3DX12 \_ Stamm \_ Signatur \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="76835-125">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="76835-126">**D3D12 \_ root \_ Signature- \_ Flags**</span><span class="sxs-lookup"><span data-stu-id="76835-126">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="76835-127">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="76835-127">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="76835-128">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="76835-128">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="76835-129">**D3D \_ Stamm \_ Signatur \_ Version**</span><span class="sxs-lookup"><span data-stu-id="76835-129">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="76835-130">**"Kreaterootsignature"**</span><span class="sxs-lookup"><span data-stu-id="76835-130">**CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [<span data-ttu-id="76835-131">**CD3DX12 \_ Stamm \_ Signatur \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="76835-131">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) |                                                                       |
| [<span data-ttu-id="76835-132">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="76835-132">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="76835-133">**D3D \_ Stamm \_ Signatur \_ Version**</span><span class="sxs-lookup"><span data-stu-id="76835-133">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="76835-134">**"Kreaterootsignature"**</span><span class="sxs-lookup"><span data-stu-id="76835-134">**CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-srv-and-uav-buffers"></a><span data-ttu-id="76835-135">Erstellen der SRV-und UAV-Puffer</span><span class="sxs-lookup"><span data-stu-id="76835-135">Create the SRV and UAV buffers</span></span>

<span data-ttu-id="76835-136">Die SRV-und UAV-Puffer bestehen aus einem Array von Positions-und Geschwindigkeitsdaten.</span><span class="sxs-lookup"><span data-stu-id="76835-136">The SRV and UAV buffers consist of an array of position and velocity data.</span></span>

``` syntax
 // Position and velocity data for the particles in the system.
       // Two buffers full of Particle data are utilized in this sample.
       // The compute thread alternates writing to each of them.
       // The render thread renders using the buffer that is not currently
       // in use by the compute shader.
       struct Particle
       {
              XMFLOAT4 position;
              XMFLOAT4 velocity;
       };
```



| <span data-ttu-id="76835-137">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="76835-137">Call flow</span></span>                       | <span data-ttu-id="76835-138">Parameter</span><span class="sxs-lookup"><span data-stu-id="76835-138">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="76835-139">**XMFLOAT4**</span><span class="sxs-lookup"><span data-stu-id="76835-139">**XMFLOAT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

## <a name="create-the-cbv-and-vertex-buffers"></a><span data-ttu-id="76835-140">Erstellen der CBV-und Vertex-Puffer</span><span class="sxs-lookup"><span data-stu-id="76835-140">Create the CBV and vertex buffers</span></span>

<span data-ttu-id="76835-141">Bei der Grafik Pipeline ist die CBV eine **Struktur** , die zwei Matrizen enthält, die vom Geometry-Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76835-141">For the graphics pipeline, the CBV is a **struct** containing two matrices used by the geometry shader.</span></span> <span data-ttu-id="76835-142">Der Geometry-Shader nimmt die Position jedes Partikels im System an und generiert ein Vierfach, um es mithilfe dieser Matrizen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="76835-142">The geometry shader takes the position of each particle in the system and generates a quad to represent it using these matrices.</span></span>

``` syntax
 struct ConstantBufferGS
       {
              XMMATRIX worldViewProjection;
              XMMATRIX inverseView;

              // Constant buffers are 256-byte aligned in GPU memory. Padding is added
              // for convenience when computing the struct's size.
              float padding[32];
       };
```



| <span data-ttu-id="76835-143">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="76835-143">Call flow</span></span>                       | <span data-ttu-id="76835-144">Parameter</span><span class="sxs-lookup"><span data-stu-id="76835-144">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="76835-145">**Xmmatrix**</span><span class="sxs-lookup"><span data-stu-id="76835-145">**XMMATRIX**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) |            |



 

<span data-ttu-id="76835-146">Folglich enthält der Vertex-Puffer, der vom Vertex-Shader verwendet wird, keine Positionsdaten.</span><span class="sxs-lookup"><span data-stu-id="76835-146">As a result, the vertex buffer used by the vertex shader actually does not contain any positional data.</span></span>

``` syntax
 // "Vertex" definition for particles. Triangle vertices are generated 
       // by the geometry shader. Color data will be assigned to those 
       // vertices via this struct.
       struct ParticleVertex
       {
              XMFLOAT4 color;
       };
```



| <span data-ttu-id="76835-147">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="76835-147">Call flow</span></span>                       | <span data-ttu-id="76835-148">Parameter</span><span class="sxs-lookup"><span data-stu-id="76835-148">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="76835-149">**XMFLOAT4**</span><span class="sxs-lookup"><span data-stu-id="76835-149">**XMFLOAT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

<span data-ttu-id="76835-150">Bei der COMPUTE-Pipeline ist die CBV eine **Struktur** , die einige Konstanten enthält, die von der n-Text-Gravitations Simulation im COMPUTE-Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76835-150">For the compute pipeline, the CBV is a **struct** containing some constants used by the n-body gravity simulation in the compute shader.</span></span>

``` syntax
 struct ConstantBufferCS
       {
              UINT param[4];
              float paramf[4];
       };
```

## <a name="synchronize-the-rendering-and-compute-threads"></a><span data-ttu-id="76835-151">Synchronisieren der Rendering-und Compute-Threads</span><span class="sxs-lookup"><span data-stu-id="76835-151">Synchronize the rendering and compute threads</span></span>

<span data-ttu-id="76835-152">Nachdem alle Puffer initialisiert wurden, werden das Rendering und die Compute-Arbeit gestartet.</span><span class="sxs-lookup"><span data-stu-id="76835-152">After the buffers are all initialized, the rendering and compute work will begin.</span></span> <span data-ttu-id="76835-153">Der computethread ändert den Status der beiden Positions-/Velocity-Puffer zwischen SRV und UAV, während er die Simulation durchläuft, und der Renderingthread muss sicherstellen, dass er die Arbeit an der Grafik Pipeline plant, die auf dem SRV ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76835-153">The compute thread will be changing the state of the two position/velocity buffers back and forth between SRV and UAV as it iterates on the simulation, and the rendering thread needs to ensure that it schedules work on the graphics pipeline that operates on the SRV.</span></span> <span data-ttu-id="76835-154">Mithilfe von Zäunen wird der Zugriff auf die beiden Puffer synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="76835-154">Fences are used to synchronize access to the two buffers.</span></span>

<span data-ttu-id="76835-155">Im Renderthread:</span><span class="sxs-lookup"><span data-stu-id="76835-155">On the Render thread:</span></span>

``` syntax
// Render the scene.
void D3D12nBodyGravity::OnRender()
{
       // Let the compute thread know that a new frame is being rendered.
       for (int n = 0; n < ThreadCount; n++)
       {
              InterlockedExchange(&m_renderContextFenceValues[n], m_renderContextFenceValue);
       }

       // Compute work must be completed before the frame can render or else the SRV 
       // will be in the wrong state.
       for (UINT n = 0; n < ThreadCount; n++)
       {
              UINT64 threadFenceValue = InterlockedGetValue(&m_threadFenceValues[n]);
              if (m_threadFences[n]->GetCompletedValue() < threadFenceValue)
              {
                     // Instruct the rendering command queue to wait for the current 
                     // compute work to complete.
                     ThrowIfFailed(m_commandQueue->Wait(m_threadFences[n].Get(), threadFenceValue));
              }
       }

       // Record all the commands we need to render the scene into the command list.
       PopulateCommandList();

       // Execute the command list.
       ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
       m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

       // Present the frame.
       ThrowIfFailed(m_swapChain->Present(0, 0));

       MoveToNextFrame();
}
```



| <span data-ttu-id="76835-156">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="76835-156">Call flow</span></span>                                                              | <span data-ttu-id="76835-157">Parameter</span><span class="sxs-lookup"><span data-stu-id="76835-157">Parameters</span></span> |
|------------------------------------------------------------------------|------------|
| [<span data-ttu-id="76835-158">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="76835-158">**InterlockedExchange**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                  |            |
| [<span data-ttu-id="76835-159">**Interlockedgetvalue**</span><span class="sxs-lookup"><span data-stu-id="76835-159">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)           |            |
| [<span data-ttu-id="76835-160">**Getcompletedvalue**</span><span class="sxs-lookup"><span data-stu-id="76835-160">**GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)             |            |
| [<span data-ttu-id="76835-161">**Wait**</span><span class="sxs-lookup"><span data-stu-id="76835-161">**Wait**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                |            |
| [<span data-ttu-id="76835-162">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="76835-162">**ID3D12CommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [<span data-ttu-id="76835-163">**Executecommandlists**</span><span class="sxs-lookup"><span data-stu-id="76835-163">**ExecuteCommandLists**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [<span data-ttu-id="76835-164">**IDXGISwapChain1::Present1**</span><span class="sxs-lookup"><span data-stu-id="76835-164">**IDXGISwapChain1::Present1**</span></span>](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

<span data-ttu-id="76835-165">Um das Beispiel etwas zu vereinfachen, wartet der computethread, bis die GPU jede Iterationen abschließt, bevor eine weitere computearbeit geplant wird.</span><span class="sxs-lookup"><span data-stu-id="76835-165">To simplify the sample a bit, the compute thread waits for the GPU to complete each iteration before scheduling any more compute work.</span></span> <span data-ttu-id="76835-166">In der Praxis möchten Anwendungen wahrscheinlich die computewarteschlange vollständig aufbewahren, um eine maximale Leistung von der GPU zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="76835-166">In practice, applications will likely want to keep the compute queue full to achieve maximum performance from the GPU.</span></span>

<span data-ttu-id="76835-167">Im COMPUTE-Thread:</span><span class="sxs-lookup"><span data-stu-id="76835-167">On the Compute thread:</span></span>

``` syntax
DWORD D3D12nBodyGravity::AsyncComputeThreadProc(int threadIndex)
{
       ID3D12CommandQueue* pCommandQueue = m_computeCommandQueue[threadIndex].Get();
       ID3D12CommandAllocator* pCommandAllocator = m_computeAllocator[threadIndex].Get();
       ID3D12GraphicsCommandList* pCommandList = m_computeCommandList[threadIndex].Get();
       ID3D12Fence* pFence = m_threadFences[threadIndex].Get();

       while (0 == InterlockedGetValue(&m_terminating))
       {
              // Run the particle simulation.
              Simulate(threadIndex);

              // Close and execute the command list.
              ThrowIfFailed(pCommandList->Close());
              ID3D12CommandList* ppCommandLists[] = { pCommandList };

              pCommandQueue->ExecuteCommandLists(1, ppCommandLists);

              // Wait for the compute shader to complete the simulation.
              UINT64 threadFenceValue = InterlockedIncrement(&m_threadFenceValues[threadIndex]);
              ThrowIfFailed(pCommandQueue->Signal(pFence, threadFenceValue));
              ThrowIfFailed(pFence->SetEventOnCompletion(threadFenceValue, m_threadFenceEvents[threadIndex]));
              WaitForSingleObject(m_threadFenceEvents[threadIndex], INFINITE);

              // Wait for the render thread to be done with the SRV so that
              // the next frame in the simulation can run.
              UINT64 renderContextFenceValue = InterlockedGetValue(&m_renderContextFenceValues[threadIndex]);
              if (m_renderContextFence->GetCompletedValue() < renderContextFenceValue)
              {
                     ThrowIfFailed(pCommandQueue->Wait(m_renderContextFence.Get(), renderContextFenceValue));
                     InterlockedExchange(&m_renderContextFenceValues[threadIndex], 0);
              }

              // Swap the indices to the SRV and UAV.
              m_srvIndex[threadIndex] = 1 - m_srvIndex[threadIndex];

              // Prepare for the next frame.
              ThrowIfFailed(pCommandAllocator->Reset());
              ThrowIfFailed(pCommandList->Reset(pCommandAllocator, m_computeState.Get()));
       }

       return 0;
}
```



| <span data-ttu-id="76835-168">Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="76835-168">Call flow</span></span>                                                                   | <span data-ttu-id="76835-169">Parameter</span><span class="sxs-lookup"><span data-stu-id="76835-169">Parameters</span></span> |
|-----------------------------------------------------------------------------|------------|
| [<span data-ttu-id="76835-170">**ID3D12CommandQueue**</span><span class="sxs-lookup"><span data-stu-id="76835-170">**ID3D12CommandQueue**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)                            |            |
| [<span data-ttu-id="76835-171">**ID3D12CommandAllocator**</span><span class="sxs-lookup"><span data-stu-id="76835-171">**ID3D12CommandAllocator**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)                    |            |
| [<span data-ttu-id="76835-172">**ID3D12GraphicsCommandList**</span><span class="sxs-lookup"><span data-stu-id="76835-172">**ID3D12GraphicsCommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)              |            |
| [<span data-ttu-id="76835-173">**ID3D12Fence**</span><span class="sxs-lookup"><span data-stu-id="76835-173">**ID3D12Fence**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)                                          |            |
| [<span data-ttu-id="76835-174">**Interlockedgetvalue**</span><span class="sxs-lookup"><span data-stu-id="76835-174">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [<span data-ttu-id="76835-175">**Schließen**</span><span class="sxs-lookup"><span data-stu-id="76835-175">**Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)                            |            |
| [<span data-ttu-id="76835-176">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="76835-176">**ID3D12CommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                              |            |
| [<span data-ttu-id="76835-177">**Executecommandlists**</span><span class="sxs-lookup"><span data-stu-id="76835-177">**ExecuteCommandLists**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)       |            |
| [<span data-ttu-id="76835-178">**InterlockedIncrement**</span><span class="sxs-lookup"><span data-stu-id="76835-178">**InterlockedIncrement**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedincrement)                     |            |
| [<span data-ttu-id="76835-179">**Aussendet**</span><span class="sxs-lookup"><span data-stu-id="76835-179">**Signal**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                                 |            |
| [<span data-ttu-id="76835-180">**"Abschlusventoncompletion"**</span><span class="sxs-lookup"><span data-stu-id="76835-180">**SetEventOnCompletion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)            |            |
| [<span data-ttu-id="76835-181">**WaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="76835-181">**WaitForSingleObject**</span></span>](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)                         |            |
| [<span data-ttu-id="76835-182">**Interlockedgetvalue**</span><span class="sxs-lookup"><span data-stu-id="76835-182">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [<span data-ttu-id="76835-183">**Getcompletedvalue**</span><span class="sxs-lookup"><span data-stu-id="76835-183">**GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)                  |            |
| [<span data-ttu-id="76835-184">**Wait**</span><span class="sxs-lookup"><span data-stu-id="76835-184">**Wait**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                     |            |
| [<span data-ttu-id="76835-185">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="76835-185">**InterlockedExchange**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                       |            |
| [<span data-ttu-id="76835-186">**ID3D12CommandAllocator:: Reset**</span><span class="sxs-lookup"><span data-stu-id="76835-186">**ID3D12CommandAllocator::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)       |            |
| [<span data-ttu-id="76835-187">**ID3D12GraphicsCommandList:: Reset**</span><span class="sxs-lookup"><span data-stu-id="76835-187">**ID3D12GraphicsCommandList::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) |            |



 

## <a name="run-the-sample"></a><span data-ttu-id="76835-188">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="76835-188">Run the sample</span></span>

![Screenshot der abschließenden n-Text Schwerpunkt Simulation](images/nbodygravity.png)

## <a name="related-topics"></a><span data-ttu-id="76835-190">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="76835-190">Related topics</span></span>

[<span data-ttu-id="76835-191">D3D12-Code Exemplarische Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="76835-191">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)

[<span data-ttu-id="76835-192">Multi-Engine-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="76835-192">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)