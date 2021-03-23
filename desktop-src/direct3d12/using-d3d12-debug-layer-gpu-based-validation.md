---
title: GPU-basierte Validierung und die Direct3D 12-Debugebene
description: In diesem Thema wird beschrieben, wie die Direct3D 12-Debugebene optimal genutzt wird. Die GPU-basierte Validierung (GBV) ermöglicht Validierungs Szenarien auf der GPU-Zeitachse, die bei API-aufrufen auf der CPU nicht möglich sind.
ms.assetid: 01D1F94F-4DD4-4781-86EF-6C639E8B1069
ms.localizationpriority: high
ms.topic: article
ms.date: 02/12/2019
ms.openlocfilehash: 3160df3faf994df2abf9cf878088e84564bb5fe1
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548731"
---
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a><span data-ttu-id="17f58-104">GPU-basierte Validierung und die Direct3D 12-Debugebene</span><span class="sxs-lookup"><span data-stu-id="17f58-104">GPU-based validation and the Direct3D 12 Debug Layer</span></span>

<span data-ttu-id="17f58-105">In diesem Thema wird beschrieben, wie die Direct3D 12-Debugebene optimal genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="17f58-105">This topic describes how to make best use of the Direct3D 12 Debug Layer.</span></span> <span data-ttu-id="17f58-106">Die GPU-basierte Validierung (GBV) ermöglicht Validierungs Szenarien auf der GPU-Zeitachse, die bei API-aufrufen auf der CPU nicht möglich sind.</span><span class="sxs-lookup"><span data-stu-id="17f58-106">GPU-based validation (GBV) enables validation scenarios on the GPU timeline that are not possible during API calls on the CPU.</span></span> <span data-ttu-id="17f58-107">GBV ist ab dem Grafik Tool für Windows 10 Anniversary Update verfügbar.</span><span class="sxs-lookup"><span data-stu-id="17f58-107">GBV is available starting with the Graphics Tools for Windows 10 Anniversary Update.</span></span>

## <a name="purpose-of-gpu-based-validation"></a><span data-ttu-id="17f58-108">Zweck der GPU-basierten Validierung</span><span class="sxs-lookup"><span data-stu-id="17f58-108">Purpose of GPU-based validation</span></span>

<span data-ttu-id="17f58-109">Die GPU-basierte Überprüfung hilft bei der Identifizierung der folgenden Fehler:</span><span class="sxs-lookup"><span data-stu-id="17f58-109">GPU-based validation helps to identify the following errors:</span></span>

- <span data-ttu-id="17f58-110">Verwendung von nicht initialisierten oder inkompatiblen Deskriptoren in einem Shader.</span><span class="sxs-lookup"><span data-stu-id="17f58-110">Use of uninitialized or incompatible descriptors in a shader.</span></span>
- <span data-ttu-id="17f58-111">Verwendung von Deskriptoren, die auf gelöschte Ressourcen in einem Shader verweisen.</span><span class="sxs-lookup"><span data-stu-id="17f58-111">Use of descriptors referencing deleted Resources in a shader.</span></span>
- <span data-ttu-id="17f58-112">Validierung der höher gestuften Ressourcen Zustände und des Zustands des Ressourcen Zustands.</span><span class="sxs-lookup"><span data-stu-id="17f58-112">Validation of promoted resource states and resource state decay.</span></span>
- <span data-ttu-id="17f58-113">Indizierung über das Ende des deskriptorheaps in einem Shader hinaus.</span><span class="sxs-lookup"><span data-stu-id="17f58-113">Indexing beyond the end of the descriptor heap in a shader.</span></span>
- <span data-ttu-id="17f58-114">Shader-Zugriffe von Ressourcen im inkompatiblen Zustand.</span><span class="sxs-lookup"><span data-stu-id="17f58-114">Shader accesses of resources in incompatible state.</span></span>
- <span data-ttu-id="17f58-115">Verwendung von nicht initialisierten oder inkompatiblen Samplern in einem Shader.</span><span class="sxs-lookup"><span data-stu-id="17f58-115">Use of uninitialized or incompatible Samplers in a shader.</span></span>

