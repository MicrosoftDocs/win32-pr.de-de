---
title: Erstellen einer einfachen Direct3D 12-Komponente
description: In diesem Thema wird der aufrufflow zum Erstellen einer grundlegenden Direct3D 12-Komponente beschrieben.
ms.assetid: A0FB108B-15C1-42AD-9277-D5CB63FA8329
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: d0c7ead9ce67ee23a0668304a006d6cd67fb3d67
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "104758860"
---
# <a name="creating-a-basic-direct3d-12-component"></a><span data-ttu-id="538cb-103">Erstellen einer einfachen Direct3D 12-Komponente</span><span class="sxs-lookup"><span data-stu-id="538cb-103">Creating a basic Direct3D 12 component</span></span>

> [!NOTE]
> <span data-ttu-id="538cb-104">Weitere Informationen zum Erstellen von Grafik intensiven Anwendungen für Windows 10 finden Sie im " [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) "-Repository für DirectX 12-Grafik Beispiele.</span><span class="sxs-lookup"><span data-stu-id="538cb-104">See the [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) repo for DirectX 12 Graphics samples that demonstrate how to build graphics-intensive applications for Windows 10.</span></span>

<span data-ttu-id="538cb-105">In diesem Thema wird der aufrufflow zum Erstellen einer grundlegenden Direct3D 12-Komponente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="538cb-105">This topic describes the call flow to create a basic Direct3D 12 component.</span></span>

