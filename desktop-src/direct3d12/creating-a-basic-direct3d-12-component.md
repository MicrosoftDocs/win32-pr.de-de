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
# <a name="creating-a-basic-direct3d-12-component"></a>Erstellen einer einfachen Direct3D 12-Komponente

> [!NOTE]
> Weitere Informationen zum Erstellen von Grafik intensiven Anwendungen für Windows 10 finden Sie im " [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) "-Repository für DirectX 12-Grafik Beispiele.

In diesem Thema wird der aufrufflow zum Erstellen einer grundlegenden Direct3D 12-Komponente beschrieben.

-   [Codefluss für eine einfache APP](#code-flow-for-a-simple-app)
    -   [Initialisieren](#initialize)
    -   [Aktualisieren](#update)
    -   [Render](#render)
    -   [Zerstören](#destroy)
-   [Code Beispiel für eine einfache APP](#code-example-for-a-simple-app)
    -   [Class D3D12HelloTriangle](#class-d3d12hellotriangle)
    -   [OnInit ()](#oninit)
    -   [Loadpipeline ()](#loadpipeline)
    -   [Loadassets ()](#loadassets)
    -   [OnUpdate ()](#onupdate)
    -   [Onrendering ()](#onrender)
    -   [Populatecommandlist ()](#populatecommandlist)
    -   [Waitforpreviousframe ()](#waitforpreviousframe)
    -   [OnDestroy ()](#ondestroy)
-   [Zugehörige Themen](#related-topics)

## <a name="code-flow-for-a-simple-app"></a>Codefluss für eine einfache APP

Die äußerste Schleife eines D3D 12-Programms folgt einem sehr standardmäßigen Grafik Prozess:

> [!TIP]
> Auf die neuen Funktionen von Direct3D 12 folgt ein Hinweis.

-   [Initialisieren](#initialize)
-   **Wiederholung**
    -   [Aktualisieren](#update)
    -   [Render](#render)
-   [Zerstören](#destroy)

### <a name="initialize"></a>Initialisieren

Bei der Initialisierung müssen zunächst die globalen Variablen und Klassen eingerichtet werden, und die Pipeline und die Assets müssen von einer Initialisierungsfunktion vorbereitet werden.

-   Initialisieren Sie die Pipeline.
    -   Aktivieren Sie die Debugebene.
    -   Erstellen Sie das Gerät.
    -   Erstellen Sie die Befehls Warteschlange.
    -   Erstellen Sie die Swapkette.
    -   Erstellen Sie einen RTV-deskriptorheap (renderzielansicht).
        > [!Note]  
        > Ein [deskriptorheap](descriptor-heaps.md) kann als ein Array von [Deskriptoren](descriptors.md)betrachtet werden. , Wobei jeder Deskriptor ein Objekt vollständig auf die GPU beschreibt.

    -   Erstellen von Frame Ressourcen (eine renderzielansicht für jeden Frame).
    -   Erstellen Sie eine Befehls Zuweisung.
        > [!Note]  
        > Ein Befehls Zuweiser verwaltet den zugrunde liegenden Speicher für [Befehlslisten und Pakete](recording-command-lists-and-bundles.md).
         
-   Initialisieren Sie die Objekte.
    -   Erstellen Sie eine leere Stamm Signatur.
        > [!Note]  
        > Eine Grafik Stamm [Signatur](root-signatures.md) definiert, welche Ressourcen an die Grafik Pipeline gebunden sind.

    -   Kompilieren Sie die Shader.
    -   Erstellen Sie das Vertex-Eingabe Layout.
    -   Erstellen Sie eine Beschreibung des [Pipeline Zustands Objekts](managing-graphics-pipeline-state-in-direct3d-12.md) , und erstellen Sie dann das-Objekt.
        > [!Note]  
        > Ein Pipeline Zustands Objekt verwaltet den Status aller aktuell festgelegten Shader sowie bestimmter fester Funktions Zustands Objekte (z. b. den *Eingabe Assembler*, den *tesselator*, den *Raster* und die *Ausgabe* Zusammenführung).

    -   Erstellen Sie die Befehlsliste.
    -   Schließen Sie die Befehlsliste.
    -   Erstellen und laden Sie die Scheitelpunkt Puffer.
    -   Erstellen Sie die Vertex-Puffer Ansichten.
    -   Erstellen Sie einen Fence.
        > [!Note]  
        > Ein Fence wird verwendet, um die CPU mit der GPU zu synchronisieren (Weitere Informationen finden Sie unter [Synchronisierung mit mehreren](./user-mode-heap-synchronization.md)Modulen).

    -   Erstellen Sie ein Ereignis handle.
    -   Warten Sie, bis die GPU abgeschlossen ist.
        > [!Note]  
        > Überprüfen Sie den Fence!

Weitere Informationen finden Sie in den [Klassen D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [loadpipeline](#loadpipeline) und [loadassets](#loadassets).

### <a name="update"></a>Aktualisieren

Aktualisieren Sie alle Elemente, die sich seit dem letzten Frame ändern sollten.

-   Ändern Sie nach Bedarf die Konstante, den Scheitelpunkt, Index Puffer und alles andere.

Weitere Informationen finden Sie unter [OnUpdate](#onupdate).

### <a name="render"></a>Rendern

Zeichnen Sie die neue Welt.

-   Füllt die Befehlsliste auf.
    -   Setzt die Zuweisung der Befehlsliste zurück.
        > [!Note]  
        > Verwenden Sie den Speicher, der mit der Befehls Zuweisung verknüpft ist, erneut.

         

    -   Setzen Sie die Befehlsliste zurück.
    -   Legen Sie die Grafik Stamm Signatur fest.
        > [!Note]  
        > Legt die Grafik Stamm Signatur fest, die für die aktuelle Befehlsliste verwendet werden soll.

         

    -   Legen Sie die Rechtecke Viewport und Scheren fest.
    -   Legen Sie eine Ressourcengrenze fest, die angibt, dass der Hintergrund Puffer als Renderziel verwendet werden soll.
        > [!Note]  
        > Ressourcen Barrieren werden verwendet, um Ressourcen Übergänge zu verwalten.

         

    -   Aufzeichnen von Befehlen in der Befehlsliste.
    -   Gibt an, dass der Hintergrund Puffer nach der Ausführung der Befehlsliste verwendet werden soll.
        > [!Note]  
        > Ein weiterer Rückruf zum Festlegen einer Ressourcen Barriere.

         

    -   Schließen Sie die Befehlsliste, um die Aufzeichnung zu erhöhen.
-   Führen Sie die Befehlsliste aus.
-   Stellen Sie den Frame dar.
-   Warten Sie, bis die GPU abgeschlossen ist.
    > [!Note]  
    > Aktualisieren und überprüfen Sie den Fence.

Weitere Informationen finden Sie unter [onrendering](#onrender).

### <a name="destroy"></a>Zerstören

Schließen Sie die APP ordnungsgemäß.

-   Warten Sie, bis die GPU abgeschlossen ist.
    > [!Note]  
    > Abschließende Prüfung am Fence.

-   Schließen Sie das Ereignis handle.

Weitere Informationen finden Sie unter [OnDestroy](#ondestroy).

## <a name="code-example-for-a-simple-app"></a>Code Beispiel für eine einfache APP

Im folgenden wird der Code Abschnitt erweitert, um den für ein einfaches Beispiel erforderlichen Code einzubeziehen.

### <a name="class-d3d12hellotriangle"></a>Class D3D12HelloTriangle

Definieren Sie zunächst die-Klasse in einer Header Datei, einschließlich eines Viewports, Scheren-Rechtecks und Scheitelpunkt Puffers mithilfe der-Strukturen:

-   [**D3D12 \_ Viewport**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport)
-   [**D3D12 \_ Rect**](d3d12-rect.md)
-   [**D3D12 \_ Vertex- \_ Puffer \_ Ansicht**](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)

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

### <a name="oninit"></a>OnInit ()

Beginnen Sie in der Haupt Quelldatei des Projekts mit dem Initialisieren der Objekte:

```cpp
void D3D12HelloTriangle::OnInit()
{
    LoadPipeline();
    LoadAssets();
}
```

### <a name="loadpipeline"></a>Loadpipeline ()

Der folgende Code erstellt die Grundlagen für eine Grafik Pipeline. Der Prozess zum Erstellen von Geräten und Austauschen von Ketten ähnelt Direct3D 11.

-   Aktivieren Sie die Debugebene mit Aufrufen von:<dl>

[**D3D12GetDebugInterface**](/windows/win32/api/d3d12/nf-d3d12-d3d12getdebuginterface)  
    [**ID3D12Debug:: enabledebuglayer**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)  
    </dl>
-   Erstellen Sie das Gerät:<dl>

[**CreateDXGIFactory1**](/windows/win32/api/dxgi/nf-dxgi-createdxgifactory1)  
    [**D3D12CreateDevice**](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)  
    </dl>
-   Füllen Sie die Beschreibung einer Befehls Warteschlange aus, und erstellen Sie die Befehls Warteschlange<dl>

[**D3D12 \_ Befehls \_ Warteschlange entfernen \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)  
    [**ID3D12Device:: kreatecommandqueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)  
    </dl>
-   Füllen Sie eine vorhandenes SwapChain-Beschreibung aus, und erstellen Sie dann die Swapkette: <dl>

[**DXGI \_ - \_ SwapChain-Debug \_**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)  
    [**Idxgifactory:: kreateswapchain**](/windows/win32/api/dxgi/nf-dxgi-idxgifactory-createswapchain)  
    [**IDXGISwapChain3:: getcurrentbackbufferindex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex)  
    </dl>
-   Füllen Sie eine Heap Beschreibung aus. Erstellen Sie dann einen deskriptorheap: <dl>

[**D3D12 \_ \_ deskriptorheap- \_ decoeration**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)  
    [**ID3D12Device:: kreatedescriptorheap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)  
    [**ID3D12Device:: getDescriptor handleinkrementsize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)  
    </dl>
-   Erstellen Sie die Ansicht des Renderziels: <dl>

[**CD3DX12- \_ CPU- \_ \_ Deskriptorhandle**](cd3dx12-cpu-descriptor-handle.md)  
    [**Getcpudescriptor Lenker forheapstart**](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [**Idxgiswapchain:: GetBuffer**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)  
    [**ID3D12Device:: kreaterendertargetview**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)  
    </dl>
-   Erstellen Sie die Befehls Zuweisung: [**ID3D12Device:: kreatecommandzuweisung**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).

In späteren Schritten werden Befehlslisten von der Befehls Zuweisung abgerufen und an die Befehls Warteschlange übermittelt.

Laden der Rendering-Pipeline Abhängigkeiten (Beachten Sie, dass die Erstellung eines Software Warp-Geräts vollständig optional ist).


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



### <a name="loadassets"></a>Loadassets ()

Das Laden und Vorbereiten von Assets ist ein langwieriger Prozess. Viele dieser Phasen ähneln D3D 11, aber einige sind neu in D3D 12.

In Direct3D 12 wird der erforderliche Pipeline Status über ein [Pipeline Zustands Objekt](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO) an eine Befehlsliste angefügt. Dieses Beispiel zeigt, wie ein PSO erstellt wird. Sie können die PSO als Element Variable speichern und Sie so oft wie nötig wieder verwenden.

Ein deskriptorheap definiert die Sichten und den Zugriff auf Ressourcen (z. b. eine renderzielansicht).

Mit der Befehlslisten Zuweisung und PSO können Sie die tatsächliche Befehlsliste erstellen, die zu einem späteren Zeitpunkt ausgeführt wird.

Die folgenden APIs und Prozesse werden nacheinander aufgerufen.

-   Erstellen Sie eine leere Stamm Signatur, indem Sie die verfügbare hilfsstruktur verwenden: <dl>

[**CD3DX12 \_ Stamm \_ Signatur \_ DESC**](cd3dx12-root-signature-desc.md)  
    [**D3D12SerializeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)  
    [**ID3D12Device:: kreaterootsignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)  
    </dl>
-   Laden und kompilieren Sie die Shader: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).
-   Erstellen Sie das Vertex-Eingabe Layout: [**D3D12 \_ input \_ Element \_ ensc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).
-   Geben Sie eine Beschreibung des Pipeline Zustands ein, verwenden Sie die verfügbaren Hilfsstrukturen, und erstellen Sie dann den Status der Grafik Pipeline: <dl>

[**D3D12- \_ Grafik \_ Pipeline \_ Status \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)  
    [**CD3DX12 \_ Rasterizer- \_ Abteilung**](cd3dx12-rasterizer-desc.md)  
    [**CD3DX12 \_ Blend- \_ Entsc**](cd3dx12-blend-desc.md)  
    [**ID3D12Device:: kreategraphicspipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)  
    </dl>
-   Erstellen und schließen Sie eine Befehlsliste: <dl>

[**ID3D12Device:: kreatecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)  
    [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)  
    </dl>
-   Erstellen Sie den Vertex-Puffer: [**ID3D12Device:: | atecommittedresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).
-   Kopieren Sie die Scheitelpunkt Daten in den Vertex-Puffer:<dl>

[**ID3D12Resource:: map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)  
    [**ID3D12Resource:: unmap**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-unmap)  
    </dl>
-   Initialisieren Sie die Vertex-Puffer Ansicht: [**getgpuvirtualaddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).
-   Erstellen und initialisieren Sie den Fence: [**ID3D12Device:: kreatefence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).
-   Erstellen Sie ein Ereignis Handle für die Verwendung mit der Rahmen Synchronisierung.
-   Warten Sie, bis die GPU abgeschlossen ist.


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



### <a name="onupdate"></a>OnUpdate ()

Für ein einfaches Beispiel wird nichts aktualisiert.


```cpp
void D3D12HelloTriangle::OnUpdate()

{
}
```



### <a name="onrender"></a>Onrendering ()

Während der Einrichtung wurde die Element Variable **m \_ CommandList** verwendet, um alle Setup Befehle aufzuzeichnen und auszuführen. Sie können diesen Member nun in der Haupt-Renderschleife wieder verwenden.

Das Rendering umfasst einen aufzurufenden Befehl zum Auffüllen der Befehlsliste. Anschließend kann die Befehlsliste ausgeführt und der nächste Puffer in der SwapChain angezeigt werden:

-   Füllt die Befehlsliste auf.
-   Führen Sie die Befehlsliste aus: [**ID3D12CommandQueue:: executecommandlists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).
-   [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) der Frame.
-   Warten Sie, bis die GPU abgeschlossen ist.


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



### <a name="populatecommandlist"></a>Populatecommandlist ()

Sie müssen die Zuweisung der Befehlsliste und die Befehlsliste selbst zurücksetzen, bevor Sie Sie wieder verwenden können. In komplexeren Szenarien kann es sinnvoll sein, die Zuweisung jedes Paar Frames zurückzusetzen. Der Arbeitsspeicher ist mit der Zuweisung verknüpft, die nicht sofort nach dem Ausführen einer Befehlsliste freigegeben werden kann. Dieses Beispiel zeigt, wie Sie die Zuweisung nach jedem Frame zurücksetzen können.

Wieder verwenden Sie nun die Befehlsliste für den aktuellen Frame. Fügen Sie den Viewport erneut an die Befehlsliste an (Dies muss immer erfolgen, wenn eine Befehlsliste zurückgesetzt wird und bevor die Befehlsliste ausgeführt wird). Geben Sie an, dass die Ressource als Renderziel verwendet werden soll, und geben Sie dann an, dass das Renderziel verwendet wird, wenn die Ausführung der Befehlsliste abgeschlossen ist.

Beim Auffüllen von Befehlslisten werden wiederum die folgenden Methoden und Prozesse aufgerufen:

-   Zurücksetzen der Befehls Zuweisung und der Befehlsliste: <dl>

[**ID3D12CommandAllocator:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)  
    [**ID3D12GraphicsCommandList:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)  
    </dl>
-   Legen Sie die Stamm Signatur, Viewport und Scheren Rechtecke fest: <dl>

[**ID3D12GraphicsCommandList:: setgraphicsrootsignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature)  
    [**ID3D12GraphicsCommandList:: rssetviewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)  
    [**ID3D12GraphicsCommandList:: rssezcissorrects**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)  
    </dl>
-   Geben Sie an, dass der Hintergrund Puffer als Renderziel verwendet werden soll: <dl>

[**ID3D12GraphicsCommandList:: resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)  
    [**ID3D12DescriptorHeap:: getcpudescriptor Lenker forheapstart**](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [**ID3D12GraphicsCommandList:: omgtrendertargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)  
    </dl>
-   Aufzeichnen Sie die Befehle:<dl>

[**ID3D12GraphicsCommandList:: clearrendertargetview**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)  
    [**ID3D12GraphicsCommandList:: iasetprimitivetopology**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology)  
    [**ID3D12GraphicsCommandList:: iasetvertexbuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)  
    [**ID3D12GraphicsCommandList::D rawinstanzierte**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)  
    </dl>
-   Gibt an, dass der Hintergrund Puffer nun verwendet wird, um Folgendes anzuzeigen: [**ID3D12GraphicsCommandList:: resourcebarriere**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).
-   Schließen Sie die Befehlsliste: [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).


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



### <a name="waitforpreviousframe"></a>Waitforpreviousframe ()

Der folgende Code zeigt eine vereinfachte Verwendung von Zäunen.

> [!Note]  
> Das warten auf den Abschluss eines Frames ist für die meisten apps zu ineffizient.

 

Die folgenden APIs und Prozesse werden in der angegebenen Reihenfolge aufgerufen:

-   [**ID3D12CommandQueue:: Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
-   [**ID3D12Fence:: getcompletedvalue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)
-   [**ID3D12Fence:: Einstellungs Element**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)
-   Warten Sie auf das-Ereignis.
-   Aktualisieren Sie den Frame Index: [**IDXGISwapChain3:: getcurrentbackbufferindex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).


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



### <a name="ondestroy"></a>OnDestroy ()

Schließen Sie die APP ordnungsgemäß.

-   Warten Sie, bis die GPU abgeschlossen ist.
-   Schließen Sie das-Ereignis.


```cpp
void D3D12HelloTriangle::OnDestroy()
{

    // Wait for the GPU to be done with all resources.
    WaitForPreviousFrame();

    CloseHandle(m_fenceEvent);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegendes zu Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Funktionierende Beispiele](working-samples.md)
</dt> </dl>

 

 