<span data-ttu-id="17f58-116">GBV funktioniert, indem gepatchte Shader erstellt werden, deren Validierung dem Shader direkt hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="17f58-116">GBV works by creating patched shaders that have validation added directly to the shader.</span></span> <span data-ttu-id="17f58-117">Die gepatchten Shader überprüfen Stamm Argumente und Ressourcen, auf die während der shaderausführung zugegriffen wurde, und melden Fehler an einen Protokollpuffer</span><span class="sxs-lookup"><span data-stu-id="17f58-117">The patched shaders inspect root arguments and resources accessed during shader execution and report errors to a log buffer.</span></span> <span data-ttu-id="17f58-118">GBV fügt auch zusätzliche Vorgänge und Dispatch-Aufrufe in die Anwendungs Befehlslisten ein, um Änderungen am Ressourcen Status zu überprüfen und nachverfolgen, die von der Befehlsliste auf der GPU-Zeitachse erhoben werden.</span><span class="sxs-lookup"><span data-stu-id="17f58-118">GBV also injects extra operations and Dispatch calls into the application command lists to validate and track changes to resource state imposed by the command list on the GPU-timeline.</span></span>

<span data-ttu-id="17f58-119">Da GBV die Fähigkeit zum Ausführen von Shadern erfordert, werden Kopier Befehlslisten durch eine COMPUTE-Befehlsliste emuliert.</span><span class="sxs-lookup"><span data-stu-id="17f58-119">Because GBV requires the ability to execute shaders, COPY command lists are emulated by a COMPUTE command list.</span></span> <span data-ttu-id="17f58-120">Dies kann möglicherweise die Art und Weise ändern, wie Hardware Kopien ausführt, obwohl das Endergebnis nicht geändert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="17f58-120">This may potentially change how hardware performs copies though the end result should not be changed.</span></span> <span data-ttu-id="17f58-121">Diese werden von der Anwendung weiterhin als Kopier Befehlslisten wahrgenommen, und die debugschicht überprüft sie als solche.</span><span class="sxs-lookup"><span data-stu-id="17f58-121">The application will still perceive these are COPY command lists and the debug layer will validate them as such.</span></span>

## <a name="turning-on-gpu-based-validation"></a><span data-ttu-id="17f58-122">Aktivieren der GPU-basierten Validierung</span><span class="sxs-lookup"><span data-stu-id="17f58-122">Turning on GPU-based validation</span></span>

<span data-ttu-id="17f58-123">GBV kann bei der Verwendung der DirectX-Systemsteuerung (dxcpl) erzwungen werden, indem auf der Direct3D 12-debugschicht erzwungen und zusätzlich die GPU-basierte Validierung erzwungen wird (neue Registerkarte in der Systemsteuerung).</span><span class="sxs-lookup"><span data-stu-id="17f58-123">GBV can be forced on using the DirectX Control Panel (DXCPL) by forcing on the Direct3D 12 Debug Layer and additionally forcing on GPU-based validation (new tab in the control panel).</span></span> <span data-ttu-id="17f58-124">Nach der Aktivierung bleibt GBV aktiviert, bis das Direct3D 12-Gerät freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="17f58-124">Once enabled, GBV will remain enabled until the Direct3D 12 device is released.</span></span> <span data-ttu-id="17f58-125">Alternativ kann GBV auch Programm gesteuert aktiviert werden, bevor das Direct3D 12-Gerät erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="17f58-125">Alternatively, GBV can be enabled programmatically prior to creating the Direct3D 12 Device:</span></span>

```cpp
void EnableShaderBasedValidation()
{
    CComPtr<ID3D12Debug> spDebugController0;
    CComPtr<ID3D12Debug1> spDebugController1;
    VERIFY(D3D12GetDebugInterface(IID_PPV_ARGS(&spDebugController0)));
    VERIFY(spDebugController0->QueryInterface(IID_PPV_ARGS(&spDebugController1)));
    spDebugController1->SetEnableGPUBasedValidation(true);
}
```

## <a name="recommended-usage"></a><span data-ttu-id="17f58-126">Empfohlene Verwendung</span><span class="sxs-lookup"><span data-stu-id="17f58-126">Recommended usage</span></span>