-   [<span data-ttu-id="538cb-106">Codefluss für eine einfache APP</span><span class="sxs-lookup"><span data-stu-id="538cb-106">Code flow for a simple app</span></span>](#code-flow-for-a-simple-app)
    -   [<span data-ttu-id="538cb-107">Initialisieren</span><span class="sxs-lookup"><span data-stu-id="538cb-107">Initialize</span></span>](#initialize)
    -   [<span data-ttu-id="538cb-108">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="538cb-108">Update</span></span>](#update)
    -   [<span data-ttu-id="538cb-109">Render</span><span class="sxs-lookup"><span data-stu-id="538cb-109">Render</span></span>](#render)
    -   [<span data-ttu-id="538cb-110">Zerstören</span><span class="sxs-lookup"><span data-stu-id="538cb-110">Destroy</span></span>](#destroy)
-   [<span data-ttu-id="538cb-111">Code Beispiel für eine einfache APP</span><span class="sxs-lookup"><span data-stu-id="538cb-111">Code example for a simple app</span></span>](#code-example-for-a-simple-app)
    -   [<span data-ttu-id="538cb-112">Class D3D12HelloTriangle</span><span class="sxs-lookup"><span data-stu-id="538cb-112">class D3D12HelloTriangle</span></span>](#class-d3d12hellotriangle)
    -   [<span data-ttu-id="538cb-113">OnInit ()</span><span class="sxs-lookup"><span data-stu-id="538cb-113">OnInit()</span></span>](#oninit)
    -   [<span data-ttu-id="538cb-114">Loadpipeline ()</span><span class="sxs-lookup"><span data-stu-id="538cb-114">LoadPipeline()</span></span>](#loadpipeline)
    -   [<span data-ttu-id="538cb-115">Loadassets ()</span><span class="sxs-lookup"><span data-stu-id="538cb-115">LoadAssets()</span></span>](#loadassets)
    -   [<span data-ttu-id="538cb-116">OnUpdate ()</span><span class="sxs-lookup"><span data-stu-id="538cb-116">OnUpdate()</span></span>](#onupdate)
    -   [<span data-ttu-id="538cb-117">Onrendering ()</span><span class="sxs-lookup"><span data-stu-id="538cb-117">OnRender()</span></span>](#onrender)
    -   [<span data-ttu-id="538cb-118">Populatecommandlist ()</span><span class="sxs-lookup"><span data-stu-id="538cb-118">PopulateCommandList()</span></span>](#populatecommandlist)
    -   [<span data-ttu-id="538cb-119">Waitforpreviousframe ()</span><span class="sxs-lookup"><span data-stu-id="538cb-119">WaitForPreviousFrame()</span></span>](#waitforpreviousframe)
    -   [<span data-ttu-id="538cb-120">OnDestroy ()</span><span class="sxs-lookup"><span data-stu-id="538cb-120">OnDestroy()</span></span>](#ondestroy)
-   [<span data-ttu-id="538cb-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="538cb-121">Related topics</span></span>](#related-topics)

## <a name="code-flow-for-a-simple-app"></a><span data-ttu-id="538cb-122">Codefluss für eine einfache APP</span><span class="sxs-lookup"><span data-stu-id="538cb-122">Code flow for a simple app</span></span>

<span data-ttu-id="538cb-123">Die äußerste Schleife eines D3D 12-Programms folgt einem sehr standardmäßigen Grafik Prozess:</span><span class="sxs-lookup"><span data-stu-id="538cb-123">The outermost loop of a D3D 12 program follows a very standard graphics process:</span></span>

> [!TIP]
> <span data-ttu-id="538cb-124">Auf die neuen Funktionen von Direct3D 12 folgt ein Hinweis.</span><span class="sxs-lookup"><span data-stu-id="538cb-124">Features new to Direct3D 12 are followed by a note.</span></span>

-   [<span data-ttu-id="538cb-125">Initialisieren</span><span class="sxs-lookup"><span data-stu-id="538cb-125">Initialize</span></span>](#initialize)
-   <span data-ttu-id="538cb-126">**Wiederholung**</span><span class="sxs-lookup"><span data-stu-id="538cb-126">**Repeat**</span></span>
    -   [<span data-ttu-id="538cb-127">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="538cb-127">Update</span></span>](#update)
    -   [<span data-ttu-id="538cb-128">Render</span><span class="sxs-lookup"><span data-stu-id="538cb-128">Render</span></span>](#render)
-   [<span data-ttu-id="538cb-129">Zerstören</span><span class="sxs-lookup"><span data-stu-id="538cb-129">Destroy</span></span>](#destroy)

### <a name="initialize"></a><span data-ttu-id="538cb-130">Initialisieren</span><span class="sxs-lookup"><span data-stu-id="538cb-130">Initialize</span></span>

<span data-ttu-id="538cb-131">Bei der Initialisierung müssen zunächst die globalen Variablen und Klassen eingerichtet werden, und die Pipeline und die Assets müssen von einer Initialisierungsfunktion vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="538cb-131">Initialization involves first setting up the global variables and classes, and an initialize function must prepare the pipeline and assets.</span></span>

-   <span data-ttu-id="538cb-132">Initialisieren Sie die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="538cb-132">Initialize the pipeline.</span></span>
    -   <span data-ttu-id="538cb-133">Aktivieren Sie die Debugebene.</span><span class="sxs-lookup"><span data-stu-id="538cb-133">Enable the debug layer.</span></span>
    -   <span data-ttu-id="538cb-134">Erstellen Sie das Gerät.</span><span class="sxs-lookup"><span data-stu-id="538cb-134">Create the device.</span></span>
    -   <span data-ttu-id="538cb-135">Erstellen Sie die Befehls Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="538cb-135">Create the command queue.</span></span>
    -   <span data-ttu-id="538cb-136">Erstellen Sie die Swapkette.</span><span class="sxs-lookup"><span data-stu-id="538cb-136">Create the swap chain.</span></span>
    -   <span data-ttu-id="538cb-137">Erstellen Sie einen RTV-deskriptorheap (renderzielansicht).</span><span class="sxs-lookup"><span data-stu-id="538cb-137">Create a render target view (RTV) descriptor heap.</span></span>
        > [!Note]  
        > <span data-ttu-id="538cb-138">Ein [deskriptorheap](descriptor-heaps.md) kann als ein Array von [Deskriptoren](descriptors.md)betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="538cb-138">A [descriptor heap](descriptor-heaps.md) can be thought of as an array of [descriptors](descriptors.md).</span></span> <span data-ttu-id="538cb-139">, Wobei jeder Deskriptor ein Objekt vollständig auf die GPU beschreibt.</span><span class="sxs-lookup"><span data-stu-id="538cb-139">Where each descriptor fully describes an object to the GPU.</span></span>

    -   <span data-ttu-id="538cb-140">Erstellen von Frame Ressourcen (eine renderzielansicht für jeden Frame).</span><span class="sxs-lookup"><span data-stu-id="538cb-140">Create frame resources (a render target view for each frame).</span></span>
    -   <span data-ttu-id="538cb-141">Erstellen Sie eine Befehls Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="538cb-141">Create a command allocator.</span></span>
        > [!Note]  
        > <span data-ttu-id="538cb-142">Ein Befehls Zuweiser verwaltet den zugrunde liegenden Speicher für [Befehlslisten und Pakete](recording-command-lists-and-bundles.md).</span><span class="sxs-lookup"><span data-stu-id="538cb-142">A command allocator manages the underlying storage for [command lists and bundles](recording-command-lists-and-bundles.md).</span></span>
         
-   <span data-ttu-id="538cb-143">Initialisieren Sie die Objekte.</span><span class="sxs-lookup"><span data-stu-id="538cb-143">Initialize the assets.</span></span>
    -   <span data-ttu-id="538cb-144">Erstellen Sie eine leere Stamm Signatur.</span><span class="sxs-lookup"><span data-stu-id="538cb-144">Create an empty root signature.</span></span>
        > [!Note]  
        > <span data-ttu-id="538cb-145">Eine Grafik Stamm [Signatur](root-signatures.md) definiert, welche Ressourcen an die Grafik Pipeline gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="538cb-145">A graphics [root signature](root-signatures.md) defines what resources are bound to the graphics pipeline.</span></span>

    -   <span data-ttu-id="538cb-146">Kompilieren Sie die Shader.</span><span class="sxs-lookup"><span data-stu-id="538cb-146">Compile the shaders.</span></span>
    -   <span data-ttu-id="538cb-147">Erstellen Sie das Vertex-Eingabe Layout.</span><span class="sxs-lookup"><span data-stu-id="538cb-147">Create the vertex input layout.</span></span>
    -   <span data-ttu-id="538cb-148">Erstellen Sie eine Beschreibung des [Pipeline Zustands Objekts](managing-graphics-pipeline-state-in-direct3d-12.md) , und erstellen Sie dann das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="538cb-148">Create a [pipeline state object](managing-graphics-pipeline-state-in-direct3d-12.md) description, then create the object.</span></span>
        > [!Note]  
        > <span data-ttu-id="538cb-149">Ein Pipeline Zustands Objekt verwaltet den Status aller aktuell festgelegten Shader sowie bestimmter fester Funktions Zustands Objekte (z. b. den *Eingabe Assembler*, den *tesselator*, den *Raster* und die *Ausgabe* Zusammenführung).</span><span class="sxs-lookup"><span data-stu-id="538cb-149">A pipeline state object maintains the state of all currently set shaders as well as certain fixed function state objects (such as the *input assembler*, *tesselator*, *rasterizer* and *output merger*).</span></span>

    -   <span data-ttu-id="538cb-150">Erstellen Sie die Befehlsliste.</span><span class="sxs-lookup"><span data-stu-id="538cb-150">Create the command list.</span></span>
    -   <span data-ttu-id="538cb-151">Schließen Sie die Befehlsliste.</span><span class="sxs-lookup"><span data-stu-id="538cb-151">Close the command list.</span></span>
    -   <span data-ttu-id="538cb-152">Erstellen und laden Sie die Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="538cb-152">Create and load the vertex buffers.</span></span>
    -   <span data-ttu-id="538cb-153">Erstellen Sie die Vertex-Puffer Ansichten.</span><span class="sxs-lookup"><span data-stu-id="538cb-153">Create the vertex buffer views.</span></span>
    -   <span data-ttu-id="538cb-154">Erstellen Sie einen Fence.</span><span class="sxs-lookup"><span data-stu-id="538cb-154">Create a fence.</span></span>
        > [!Note]  
        > <span data-ttu-id="538cb-155">Ein Fence wird verwendet, um die CPU mit der GPU zu synchronisieren (Weitere Informationen finden Sie unter [Synchronisierung mit mehreren](./user-mode-heap-synchronization.md)Modulen).</span><span class="sxs-lookup"><span data-stu-id="538cb-155">A fence is used to synchronize the CPU with the GPU (see [Multi-engine synchronization](./user-mode-heap-synchronization.md)).</span></span>

    -   <span data-ttu-id="538cb-156">Erstellen Sie ein Ereignis handle.</span><span class="sxs-lookup"><span data-stu-id="538cb-156">Create an event handle.</span></span>
    -   <span data-ttu-id="538cb-157">Warten Sie, bis die GPU abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="538cb-157">Wait for the GPU to finish.</span></span>
        > [!Note]  
        > <span data-ttu-id="538cb-158">Überprüfen Sie den Fence!</span><span class="sxs-lookup"><span data-stu-id="538cb-158">Check on the fence!</span></span>

<span data-ttu-id="538cb-159">Weitere Informationen finden Sie in den [Klassen D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [loadpipeline](#loadpipeline) und [loadassets](#loadassets).</span><span class="sxs-lookup"><span data-stu-id="538cb-159">Refer to [class D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [LoadPipeline](#loadpipeline) and [LoadAssets](#loadassets).</span></span>

### <a name="update"></a><span data-ttu-id="538cb-160">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="538cb-160">Update</span></span>

<span data-ttu-id="538cb-161">Aktualisieren Sie alle Elemente, die sich seit dem letzten Frame ändern sollten.</span><span class="sxs-lookup"><span data-stu-id="538cb-161">Update everything that should change since the last frame.</span></span>

-   <span data-ttu-id="538cb-162">Ändern Sie nach Bedarf die Konstante, den Scheitelpunkt, Index Puffer und alles andere.</span><span class="sxs-lookup"><span data-stu-id="538cb-162">Modify the constant, vertex, index buffers, and everything else, as necessary.</span></span>

<span data-ttu-id="538cb-163">Weitere Informationen finden Sie unter [OnUpdate](#onupdate).</span><span class="sxs-lookup"><span data-stu-id="538cb-163">Refer to [OnUpdate](#onupdate).</span></span>

### <a name="render"></a><span data-ttu-id="538cb-164">Rendern</span><span class="sxs-lookup"><span data-stu-id="538cb-164">Render</span></span>

<span data-ttu-id="538cb-165">Zeichnen Sie die neue Welt.</span><span class="sxs-lookup"><span data-stu-id="538cb-165">Draw the new world.</span></span>

-   <span data-ttu-id="538cb-166">Füllt die Befehlsliste auf.</span><span class="sxs-lookup"><span data-stu-id="538cb-166">Populate the command list.</span></span>
    -   <span data-ttu-id="538cb-167">Setzt die Zuweisung der Befehlsliste zurück.</span><span class="sxs-lookup"><span data-stu-id="538cb-167">Reset the command list allocator.</span></span>
        > [!Note]  
        > <span data-ttu-id="538cb-168">Verwenden Sie den Speicher, der mit der Befehls Zuweisung verknüpft ist, erneut.</span><span class="sxs-lookup"><span data-stu-id="538cb-168">Re-use the memory that is associated with the command allocator.</span></span>

         

    -   <span data-ttu-id="538cb-169">Setzen Sie die Befehlsliste zurück.</span><span class="sxs-lookup"><span data-stu-id="538cb-169">Reset the command list.</span></span>
    -   <span data-ttu-id="538cb-170">Legen Sie die Grafik Stamm Signatur fest.</span><span class="sxs-lookup"><span data-stu-id="538cb-170">Set the graphics root signature.</span></span>
        > [!Note]  
        > <span data-ttu-id="538cb-171">Legt die Grafik Stamm Signatur fest, die für die aktuelle Befehlsliste verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="538cb-171">Sets the graphics root signature to use for the current command list.</span></span>

         

    -   <span data-ttu-id="538cb-172">Legen Sie die Rechtecke Viewport und Scheren fest.</span><span class="sxs-lookup"><span data-stu-id="538cb-172">Set the viewport and scissor rectangles.</span></span>
    -   <span data-ttu-id="538cb-173">Legen Sie eine Ressourcengrenze fest, die angibt, dass der Hintergrund Puffer als Renderziel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="538cb-173">Set a resource barrier, indicating the back buffer is to be used as a render target.</span></span>
        > [!Note]  
        > <span data-ttu-id="538cb-174">Ressourcen Barrieren werden verwendet, um Ressourcen Übergänge zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="538cb-174">Resource barriers are used to manage resource transitions.</span></span>

         

    -   <span data-ttu-id="538cb-175">Aufzeichnen von Befehlen in der Befehlsliste.</span><span class="sxs-lookup"><span data-stu-id="538cb-175">Record commands into the command list.</span></span>
    -   <span data-ttu-id="538cb-176">Gibt an, dass der Hintergrund Puffer nach der Ausführung der Befehlsliste verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="538cb-176">Indicate the back buffer will be used to present after the command list has executed.</span></span>
        > [!Note]  
        > <span data-ttu-id="538cb-177">Ein weiterer Rückruf zum Festlegen einer Ressourcen Barriere.</span><span class="sxs-lookup"><span data-stu-id="538cb-177">Another call to set a resource barrier.</span></span>

         

    -   <span data-ttu-id="538cb-178">Schließen Sie die Befehlsliste, um die Aufzeichnung zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="538cb-178">Close the command list to further recording.</span></span>
-   <span data-ttu-id="538cb-179">Führen Sie die Befehlsliste aus.</span><span class="sxs-lookup"><span data-stu-id="538cb-179">Execute the command list.</span></span>
-   <span data-ttu-id="538cb-180">Stellen Sie den Frame dar.</span><span class="sxs-lookup"><span data-stu-id="538cb-180">Present the frame.</span></span>
-   <span data-ttu-id="538cb-181">Warten Sie, bis die GPU abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="538cb-181">Wait for the GPU to finish.</span></span>
    > [!Note]  
    > <span data-ttu-id="538cb-182">Aktualisieren und überprüfen Sie den Fence.</span><span class="sxs-lookup"><span data-stu-id="538cb-182">Keep updating and checking the fence.</span></span>

<span data-ttu-id="538cb-183">Weitere Informationen finden Sie unter [onrendering](#onrender).</span><span class="sxs-lookup"><span data-stu-id="538cb-183">Refer to [OnRender](#onrender).</span></span>

### <a name="destroy"></a><span data-ttu-id="538cb-184">Zerstören</span><span class="sxs-lookup"><span data-stu-id="538cb-184">Destroy</span></span>

<span data-ttu-id="538cb-185">Schließen Sie die APP ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="538cb-185">Cleanly close down the app.</span></span>

-   <span data-ttu-id="538cb-186">Warten Sie, bis die GPU abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="538cb-186">Wait for the GPU to finish.</span></span>
    > [!Note]  
    > <span data-ttu-id="538cb-187">Abschließende Prüfung am Fence.</span><span class="sxs-lookup"><span data-stu-id="538cb-187">Final check on the fence.</span></span>

-   <span data-ttu-id="538cb-188">Schließen Sie das Ereignis handle.</span><span class="sxs-lookup"><span data-stu-id="538cb-188">Close the event handle.</span></span>

<span data-ttu-id="538cb-189">Weitere Informationen finden Sie unter [OnDestroy](#ondestroy).</span><span class="sxs-lookup"><span data-stu-id="538cb-189">Refer to [OnDestroy](#ondestroy).</span></span>

## <a name="code-example-for-a-simple-app"></a><span data-ttu-id="538cb-190">Code Beispiel für eine einfache APP</span><span class="sxs-lookup"><span data-stu-id="538cb-190">Code example for a simple app</span></span>

<span data-ttu-id="538cb-191">Im folgenden wird der Code Abschnitt erweitert, um den für ein einfaches Beispiel erforderlichen Code einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="538cb-191">The following expands the code flow above to include the code required for a basic sample.</span></span>

### <a name="class-d3d12hellotriangle"></a><span data-ttu-id="538cb-192">Class D3D12HelloTriangle</span><span class="sxs-lookup"><span data-stu-id="538cb-192">class D3D12HelloTriangle</span></span>

<span data-ttu-id="538cb-193">Definieren Sie zunächst die-Klasse in einer Header Datei, einschließlich eines Viewports, Scheren-Rechtecks und Scheitelpunkt Puffers mithilfe der-Strukturen:</span><span class="sxs-lookup"><span data-stu-id="538cb-193">First define the class in a header file, including a viewport, scissor rectangle and vertex buffer using the structures:</span></span>

-   [<span data-ttu-id="538cb-194">**D3D12 \_ Viewport**</span><span class="sxs-lookup"><span data-stu-id="538cb-194">**D3D12\_VIEWPORT**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport)
-   [<span data-ttu-id="538cb-195">**D3D12 \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="538cb-195">**D3D12\_RECT**</span></span>](d3d12-rect.md)
-   [<span data-ttu-id="538cb-196">**D3D12 \_ Vertex- \_ Puffer \_ Ansicht**</span><span class="sxs-lookup"><span data-stu-id="538cb-196">**D3D12\_VERTEX\_BUFFER\_VIEW**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)

```cpp
#include "DXSample.h"

using namespace DirectX;
using namespace Microsoft::WRL;

class D3D12HelloTriangle : public DXSample
{
public:
    D3D12HelloTriangle(UINT width, UINT height, std::wstring name);

    virtual void OnInit();
    virtual void OnUpdate();
    virtual void OnRender();
    virtual void OnDestroy();

private:
    static const UINT FrameCount = 2;

    struct Vertex
    {
        XMFLOAT3 position;
        XMFLOAT4 color;
    };

    // Pipeline objects.
    D3D12_VIEWPORT m_viewport;
    D3D12_RECT m_scissorRect;
    ComPtr<IDXGISwapChain3> m_swapChain;
    ComPtr<ID3D12Device> m_device;
    ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
    ComPtr<ID3D12CommandAllocator> m_commandAllocator;
    ComPtr<ID3D12CommandQueue> m_commandQueue;
    ComPtr<ID3D12RootSignature> m_rootSignature;
    ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
    ComPtr<ID3D12PipelineState> m_pipelineState;
    ComPtr<ID3D12GraphicsCommandList> m_commandList;
    UINT m_rtvDescriptorSize;

    // App resources.
    ComPtr<ID3D12Resource> m_vertexBuffer;
    D3D12_VERTEX_BUFFER_VIEW m_vertexBufferView;

    // Synchronization objects.
    UINT m_frameIndex;
    HANDLE m_fenceEvent;
    ComPtr<ID3D12Fence> m_fence;
    UINT64 m_fenceValue;

    void LoadPipeline();
    void LoadAssets();
    void PopulateCommandList();
    void WaitForPreviousFrame();
};
```

### <a name="oninit"></a><span data-ttu-id="538cb-197">OnInit ()</span><span class="sxs-lookup"><span data-stu-id="538cb-197">OnInit()</span></span>

<span data-ttu-id="538cb-198">Beginnen Sie in der Haupt Quelldatei des Projekts mit dem Initialisieren der Objekte:</span><span class="sxs-lookup"><span data-stu-id="538cb-198">In the projects main source file, start initializing the objects:</span></span>

```cpp
void D3D12HelloTriangle::OnInit()
{
    LoadPipeline();
    LoadAssets();
}
```

### <a name="loadpipeline"></a><span data-ttu-id="538cb-199">Loadpipeline ()</span><span class="sxs-lookup"><span data-stu-id="538cb-199">LoadPipeline()</span></span>

<span data-ttu-id="538cb-200">Der folgende Code erstellt die Grundlagen für eine Grafik Pipeline.</span><span class="sxs-lookup"><span data-stu-id="538cb-200">The following code creates the basics for a graphics pipeline.</span></span> <span data-ttu-id="538cb-201">Der Prozess zum Erstellen von Geräten und Austauschen von Ketten ähnelt Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="538cb-201">The process of creating devices and swap chains is very similar to Direct3D 11.</span></span>

-   <span data-ttu-id="538cb-202">Aktivieren Sie die Debugebene mit Aufrufen von:</span><span class="sxs-lookup"><span data-stu-id="538cb-202">Enable the debug layer, with calls to:</span></span><dl>

[<span data-ttu-id="538cb-203">**D3D12GetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="538cb-203">**D3D12GetDebugInterface**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12getdebuginterface)  
    [<span data-ttu-id="538cb-204">**ID3D12Debug:: enabledebuglayer**</span><span class="sxs-lookup"><span data-stu-id="538cb-204">**ID3D12Debug::EnableDebugLayer**</span></span>](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)  
    </dl>
-   <span data-ttu-id="538cb-205">Erstellen Sie das Gerät:</span><span class="sxs-lookup"><span data-stu-id="538cb-205">Create the device:</span></span><dl>

[<span data-ttu-id="538cb-206">**CreateDXGIFactory1**</span><span class="sxs-lookup"><span data-stu-id="538cb-206">**CreateDXGIFactory1**</span></span>](/windows/win32/api/dxgi/nf-dxgi-createdxgifactory1)  
    [<span data-ttu-id="538cb-207">**D3D12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="538cb-207">**D3D12CreateDevice**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)  
    </dl>
-   <span data-ttu-id="538cb-208">Füllen Sie die Beschreibung einer Befehls Warteschlange aus, und erstellen Sie die Befehls Warteschlange</span><span class="sxs-lookup"><span data-stu-id="538cb-208">Fill out a command queue description, then create the command queue:</span></span><dl>

[<span data-ttu-id="538cb-209">**D3D12 \_ Befehls \_ Warteschlange entfernen \_**</span><span class="sxs-lookup"><span data-stu-id="538cb-209">**D3D12\_COMMAND\_QUEUE\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)  
    [<span data-ttu-id="538cb-210">**ID3D12Device:: kreatecommandqueue**</span><span class="sxs-lookup"><span data-stu-id="538cb-210">**ID3D12Device::CreateCommandQueue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)  
    </dl>
-   <span data-ttu-id="538cb-211">Füllen Sie eine vorhandenes SwapChain-Beschreibung aus, und erstellen Sie dann die Swapkette:</span><span class="sxs-lookup"><span data-stu-id="538cb-211">Fill out a swapchain description, then create the swap chain:</span></span> <dl>

[<span data-ttu-id="538cb-212">**DXGI \_ - \_ SwapChain-Debug \_**</span><span class="sxs-lookup"><span data-stu-id="538cb-212">**DXGI\_SWAP\_CHAIN\_DESC**</span></span>](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)  
    [<span data-ttu-id="538cb-213">**Idxgifactory:: kreateswapchain**</span><span class="sxs-lookup"><span data-stu-id="538cb-213">**IDXGIFactory::CreateSwapChain**</span></span>](/windows/win32/api/dxgi/nf-dxgi-idxgifactory-createswapchain)  
    [<span data-ttu-id="538cb-214">**IDXGISwapChain3:: getcurrentbackbufferindex**</span><span class="sxs-lookup"><span data-stu-id="538cb-214">**IDXGISwapChain3::GetCurrentBackBufferIndex**</span></span>](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex)  
    </dl>
-   <span data-ttu-id="538cb-215">Füllen Sie eine Heap Beschreibung aus.</span><span class="sxs-lookup"><span data-stu-id="538cb-215">Fill out a heap description.</span></span> <span data-ttu-id="538cb-216">Erstellen Sie dann einen deskriptorheap:</span><span class="sxs-lookup"><span data-stu-id="538cb-216">then create a descriptor heap:</span></span> <dl>

[<span data-ttu-id="538cb-217">**D3D12 \_ \_ deskriptorheap- \_ decoeration**</span><span class="sxs-lookup"><span data-stu-id="538cb-217">**D3D12\_DESCRIPTOR\_HEAP\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)  
    [<span data-ttu-id="538cb-218">**ID3D12Device:: kreatedescriptorheap**</span><span class="sxs-lookup"><span data-stu-id="538cb-218">**ID3D12Device::CreateDescriptorHeap**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)  
    [<span data-ttu-id="538cb-219">**ID3D12Device:: getDescriptor handleinkrementsize**</span><span class="sxs-lookup"><span data-stu-id="538cb-219">**ID3D12Device::GetDescriptorHandleIncrementSize**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)  
    </dl>
-   <span data-ttu-id="538cb-220">Erstellen Sie die Ansicht des Renderziels:</span><span class="sxs-lookup"><span data-stu-id="538cb-220">Create the render target view:</span></span> <dl>

[<span data-ttu-id="538cb-221">**CD3DX12- \_ CPU- \_ \_ Deskriptorhandle**</span><span class="sxs-lookup"><span data-stu-id="538cb-221">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE**</span></span>](cd3dx12-cpu-descriptor-handle.md)  
    [<span data-ttu-id="538cb-222">**Getcpudescriptor Lenker forheapstart**</span><span class="sxs-lookup"><span data-stu-id="538cb-222">**GetCPUDescriptorHandleForHeapStart**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [<span data-ttu-id="538cb-223">**Idxgiswapchain:: GetBuffer**</span><span class="sxs-lookup"><span data-stu-id="538cb-223">**IDXGISwapChain::GetBuffer**</span></span>](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)  
    [<span data-ttu-id="538cb-224">**ID3D12Device:: kreaterendertargetview**</span><span class="sxs-lookup"><span data-stu-id="538cb-224">**ID3D12Device::CreateRenderTargetView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)  
    </dl>
-   <span data-ttu-id="538cb-225">Erstellen Sie die Befehls Zuweisung: [**ID3D12Device:: kreatecommandzuweisung**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).</span><span class="sxs-lookup"><span data-stu-id="538cb-225">Create the command allocator: [**ID3D12Device::CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).</span></span>

<span data-ttu-id="538cb-226">In späteren Schritten werden Befehlslisten von der Befehls Zuweisung abgerufen und an die Befehls Warteschlange übermittelt.</span><span class="sxs-lookup"><span data-stu-id="538cb-226">In later steps, command lists are obtained from the command allocator and submitted to the command queue.</span></span>

<span data-ttu-id="538cb-227">Laden der Rendering-Pipeline Abhängigkeiten (Beachten Sie, dass die Erstellung eines Software Warp-Geräts vollständig optional ist).</span><span class="sxs-lookup"><span data-stu-id="538cb-227">Load the rendering pipeline dependencies (note that the creation of a software WARP device is entirely optional).</span></span>


```cpp
void D3D12HelloTriangle::LoadPipeline()
{
#if defined(_DEBUG)
    // Enable the D3D12 debug layer.
    {
        
        ComPtr<ID3D12Debug> debugController;
        if (SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&debugController))))
        {
            debugController->EnableDebugLayer();
        }
    }
#endif

    ComPtr<IDXGIFactory4> factory;
    ThrowIfFailed(CreateDXGIFactory1(IID_PPV_ARGS(&factory)));

    if (m_useWarpDevice)
    {
        ComPtr<IDXGIAdapter> warpAdapter;
        ThrowIfFailed(factory->EnumWarpAdapter(IID_PPV_ARGS(&warpAdapter)));

        ThrowIfFailed(D3D12CreateDevice(
            warpAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }
    else
    {
        ComPtr<IDXGIAdapter1> hardwareAdapter;
        GetHardwareAdapter(factory.Get(), &hardwareAdapter);

        ThrowIfFailed(D3D12CreateDevice(
            hardwareAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }

    // Describe and create the command queue.
    D3D12_COMMAND_QUEUE_DESC queueDesc = {};
    queueDesc.Flags = D3D12_COMMAND_QUEUE_FLAG_NONE;
    queueDesc.Type = D3D12_COMMAND_LIST_TYPE_DIRECT;

    ThrowIfFailed(m_device->CreateCommandQueue(&queueDesc, IID_PPV_ARGS(&m_commandQueue)));

    // Describe and create the swap chain.
    DXGI_SWAP_CHAIN_DESC swapChainDesc = {};
    swapChainDesc.BufferCount = FrameCount;
    swapChainDesc.BufferDesc.Width = m_width;
    swapChainDesc.BufferDesc.Height = m_height;
    swapChainDesc.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
    swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
    swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_DISCARD;
    swapChainDesc.OutputWindow = Win32Application::GetHwnd();
    swapChainDesc.SampleDesc.Count = 1;
    swapChainDesc.Windowed = TRUE;

    ComPtr<IDXGISwapChain> swapChain;
    ThrowIfFailed(factory->CreateSwapChain(
        m_commandQueue.Get(),        // Swap chain needs the queue so that it can force a flush on it.
        &swapChainDesc,
        &swapChain
        ));

    ThrowIfFailed(swapChain.As(&m_swapChain));

    // This sample does not support fullscreen transitions.
    ThrowIfFailed(factory->MakeWindowAssociation(Win32Application::GetHwnd(), DXGI_MWA_NO_ALT_ENTER));

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();

    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);
            rtvHandle.Offset(1, m_rtvDescriptorSize);
        }
    }

    ThrowIfFailed(m_device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocator)));
}
```



### <a name="loadassets"></a><span data-ttu-id="538cb-228">Loadassets ()</span><span class="sxs-lookup"><span data-stu-id="538cb-228">LoadAssets()</span></span>

<span data-ttu-id="538cb-229">Das Laden und Vorbereiten von Assets ist ein langwieriger Prozess.</span><span class="sxs-lookup"><span data-stu-id="538cb-229">Loading and preparing assets is a lengthy process.</span></span> <span data-ttu-id="538cb-230">Viele dieser Phasen ähneln D3D 11, aber einige sind neu in D3D 12.</span><span class="sxs-lookup"><span data-stu-id="538cb-230">Many of these stages are similar to D3D 11, though some are new to D3D 12.</span></span>

<span data-ttu-id="538cb-231">In Direct3D 12 wird der erforderliche Pipeline Status über ein [Pipeline Zustands Objekt](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO) an eine Befehlsliste angefügt.</span><span class="sxs-lookup"><span data-stu-id="538cb-231">In Direct3D 12, required pipeline state is attached to a command list via a [pipeline state object](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO).</span></span> <span data-ttu-id="538cb-232">Dieses Beispiel zeigt, wie ein PSO erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="538cb-232">This example shows how to create a PSO.</span></span> <span data-ttu-id="538cb-233">Sie können die PSO als Element Variable speichern und Sie so oft wie nötig wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="538cb-233">You can store the PSO as a member variable and reuse it as many times as needed.</span></span>

<span data-ttu-id="538cb-234">Ein deskriptorheap definiert die Sichten und den Zugriff auf Ressourcen (z. b. eine renderzielansicht).</span><span class="sxs-lookup"><span data-stu-id="538cb-234">A descriptor heap defines the views and how to access resources (for example, a render target view).</span></span>

<span data-ttu-id="538cb-235">Mit der Befehlslisten Zuweisung und PSO können Sie die tatsächliche Befehlsliste erstellen, die zu einem späteren Zeitpunkt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="538cb-235">With the command list allocator and PSO, you can create the actual command list, which will be executed at a later time.</span></span>

<span data-ttu-id="538cb-236">Die folgenden APIs und Prozesse werden nacheinander aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="538cb-236">The following APIs and processes are called in succession.</span></span>

-   <span data-ttu-id="538cb-237">Erstellen Sie eine leere Stamm Signatur, indem Sie die verfügbare hilfsstruktur verwenden:</span><span class="sxs-lookup"><span data-stu-id="538cb-237">Create an empty root signature, using the available helper structure:</span></span> <dl>

[<span data-ttu-id="538cb-238">**CD3DX12 \_ Stamm \_ Signatur \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="538cb-238">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md)  
    [<span data-ttu-id="538cb-239">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="538cb-239">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)  
    [<span data-ttu-id="538cb-240">**ID3D12Device:: kreaterootsignature**</span><span class="sxs-lookup"><span data-stu-id="538cb-240">**ID3D12Device::CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)  
    </dl>
-   <span data-ttu-id="538cb-241">Laden und kompilieren Sie die Shader: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).</span><span class="sxs-lookup"><span data-stu-id="538cb-241">Load and compile the shaders: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).</span></span>
-   <span data-ttu-id="538cb-242">Erstellen Sie das Vertex-Eingabe Layout: [**D3D12 \_ input \_ Element \_ ensc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="538cb-242">Create the vertex input layout: [**D3D12\_INPUT\_ELEMENT\_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).</span></span>
-   <span data-ttu-id="538cb-243">Geben Sie eine Beschreibung des Pipeline Zustands ein, verwenden Sie die verfügbaren Hilfsstrukturen, und erstellen Sie dann den Status der Grafik Pipeline:</span><span class="sxs-lookup"><span data-stu-id="538cb-243">Fill out a pipeline state description, using the helper structures available, then create the graphics pipeline state:</span></span> <dl>

[<span data-ttu-id="538cb-244">**D3D12- \_ Grafik \_ Pipeline \_ Status \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="538cb-244">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)  
    [<span data-ttu-id="538cb-245">**CD3DX12 \_ Rasterizer- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="538cb-245">**CD3DX12\_RASTERIZER\_DESC**</span></span>](cd3dx12-rasterizer-desc.md)  
    [<span data-ttu-id="538cb-246">**CD3DX12 \_ Blend- \_ Entsc**</span><span class="sxs-lookup"><span data-stu-id="538cb-246">**CD3DX12\_BLEND\_DESC**</span></span>](cd3dx12-blend-desc.md)  
    [<span data-ttu-id="538cb-247">**ID3D12Device:: kreategraphicspipelinestate**</span><span class="sxs-lookup"><span data-stu-id="538cb-247">**ID3D12Device::CreateGraphicsPipelineState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)  
    </dl>
-   <span data-ttu-id="538cb-248">Erstellen und schließen Sie eine Befehlsliste:</span><span class="sxs-lookup"><span data-stu-id="538cb-248">Create, then close, a command list:</span></span> <dl>

[<span data-ttu-id="538cb-249">**ID3D12Device:: kreatecommandlist**</span><span class="sxs-lookup"><span data-stu-id="538cb-249">**ID3D12Device::CreateCommandList**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)  
    [<span data-ttu-id="538cb-250">**ID3D12GraphicsCommandList:: Close**</span><span class="sxs-lookup"><span data-stu-id="538cb-250">**ID3D12GraphicsCommandList::Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)  
    </dl>
-   <span data-ttu-id="538cb-251">Erstellen Sie den Vertex-Puffer: [**ID3D12Device:: | atecommittedresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="538cb-251">Create the vertex buffer: [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>
-   <span data-ttu-id="538cb-252">Kopieren Sie die Scheitelpunkt Daten in den Vertex-Puffer:</span><span class="sxs-lookup"><span data-stu-id="538cb-252">Copy the vertex data to the vertex buffer:</span></span><dl>

[<span data-ttu-id="538cb-253">**ID3D12Resource:: map**</span><span class="sxs-lookup"><span data-stu-id="538cb-253">**ID3D12Resource::Map**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)  
    [<span data-ttu-id="538cb-254">**ID3D12Resource:: unmap**</span><span class="sxs-lookup"><span data-stu-id="538cb-254">**ID3D12Resource::Unmap**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-unmap)  
    </dl>
-   <span data-ttu-id="538cb-255">Initialisieren Sie die Vertex-Puffer Ansicht: [**getgpuvirtualaddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).</span><span class="sxs-lookup"><span data-stu-id="538cb-255">Initialize the vertex buffer view: [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).</span></span>
-   <span data-ttu-id="538cb-256">Erstellen und initialisieren Sie den Fence: [**ID3D12Device:: kreatefence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).</span><span class="sxs-lookup"><span data-stu-id="538cb-256">Create and initialize the fence: [**ID3D12Device::CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).</span></span>
-   <span data-ttu-id="538cb-257">Erstellen Sie ein Ereignis Handle für die Verwendung mit der Rahmen Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="538cb-257">Create an event handle for use with frame synchronization.</span></span>
-   <span data-ttu-id="538cb-258">Warten Sie, bis die GPU abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="538cb-258">Wait for the GPU to finish.</span></span>


```cpp
void D3D12HelloTriangle::LoadAssets()
{
    // Create an empty root signature.
    {
        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }

    // Create the pipeline state, which includes compiling and loading shaders.
    {
        ComPtr<ID3DBlob> vertexShader;
        ComPtr<ID3DBlob> pixelShader;

#if defined(_DEBUG)
        // Enable better shader debugging with the graphics debugging tools.
        UINT compileFlags = D3DCOMPILE_DEBUG | D3DCOMPILE_SKIP_OPTIMIZATION;
#else
        UINT compileFlags = 0;
#endif

        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "VSMain", "vs_5_0", compileFlags, 0, &vertexShader, nullptr));
        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "PSMain", "ps_5_0", compileFlags, 0, &pixelShader, nullptr));

        // Define the vertex input layout.
        D3D12_INPUT_ELEMENT_DESC inputElementDescs[] =
        {
            { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 },
            { "COLOR", 0, DXGI_FORMAT_R32G32B32A32_FLOAT, 0, 12, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 }
        };

        // Describe and create the graphics pipeline state object (PSO).
        D3D12_GRAPHICS_PIPELINE_STATE_DESC psoDesc = {};
        psoDesc.InputLayout = { inputElementDescs, _countof(inputElementDescs) };
        psoDesc.pRootSignature = m_rootSignature.Get();
        psoDesc.VS = { reinterpret_cast<UINT8*>(vertexShader->GetBufferPointer()), vertexShader->GetBufferSize() };
        psoDesc.PS = { reinterpret_cast<UINT8*>(pixelShader->GetBufferPointer()), pixelShader->GetBufferSize() };
        psoDesc.RasterizerState = CD3DX12_RASTERIZER_DESC(D3D12_DEFAULT);
        psoDesc.BlendState = CD3DX12_BLEND_DESC(D3D12_DEFAULT);
        psoDesc.DepthStencilState.DepthEnable = FALSE;
        psoDesc.DepthStencilState.StencilEnable = FALSE;
        psoDesc.SampleMask = UINT_MAX;
        psoDesc.PrimitiveTopologyType = D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE;
        psoDesc.NumRenderTargets = 1;
        psoDesc.RTVFormats[0] = DXGI_FORMAT_R8G8B8A8_UNORM;
        psoDesc.SampleDesc.Count = 1;
        ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_pipelineState)));
    }

    // Create the command list.
    ThrowIfFailed(m_device->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), m_pipelineState.Get(), IID_PPV_ARGS(&m_commandList)));

    // Command lists are created in the recording state, but there is nothing
    // to record yet. The main loop expects it to be closed, so close it now.
    ThrowIfFailed(m_commandList->Close());

    // Create the vertex buffer.
    {
        // Define the geometry for a triangle.
        Vertex triangleVertices[] =
        {
            { { 0.0f, 0.25f * m_aspectRatio, 0.0f }, { 1.0f, 0.0f, 0.0f, 1.0f } },
            { { 0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 1.0f, 0.0f, 1.0f } },
            { { -0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 0.0f, 1.0f, 1.0f } }
        };

        const UINT vertexBufferSize = sizeof(triangleVertices);

        // Note: using upload heaps to transfer static data like vert buffers is not 
        // recommended. Every time the GPU needs it, the upload heap will be marshalled 
        // over. Please read up on Default Heap usage. An upload heap is used here for 
        // code simplicity and because there are very few verts to actually transfer.
        CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_UPLOAD);
        auto desc = CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize);
        ThrowIfFailed(m_device->CreateCommittedResource(
            &heapProps,
            D3D12_HEAP_FLAG_NONE,
            &desc,
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBuffer)));

        // Copy the triangle data to the vertex buffer.
        UINT8* pVertexDataBegin;
        CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
        ThrowIfFailed(m_vertexBuffer->Map(0, &readRange, reinterpret_cast<void**>(&pVertexDataBegin)));
        memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
        m_vertexBuffer->Unmap(0, nullptr);

        // Initialize the vertex buffer view.
        m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
        m_vertexBufferView.StrideInBytes = sizeof(Vertex);
        m_vertexBufferView.SizeInBytes = vertexBufferSize;
    }

    // Create synchronization objects and wait until assets have been uploaded to the GPU.
    {
        ThrowIfFailed(m_device->CreateFence(0, D3D12_FENCE_FLAG_NONE, IID_PPV_ARGS(&m_fence)));
        m_fenceValue = 1;

        // Create an event handle to use for frame synchronization.
        m_fenceEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);
        if (m_fenceEvent == nullptr)
        {
            ThrowIfFailed(HRESULT_FROM_WIN32(GetLastError()));
        }

        // Wait for the command list to execute; we are reusing the same command 
        // list in our main loop but for now, we just want to wait for setup to 
        // complete before continuing.
        WaitForPreviousFrame();
    }
}
```



### <a name="onupdate"></a><span data-ttu-id="538cb-259">OnUpdate ()</span><span class="sxs-lookup"><span data-stu-id="538cb-259">OnUpdate()</span></span>

<span data-ttu-id="538cb-260">Für ein einfaches Beispiel wird nichts aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="538cb-260">For a simple example, nothing is updated.</span></span>


```cpp
void D3D12HelloTriangle::OnUpdate()

{
}
```



### <a name="onrender"></a><span data-ttu-id="538cb-261">Onrendering ()</span><span class="sxs-lookup"><span data-stu-id="538cb-261">OnRender()</span></span>

<span data-ttu-id="538cb-262">Während der Einrichtung wurde die Element Variable **m \_ CommandList** verwendet, um alle Setup Befehle aufzuzeichnen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="538cb-262">During set up, the member variable **m\_commandList** was used to record and execute all of the set up commands.</span></span> <span data-ttu-id="538cb-263">Sie können diesen Member nun in der Haupt-Renderschleife wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="538cb-263">You can now reuse that member in the main render loop.</span></span>

<span data-ttu-id="538cb-264">Das Rendering umfasst einen aufzurufenden Befehl zum Auffüllen der Befehlsliste. Anschließend kann die Befehlsliste ausgeführt und der nächste Puffer in der SwapChain angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="538cb-264">Rendering involves a call to populate the command list, then the command list can be executed and the next buffer in the swap chain presented:</span></span>

-   <span data-ttu-id="538cb-265">Füllt die Befehlsliste auf.</span><span class="sxs-lookup"><span data-stu-id="538cb-265">Populate the command list.</span></span>
-   <span data-ttu-id="538cb-266">Führen Sie die Befehlsliste aus: [**ID3D12CommandQueue:: executecommandlists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span><span class="sxs-lookup"><span data-stu-id="538cb-266">Execute the command list: [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span></span>
-   <span data-ttu-id="538cb-267">[**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) der Frame.</span><span class="sxs-lookup"><span data-stu-id="538cb-267">[**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) the frame.</span></span>
-   <span data-ttu-id="538cb-268">Warten Sie, bis die GPU abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="538cb-268">Wait on the GPU to finish.</span></span>


```cpp
void D3D12HelloTriangle::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(1, 0));

    WaitForPreviousFrame();
}
```



### <a name="populatecommandlist"></a><span data-ttu-id="538cb-269">Populatecommandlist ()</span><span class="sxs-lookup"><span data-stu-id="538cb-269">PopulateCommandList()</span></span>

<span data-ttu-id="538cb-270">Sie müssen die Zuweisung der Befehlsliste und die Befehlsliste selbst zurücksetzen, bevor Sie Sie wieder verwenden können.</span><span class="sxs-lookup"><span data-stu-id="538cb-270">You must reset the command list allocator and the command list itself before you can reuse them.</span></span> <span data-ttu-id="538cb-271">In komplexeren Szenarien kann es sinnvoll sein, die Zuweisung jedes Paar Frames zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="538cb-271">In more advanced scenarios it might make sense to reset the allocator every several frames.</span></span> <span data-ttu-id="538cb-272">Der Arbeitsspeicher ist mit der Zuweisung verknüpft, die nicht sofort nach dem Ausführen einer Befehlsliste freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="538cb-272">Memory is associated with the allocator that can't be released immediately after executing a command list.</span></span> <span data-ttu-id="538cb-273">Dieses Beispiel zeigt, wie Sie die Zuweisung nach jedem Frame zurücksetzen können.</span><span class="sxs-lookup"><span data-stu-id="538cb-273">This example shows how to reset the allocator after every frame.</span></span>

<span data-ttu-id="538cb-274">Wieder verwenden Sie nun die Befehlsliste für den aktuellen Frame.</span><span class="sxs-lookup"><span data-stu-id="538cb-274">Now, reuse the command list for the current frame.</span></span> <span data-ttu-id="538cb-275">Fügen Sie den Viewport erneut an die Befehlsliste an (Dies muss immer erfolgen, wenn eine Befehlsliste zurückgesetzt wird und bevor die Befehlsliste ausgeführt wird). Geben Sie an, dass die Ressource als Renderziel verwendet werden soll, und geben Sie dann an, dass das Renderziel verwendet wird, wenn die Ausführung der Befehlsliste abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="538cb-275">Reattach the viewport to the command list (which must be done whenever a command list is reset, and before the command list is executed), indicate that the resource will be in use as a render target, record commands, and then indicate that the render target will be used to present when the command list is done executing.</span></span>

<span data-ttu-id="538cb-276">Beim Auffüllen von Befehlslisten werden wiederum die folgenden Methoden und Prozesse aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="538cb-276">Populating command lists calls the following methods and processes in turn:</span></span>

-   <span data-ttu-id="538cb-277">Zurücksetzen der Befehls Zuweisung und der Befehlsliste:</span><span class="sxs-lookup"><span data-stu-id="538cb-277">Reset the command allocator, and command list:</span></span> <dl>

[<span data-ttu-id="538cb-278">**ID3D12CommandAllocator:: Reset**</span><span class="sxs-lookup"><span data-stu-id="538cb-278">**ID3D12CommandAllocator::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)  
    [<span data-ttu-id="538cb-279">**ID3D12GraphicsCommandList:: Reset**</span><span class="sxs-lookup"><span data-stu-id="538cb-279">**ID3D12GraphicsCommandList::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)  
    </dl>
-   <span data-ttu-id="538cb-280">Legen Sie die Stamm Signatur, Viewport und Scheren Rechtecke fest:</span><span class="sxs-lookup"><span data-stu-id="538cb-280">Set the root signature, viewport and scissors rectangles:</span></span> <dl>

[<span data-ttu-id="538cb-281">**ID3D12GraphicsCommandList:: setgraphicsrootsignature**</span><span class="sxs-lookup"><span data-stu-id="538cb-281">**ID3D12GraphicsCommandList::SetGraphicsRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature)  
    [<span data-ttu-id="538cb-282">**ID3D12GraphicsCommandList:: rssetviewports**</span><span class="sxs-lookup"><span data-stu-id="538cb-282">**ID3D12GraphicsCommandList::RSSetViewports**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)  
    [<span data-ttu-id="538cb-283">**ID3D12GraphicsCommandList:: rssezcissorrects**</span><span class="sxs-lookup"><span data-stu-id="538cb-283">**ID3D12GraphicsCommandList::RSSetScissorRects**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)  
    </dl>
-   <span data-ttu-id="538cb-284">Geben Sie an, dass der Hintergrund Puffer als Renderziel verwendet werden soll:</span><span class="sxs-lookup"><span data-stu-id="538cb-284">Indicate that the back buffer is to be used as a render target:</span></span> <dl>

[<span data-ttu-id="538cb-285">**ID3D12GraphicsCommandList:: resourcebarrier**</span><span class="sxs-lookup"><span data-stu-id="538cb-285">**ID3D12GraphicsCommandList::ResourceBarrier**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)  
    [<span data-ttu-id="538cb-286">**ID3D12DescriptorHeap:: getcpudescriptor Lenker forheapstart**</span><span class="sxs-lookup"><span data-stu-id="538cb-286">**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [<span data-ttu-id="538cb-287">**ID3D12GraphicsCommandList:: omgtrendertargets**</span><span class="sxs-lookup"><span data-stu-id="538cb-287">**ID3D12GraphicsCommandList::OMSetRenderTargets**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)  
    </dl>
-   <span data-ttu-id="538cb-288">Aufzeichnen Sie die Befehle:</span><span class="sxs-lookup"><span data-stu-id="538cb-288">Record the commands:</span></span><dl>

[<span data-ttu-id="538cb-289">**ID3D12GraphicsCommandList:: clearrendertargetview**</span><span class="sxs-lookup"><span data-stu-id="538cb-289">**ID3D12GraphicsCommandList::ClearRenderTargetView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)  
    [<span data-ttu-id="538cb-290">**ID3D12GraphicsCommandList:: iasetprimitivetopology**</span><span class="sxs-lookup"><span data-stu-id="538cb-290">**ID3D12GraphicsCommandList::IASetPrimitiveTopology**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology)  
    [<span data-ttu-id="538cb-291">**ID3D12GraphicsCommandList:: iasetvertexbuffers**</span><span class="sxs-lookup"><span data-stu-id="538cb-291">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)  
    [<span data-ttu-id="538cb-292">**ID3D12GraphicsCommandList::D rawinstanzierte**</span><span class="sxs-lookup"><span data-stu-id="538cb-292">**ID3D12GraphicsCommandList::DrawInstanced**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)  
    </dl>
-   <span data-ttu-id="538cb-293">Gibt an, dass der Hintergrund Puffer nun verwendet wird, um Folgendes anzuzeigen: [**ID3D12GraphicsCommandList:: resourcebarriere**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="538cb-293">Indicate the back buffer will now be used to present: [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>
-   <span data-ttu-id="538cb-294">Schließen Sie die Befehlsliste: [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).</span><span class="sxs-lookup"><span data-stu-id="538cb-294">Close the command list: [**ID3D12GraphicsCommandList::Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).</span></span>


```cpp
void D3D12HelloTriangle::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated 
    // command lists have finished execution on the GPU; apps should use 
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocator->Reset());

    // However, when ExecuteCommandList() is called on a particular command 
    // list, that command list can then be reset at any time and must be before 
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocator.Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());
    m_commandList->RSSetViewports(1, &m_viewport);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET);
    m_commandList->ResourceBarrier(1, &barrier);

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);
    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->DrawInstanced(3, 1, 0, 0);

    // Indicate that the back buffer will now be used to present.
    barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT);
    m_commandList->ResourceBarrier(1, &barrier);

    ThrowIfFailed(m_commandList->Close());
}
```



### <a name="waitforpreviousframe"></a><span data-ttu-id="538cb-295">Waitforpreviousframe ()</span><span class="sxs-lookup"><span data-stu-id="538cb-295">WaitForPreviousFrame()</span></span>

<span data-ttu-id="538cb-296">Der folgende Code zeigt eine vereinfachte Verwendung von Zäunen.</span><span class="sxs-lookup"><span data-stu-id="538cb-296">The following code shows an over-simplified use of fences.</span></span>

> [!Note]  
> <span data-ttu-id="538cb-297">Das warten auf den Abschluss eines Frames ist für die meisten apps zu ineffizient.</span><span class="sxs-lookup"><span data-stu-id="538cb-297">Waiting for a frame to complete is too inefficient for most apps.</span></span>

 

<span data-ttu-id="538cb-298">Die folgenden APIs und Prozesse werden in der angegebenen Reihenfolge aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="538cb-298">The following APIs and processes are called in order:</span></span>

-   [<span data-ttu-id="538cb-299">**ID3D12CommandQueue:: Signal**</span><span class="sxs-lookup"><span data-stu-id="538cb-299">**ID3D12CommandQueue::Signal**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
-   [<span data-ttu-id="538cb-300">**ID3D12Fence:: getcompletedvalue**</span><span class="sxs-lookup"><span data-stu-id="538cb-300">**ID3D12Fence::GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)
-   [<span data-ttu-id="538cb-301">**ID3D12Fence:: Einstellungs Element**</span><span class="sxs-lookup"><span data-stu-id="538cb-301">**ID3D12Fence::SetEventOnCompletion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)
-   <span data-ttu-id="538cb-302">Warten Sie auf das-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="538cb-302">Wait for the event.</span></span>
-   <span data-ttu-id="538cb-303">Aktualisieren Sie den Frame Index: [**IDXGISwapChain3:: getcurrentbackbufferindex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).</span><span class="sxs-lookup"><span data-stu-id="538cb-303">Update the frame index: [**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).</span></span>


```cpp
void D3D12HelloTriangle::WaitForPreviousFrame()
{
    // WAITING FOR THE FRAME TO COMPLETE BEFORE CONTINUING IS NOT BEST PRACTICE.
    // This is code implemented as such for simplicity. More advanced samples 
    // illustrate how to use fences for efficient resource usage.

    // Signal and increment the fence value.
    const UINT64 fence = m_fenceValue;
    ThrowIfFailed(m_commandQueue->Signal(m_fence.Get(), fence));
    m_fenceValue++;

    // Wait until the previous frame is finished.
    if (m_fence->GetCompletedValue() < fence)
    {
        ThrowIfFailed(m_fence->SetEventOnCompletion(fence, m_fenceEvent));
        WaitForSingleObject(m_fenceEvent, INFINITE);
    }

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();
}
```



### <a name="ondestroy"></a><span data-ttu-id="538cb-304">OnDestroy ()</span><span class="sxs-lookup"><span data-stu-id="538cb-304">OnDestroy()</span></span>

<span data-ttu-id="538cb-305">Schließen Sie die APP ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="538cb-305">Cleanly close down the app.</span></span>

-   <span data-ttu-id="538cb-306">Warten Sie, bis die GPU abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="538cb-306">Wait for the GPU to finish.</span></span>
-   <span data-ttu-id="538cb-307">Schließen Sie das-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="538cb-307">Close the event.</span></span>


```cpp
void D3D12HelloTriangle::OnDestroy()
{

    // Wait for the GPU to be done with all resources.
    WaitForPreviousFrame();

    CloseHandle(m_fenceEvent);
}
```



## <a name="related-topics"></a><span data-ttu-id="538cb-308">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="538cb-308">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="538cb-309">Grundlegendes zu Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="538cb-309">Understanding Direct3D 12</span></span>](directx-12-getting-started.md)
</dt> <dt>

[<span data-ttu-id="538cb-310">Funktionierende Beispiele</span><span class="sxs-lookup"><span data-stu-id="538cb-310">Working Samples</span></span>](working-samples.md)
</dt> </dl>

 

 