<span data-ttu-id="17f58-127">Im Allgemeinen sollten Sie den Code in den meisten Fällen mit aktivierter debugschicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="17f58-127">Generally, you should run your code with the debug layer enabled most of the time.</span></span> <span data-ttu-id="17f58-128">GBV kann jedoch eine große Anzahl von Aufgaben beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="17f58-128">However, GBV can slow things down a lot.</span></span> <span data-ttu-id="17f58-129">Entwickler könnten GBV mit kleineren Datasets aktivieren (z. b. Engine-Demos oder kleine Spielebenen mit weniger PSO-und-Ressourcen) oder während der frühen Anwendungs Bereitstellung, um Leistungsprobleme zu verringern.</span><span class="sxs-lookup"><span data-stu-id="17f58-129">Developers may consider enabling GBV with smaller data sets (for example, engine demos or small game levels with fewer PSO’s and resources) or during early application bring-up to reduce performance problems.</span></span> <span data-ttu-id="17f58-130">Bei größeren Inhalten empfiehlt es sich, GBV in einem nächtlichen Test Durchlauf auf einem oder zwei Testcomputern zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="17f58-130">With larger content consider turning on GBV on one or two test machines in a nightly test pass.</span></span>

## <a name="debug-output"></a><span data-ttu-id="17f58-131">Ausgabe Debuggen</span><span class="sxs-lookup"><span data-stu-id="17f58-131">Debug output</span></span>

<span data-ttu-id="17f58-132">GBV erzeugt eine Debugausgabe, nachdem bei der Ausführung von [**executecommandlists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) die Ausführung auf der GPU abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="17f58-132">GBV produces debug output after a call to [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) completes execution on the GPU.</span></span> <span data-ttu-id="17f58-133">Da sich dies auf der GPU-Zeitachse befindet, kann die Debugausgabe mit einer anderen CPU-Zeitachsen Validierung asynchron sein.</span><span class="sxs-lookup"><span data-stu-id="17f58-133">Since this is on the GPU-timeline the debug output may be asynchronous with other CPU-timeline validation.</span></span> <span data-ttu-id="17f58-134">Anwendungsentwickler möchten möglicherweise Ihre eigene Wait-after-Execute-Datei einfügen, um die Debugausgabe zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="17f58-134">Application developers may want to inject their own wait-after-execute to synchronize debug output.</span></span>

<span data-ttu-id="17f58-135">Die GBV-Ausgabe gibt an, wo ein Fehler in einem Shader aufgetreten ist, zusammen mit der aktuellen Draw-/Dispatch-Anzahl und den Identitäten verwandter Objekte (z. b. Befehlsliste, Warteschlange, PSO usw.).</span><span class="sxs-lookup"><span data-stu-id="17f58-135">GBV output identifies where in a shader an error occurred, along with the current draw/dispatch count and identities of related objects (e.g. command list, queue, PSO, etc).</span></span>

## <a name="example-debug-message"></a><span data-ttu-id="17f58-136">Beispiel für Debugmeldung</span><span class="sxs-lookup"><span data-stu-id="17f58-136">Example debug message</span></span>

<span data-ttu-id="17f58-137">Die folgende Fehlermeldung gibt an, dass auf eine Ressource mit dem Namen "Haupt Farb Puffer" in einem Shader als Shaderressource zugegriffen wurde, sich jedoch im ungeordneten Zugriffs Zustand befunden hat, als der Shader auf der GPU ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="17f58-137">The following error message indicates that a resource named “Main Color Buffer” was accessed in a shader as a shader resource but was in the unordered access state when the shader ran on the GPU.</span></span> <span data-ttu-id="17f58-138">Weitere Informationen, wie z. b. der Speicherort in der Shader-Quelle, der Name der Befehlsliste und der Zeichnungs Zähler (Index zeichnen) und die Namen von verknüpften D3D-Schnittstellen Objekten werden ebenfalls bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="17f58-138">Additional information, such as the location in the shader source, the name of the command list and the Draw count (Draw Index), and the names of related D3D interface objects are also provided.</span></span>

```cmd
D3D12 ERROR: Incompatible resource state: Resource: 0x0000016F61A6EA80:'Main Color Buffer', 
Subresource Index: [0], 
Descriptor heap index: [0], 
Binding Type In Descriptor: SRV, 
Resource State: D3D12_RESOURCE_STATE_UNORDERED_ACCESS(0x8), 
Shader Stage: PIXEL, 
Root Parameter Index: [0], 
Draw Index: [0], 
Shader Code: E:\FileShare\MiniEngine_GitHub_160128\MiniEngine_GitHub\Core\Shaders\SharpeningUpsamplePS.hlsl(37,2-59), 
Asm Instruction Range: [0x138-0x16b], 
Asm Operand Index: [3], 
Command List: 0x0000016F6F75F740:'CommandList', SRV/UAV/CBV Descriptor Heap: 0x0000016F6F76F280:'Unnamed ID3D12DescriptorHeap Object', 
Sampler Descriptor Heap: <not set>, 
Pipeline State: 0x0000016F572C89F0:'Unnamed ID3D12PipelineState Object',  
[ EXECUTION ERROR #942: GPU_BASED_VALIDATION_INCOMPATIBLE_RESOURCE_STATE]
```

## <a name="debug-layer-apis"></a><span data-ttu-id="17f58-139">Debug-ebenenapis</span><span class="sxs-lookup"><span data-stu-id="17f58-139">Debug Layer APIs</span></span>

<span data-ttu-id="17f58-140">Um die Debug-Ebene zu aktivieren, müssen Sie [**enabledebuglayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="17f58-140">To enable the debug layer, call [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).</span></span>

<span data-ttu-id="17f58-141">Um die GPU-basierte Validierung zu aktivieren [**, geben**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)Sie "\*" an, und verweisen Sie auf die Methoden der folgenden Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="17f58-141">To enable GPU-based validation, call [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation), and refer to the methods of the following interfaces:</span></span>

- [<span data-ttu-id="17f58-142">**ID3D12Debug1**</span><span class="sxs-lookup"><span data-stu-id="17f58-142">**ID3D12Debug1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [<span data-ttu-id="17f58-143">**ID3D12DebugCommandList1**</span><span class="sxs-lookup"><span data-stu-id="17f58-143">**ID3D12DebugCommandList1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [<span data-ttu-id="17f58-144">**ID3D12DebugDevice1**</span><span class="sxs-lookup"><span data-stu-id="17f58-144">**ID3D12DebugDevice1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

<span data-ttu-id="17f58-145">Weitere Informationen finden Sie in den folgenden Enumerationen und Strukturen:</span><span class="sxs-lookup"><span data-stu-id="17f58-145">Refer to the following enumerations and structures:</span></span>

- [<span data-ttu-id="17f58-146">**D3D12 \_ Debug- \_ Befehls \_ Listen- \_ \_ Parametertyp**</span><span class="sxs-lookup"><span data-stu-id="17f58-146">**D3D12\_DEBUG\_COMMAND\_LIST\_PARAMETER\_TYPE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [<span data-ttu-id="17f58-147">**D3D12 \_ Debug \_ - \_ Geräte \_ Parametertyp**</span><span class="sxs-lookup"><span data-stu-id="17f58-147">**D3D12\_DEBUG\_DEVICE\_PARAMETER\_TYPE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [<span data-ttu-id="17f58-148">**D3D12 \_ GPU- \_ basierter \_ Validierungs \_ Pipeline \_ Status \_ Create \_ Flags**</span><span class="sxs-lookup"><span data-stu-id="17f58-148">**D3D12\_GPU\_BASED\_VALIDATION\_PIPELINE\_STATE\_CREATE\_FLAGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [<span data-ttu-id="17f58-149">**D3D12 \_ GPU- \_ basierter \_ Validierungs- \_ Shader- \_ \_ patchmodus**</span><span class="sxs-lookup"><span data-stu-id="17f58-149">**D3D12\_GPU\_BASED\_VALIDATION\_SHADER\_PATCH\_MODE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [<span data-ttu-id="17f58-150">**D3D12 \_ Debug- \_ Befehls \_ Liste GPU- \_ \_ basierte \_ Validierungs \_ Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="17f58-150">**D3D12\_DEBUG\_COMMAND\_LIST\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [<span data-ttu-id="17f58-151">**D3D12 \_ Debuggen von \_ \_ GPU-basierten Überprüfungs \_ \_ \_ Einstellungen für Geräte**</span><span class="sxs-lookup"><span data-stu-id="17f58-151">**D3D12\_DEBUG\_DEVICE\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a><span data-ttu-id="17f58-152">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="17f58-152">Related topics</span></span>

* [<span data-ttu-id="17f58-153">Grundlegendes zur Direct3D 12-Debugebene</span><span class="sxs-lookup"><span data-stu-id="17f58-153">Understanding the Direct3D 12 Debug Layer</span></span>](understanding-the-d3d12-debug-layer.md)
