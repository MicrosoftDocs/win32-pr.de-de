---
title: Grundlegendes zur Direct3D 11-Renderingpipeline
description: Zuvor haben Sie sich mit dem Erstellen eines Fensters beschäftigt, das Sie zum Zeichnen in Arbeiten mit DirectX-Geräte Ressourcen verwenden können. Nun erfahren Sie, wie Sie die Grafik Pipeline erstellen und wo Sie Sie anschließen können.
ms.assetid: 73cf62d0-7e4f-4e93-aa65-12741588d4fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50f9a387b2d44fe750abcf5a8856f75e6d0110e
ms.sourcegitcommit: 07b756a2f350efa5cfd5024a723ef392274ac3d9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "106371819"
---
# <a name="understand-the-direct3d-11-rendering-pipeline"></a>Grundlegendes zur Direct3D 11-Renderingpipeline

Zuvor haben Sie sich mit dem Erstellen eines Fensters beschäftigt, das Sie zum Zeichnen in [Arbeiten mit DirectX-Geräte Ressourcen](work-with-dxgi.md)verwenden können. Nun erfahren Sie, wie Sie die Grafik Pipeline erstellen und wo Sie Sie anschließen können.

Sie erinnern sich, dass es zwei Direct3D-Schnittstellen gibt, die die Grafik Pipeline definieren: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), das eine virtuelle Darstellung der GPU und ihrer Ressourcen bereitstellt. und [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), das die Grafik Verarbeitung für die Pipeline darstellt. In der Regel verwenden Sie eine Instanz von **ID3D11Device** zum Konfigurieren und Abrufen der GPU-Ressourcen, die Sie benötigen, um mit der Verarbeitung der Grafiken in einer Szene zu beginnen, und Sie verwenden **Verknüpfung id3d11devicecontext aus** , um diese Ressourcen in jeder entsprechenden Shader-Phase in der Grafik Pipeline zu verarbeiten. **ID3D11Device** -Methoden werden in der Regel nur selten aufgerufen – d. h. nur, wenn Sie eine Szene einrichten oder wenn das Gerät geändert wird. Auf der anderen Seite wird **Verknüpfung id3d11devicecontext aus** jedes Mal aufgerufen, wenn Sie einen Frame für die Anzeige verarbeiten.

In diesem Beispiel wird eine minimale Grafik Pipeline erstellt und konfiguriert, die für die Anzeige eines einfachen drehenden, vertexschattierten Cubes geeignet ist. Es wird ungefähr die kleinste Menge von Ressourcen veranschaulicht, die für die Anzeige notwendig ist. Beachten Sie beim Lesen der Informationen die Einschränkungen des jeweiligen Beispiels, wo Sie es möglicherweise erweitern müssen, um die Szene zu unterstützen, die Sie darstellen möchten.

In diesem Beispiel werden zwei C++-Klassen für Grafiken behandelt: eine Geräte Ressourcen-Manager-Klasse und eine 3D-Szene-Renderer-Klasse. Dieses Thema konzentriert sich speziell auf den 3D-Szenen-Renderer.

## <a name="what-does-the-cube-renderer-do"></a>Was macht der Cube-Renderer?

Die Grafik Pipeline wird von der 3D-Szene-Renderer-Klasse definiert. Der Szenen-Renderer kann:

-   Definieren konstanter Puffer zum Speichern der einheitlichen Daten.
-   Definieren Sie Vertex-Puffer für die Vertex-Objektdaten und die entsprechenden Index Puffer, damit der Vertex-Shader die Dreiecke ordnungsgemäß durchlaufen kann.
-   Erstellen Sie Textur Ressourcen und Ressourcen Ansichten.
-   Laden Sie die Shader-Objekte.
-   Aktualisieren Sie die Grafikdaten, sodass die einzelnen Frames angezeigt werden.
-   Rendering (zeichnen) der Grafik in der SwapChain.

Die ersten vier Prozesse verwenden normalerweise die [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) -Schnittstellen Methoden zum Initialisieren und Verwalten von Grafik Ressourcen. die letzten beiden Prozesse verwenden die [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) -Schnittstellen Methoden, um die Grafik Pipeline zu verwalten und auszuführen.

Eine Instanz der **Rendererklasse** wird als Element Variable in der Hauptprojekt Klasse erstellt und verwaltet. Die **deviceresources** -Instanz wird als frei gegebener Zeiger über mehrere Klassen verwaltet, einschließlich der Hauptprojekt Klasse, der **App** -Ansichts Anbieter Klasse und des **Renderers**. Wenn Sie **Renderer** durch ihre eigene Klasse ersetzen, sollten Sie die **deviceresources** -Instanz auch deklarieren und als frei gegebenes Zeiger Element zuweisen:

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

Übergeben Sie den Zeiger einfach an den Klassenkonstruktor (oder eine andere Initialisierungs Methode), nachdem die **deviceresources** -Instanz in der **Initialize** -Methode der **App** -Klasse erstellt wurde. Sie können auch eine **schwache \_ ptr** -Referenz übergeben, wenn Sie stattdessen möchten, dass Ihre Hauptklasse die **deviceresources** -Instanz vollständig besitzt.

## <a name="create-the-cube-renderer"></a>Erstellen des Cube-Renderers

In diesem Beispiel ordnen wir die Szene-Renderer-Klasse mit den folgenden Methoden an:

-   **Createdevicedependentresources**: wird aufgerufen, wenn die Szene initialisiert oder neu gestartet werden muss. Diese Methode lädt Ihre anfänglichen Scheitelpunkt Daten, Texturen, Shader und andere Ressourcen und erstellt die anfängliche Konstante und den Scheitelpunkt Puffer. Der größte Teil der Arbeit erfolgt in der Regel mit [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) -Methoden, nicht mit [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) -Methoden.
-   **Createwindowsizedependentresources**: wird immer dann aufgerufen, wenn sich der Fenster Zustand ändert, z. b. bei einer Größenänderung oder bei einer Änderung der Ausrichtung. Mit dieser Methode werden Transformations Matrizen neu erstellt, z. b. die der Kamera.
-   **Update**: wird normalerweise von dem Teil des Programms aufgerufen, der den unmittelbaren Spielzustand verwaltet. in diesem Beispiel wird es nur aus der **Haupt** Klasse aufgerufen. Lassen Sie diese Methode aus beliebigen Spiel Zustandsinformationen lesen, die sich auf das Rendering auswirken, wie z. b. Aktualisierungen der Objektposition oder Animations Rahmen, sowie auf alle globalen Spieldaten wie leichte Ebenen oder Änderungen an der Spielphysik. Diese Eingaben werden verwendet, um die pro-Frame-Konstante Puffer und Objektdaten zu aktualisieren.
-   **Rendering**: wird normalerweise von dem Teil des Programms aufgerufen, der die Spiel Schleife verwaltet. in diesem Fall wird Sie von der **Haupt** Klasse aufgerufen. Diese Methode erstellt die Grafik Pipeline: Sie bindet Shader, bindet Puffer und Ressourcen an shaderstufen und ruft die Zeichnung für den aktuellen Frame auf.

Diese Methoden umfassen den Hauptteil der Verhaltensweisen zum Rendern einer Szene mit Direct3D mithilfe Ihrer Assets. Wenn Sie dieses Beispiel mit einer neuen Renderingklasse erweitern, deklarieren Sie es in der Hauptprojekt Klasse. So:

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

zu

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

Beachten Sie, dass in diesem Beispiel davon ausgegangen wird, dass die-Methoden in ihrer Implementierung die gleichen Signaturen aufweisen. Wenn sich die Signaturen geändert haben, überprüfen Sie die **Haupt** Schleife, und nehmen Sie die Änderungen entsprechend vor.

Betrachten wir nun die Szenen Rendering-Methoden ausführlicher.

## <a name="create-device-dependent-resources"></a>Geräte abhängige Ressourcen erstellen

**Createdevicedependentresources** konsolidiert alle Vorgänge zum Initialisieren der Szene und ihrer Ressourcen mithilfe von [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) -aufrufen. Bei dieser Methode wird davon ausgegangen, dass das Direct3D-Gerät soeben für eine Szene initialisiert wurde (oder neu erstellt wurde). Es erstellt alle Szenen spezifischen Grafik Ressourcen, z. b. den Scheitelpunkt und die Pixel-Shader, den Vertex-und Index Puffer für Objekte und alle anderen Ressourcen (z. b. als Texturen und zugehörige Sichten) neu und lädt diese neu.

Hier ist Beispielcode für **createdevicedependentresources**:


```C++
void Renderer::CreateDeviceDependentResources()
{
    // Compile shaders using the Effects library.
    auto CreateShadersTask = Concurrency::create_task(
            [this]( )
            {
                CreateShaders();
            }
        );

    // Load the geometry for the spinning cube.
    auto CreateCubeTask = CreateShadersTask.then(
            [this]()
            {
                CreateCube();
            }
        );
}

void Renderer::CreateWindowSizeDependentResources()
{
    // Create the view matrix and the perspective matrix.
    CreateViewAndPerspective();
}
```



Jedes Mal, wenn Sie Ressourcen von Datenträgern laden – Ressourcen wie z. b. kompilierte Shader-Objektdateien (CSO oder. CSO) oder Texturen –, führen Sie dies asynchron aus. Dies ermöglicht es Ihnen, andere Aufgaben gleichzeitig auszuführen (z. b. andere Einrichtungs Aufgaben), und da die Hauptschleife nicht blockiert ist, können Sie die Anzeige für den Benutzer visuell interessant machen (z. b. eine ladende Animation für das Spiel). In diesem Beispiel wird die parallelcurrency:: Tasks-API verwendet, die ab Windows 8 verfügbar ist. Beachten Sie die Lambda-Syntax, die zum Kapseln asynchroner Lade Tasks verwendet wird. Diese Lambdas stellen die Funktionen dar, die außerhalb des Threads aufgerufen werden. Daher wird ein Zeiger auf das aktuelle Klassenobjekt (**this**) explizit aufgezeichnet.

Im folgenden finden Sie ein Beispiel dafür, wie Sie den Shader-Bytecode laden können:


```C++
HRESULT hr = S_OK;

// Use the Direct3D device to load resources into graphics memory.
ID3D11Device* device = m_deviceResources->GetDevice();

// You'll need to use a file loader to load the shader bytecode. In this
// example, we just use the standard library.
FILE* vShader, * pShader;
BYTE* bytes;

size_t destSize = 4096;
size_t bytesRead = 0;
bytes = new BYTE[destSize];

fopen_s(&vShader, "CubeVertexShader.cso", "rb");
bytesRead = fread_s(bytes, destSize, 1, 4096, vShader);
hr = device->CreateVertexShader(
    bytes,
    bytesRead,
    nullptr,
    &m_pVertexShader
    );

D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );

delete bytes;


bytes = new BYTE[destSize];
bytesRead = 0;
fopen_s(&pShader, "CubePixelShader.cso", "rb");
bytesRead = fread_s(bytes, destSize, 1, 4096, pShader);
hr = device->CreatePixelShader(
    bytes,
    bytesRead,
    nullptr,
    m_pPixelShader.GetAddressOf()
    );

delete bytes;

CD3D11_BUFFER_DESC cbDesc(
    sizeof(ConstantBufferStruct),
    D3D11_BIND_CONSTANT_BUFFER
    );

hr = device->CreateBuffer(
    &cbDesc,
    nullptr,
    m_pConstantBuffer.GetAddressOf()
    );

fclose(vShader);
fclose(pShader);
```



Im folgenden finden Sie ein Beispiel zum Erstellen von Scheitelpunkt-und Index Puffern:


```C++
HRESULT Renderer::CreateCube()
{
    HRESULT hr = S_OK;

    // Use the Direct3D device to load resources into graphics memory.
    ID3D11Device* device = m_deviceResources->GetDevice();

    // Create cube geometry.
    VertexPositionColor CubeVertices[] =
    {
        {DirectX::XMFLOAT3(-0.5f,-0.5f,-0.5f), DirectX::XMFLOAT3(  0,   0,   0),},
        {DirectX::XMFLOAT3(-0.5f,-0.5f, 0.5f), DirectX::XMFLOAT3(  0,   0,   1),},
        {DirectX::XMFLOAT3(-0.5f, 0.5f,-0.5f), DirectX::XMFLOAT3(  0,   1,   0),},
        {DirectX::XMFLOAT3(-0.5f, 0.5f, 0.5f), DirectX::XMFLOAT3(  0,   1,   1),},

        {DirectX::XMFLOAT3( 0.5f,-0.5f,-0.5f), DirectX::XMFLOAT3(  1,   0,   0),},
        {DirectX::XMFLOAT3( 0.5f,-0.5f, 0.5f), DirectX::XMFLOAT3(  1,   0,   1),},
        {DirectX::XMFLOAT3( 0.5f, 0.5f,-0.5f), DirectX::XMFLOAT3(  1,   1,   0),},
        {DirectX::XMFLOAT3( 0.5f, 0.5f, 0.5f), DirectX::XMFLOAT3(  1,   1,   1),},
    };
    
    // Create vertex buffer:
    
    CD3D11_BUFFER_DESC vDesc(
        sizeof(CubeVertices),
        D3D11_BIND_VERTEX_BUFFER
        );

    D3D11_SUBRESOURCE_DATA vData;
    ZeroMemory(&vData, sizeof(D3D11_SUBRESOURCE_DATA));
    vData.pSysMem = CubeVertices;
    vData.SysMemPitch = 0;
    vData.SysMemSlicePitch = 0;

    hr = device->CreateBuffer(
        &vDesc,
        &vData,
        &m_pVertexBuffer
        );

    // Create index buffer:
    unsigned short CubeIndices [] = 
    {
        0,2,1, // -x
        1,2,3,

        4,5,6, // +x
        5,7,6,

        0,1,5, // -y
        0,5,4,

        2,6,7, // +y
        2,7,3,

        0,4,6, // -z
        0,6,2,

        1,3,7, // +z
        1,7,5,
    };

    m_indexCount = ARRAYSIZE(CubeIndices);

    CD3D11_BUFFER_DESC iDesc(
        sizeof(CubeIndices),
        D3D11_BIND_INDEX_BUFFER
        );

    D3D11_SUBRESOURCE_DATA iData;
    ZeroMemory(&iData, sizeof(D3D11_SUBRESOURCE_DATA));
    iData.pSysMem = CubeIndices;
    iData.SysMemPitch = 0;
    iData.SysMemSlicePitch = 0;
    
    hr = device->CreateBuffer(
        &iDesc,
        &iData,
        &m_pIndexBuffer
        );

    return hr;
}
```



In diesem Beispiel werden keine Netzen oder Texturen geladen. Sie müssen die Methoden zum Laden der Mesh-und Textur Typen erstellen, die für das Spiel spezifisch sind, und Sie asynchron aufzurufen.

Füllen Sie hier auch die anfänglichen Werte für Ihre pro-Szene-Konstanten Puffer auf. Beispiele für den pro-Szene-Konstantenpuffer sind fixierte Lichter oder andere statische Szenen Elemente und-Daten.

## <a name="implement-the-createwindowsizedependentresources-method"></a>Implementieren der createwindowsizedependentresources-Methode

Die **createwindowsizedependentresources** -Methoden werden jedes Mal aufgerufen, wenn die Fenstergröße, die Ausrichtung oder die Auflösung geändert wird.

Fenstergrößen Ressourcen werden wie folgt aktualisiert: die statische Nachrichten Prozedur ruft eines von mehreren möglichen Ereignissen ab, das auf eine Änderung des Fenster Zustands hinweist. Die Hauptschleife wird dann über das Ereignis informiert und ruft **createwindowsizedependentresources** auf der Hauptklassen Instanz auf, die dann die **createwindowsizedependentresources** -Implementierung in der Scene Renderer-Klasse aufruft.

Der primäre Auftrag dieser Methode besteht darin, sicherzustellen, dass die visuellen Elemente aufgrund einer Änderung der Fenster Eigenschaften nicht verwirrt oder ungültig werden. In diesem Beispiel aktualisieren wir die Projekt Matrizen mit einem neuen Feld der Ansicht (FOV) für das Fenster mit der Größe oder der Umgestaltung.

Wir haben bereits den Code zum Erstellen von Fenster Ressourcen in **deviceresources** gesehen, d. h. die Swapkette (mit dem Hintergrund Puffer) und die renderzielsicht. So erstellt der Renderer Seitenverhältnis abhängige Transformationen:


```C++
void Renderer::CreateViewAndPerspective()
{
    // Use DirectXMath to create view and perspective matrices.

    DirectX::XMVECTOR eye = DirectX::XMVectorSet(0.0f, 0.7f, 1.5f, 0.f);
    DirectX::XMVECTOR at  = DirectX::XMVectorSet(0.0f,-0.1f, 0.0f, 0.f);
    DirectX::XMVECTOR up  = DirectX::XMVectorSet(0.0f, 1.0f, 0.0f, 0.f);

    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.view,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixLookAtRH(
                eye,
                at,
                up
                )
            )
        );

    float aspectRatioX = m_deviceResources->GetAspectRatio();
    float aspectRatioY = aspectRatioX < (16.0f / 9.0f) ? aspectRatioX / (16.0f / 9.0f) : 1.0f;

    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.projection,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixPerspectiveFovRH(
                2.0f * std::atan(std::tan(DirectX::XMConvertToRadians(70) * 0.5f) / aspectRatioY),
                aspectRatioX,
                0.01f,
                100.0f
                )
            )
        );
}
```



Wenn in Ihrer Szene ein bestimmtes Layout von Komponenten vorhanden ist, die vom Seitenverhältnis abhängig sind, ist dies der Ort, an dem Sie entsprechend dem Seitenverhältnis neu angeordnet werden. Möglicherweise möchten Sie die Konfiguration des Verhaltens nach der Verarbeitung auch hier ändern.

## <a name="implement-the-update-method"></a>Implementieren der Update-Methode

Die **Update** -Methode wird einmal pro Spiel Schleife aufgerufen. in diesem Beispiel wird Sie von der-Methode der Main-Klasse mit demselben Namen aufgerufen. Es hat einen einfachen Zweck: Aktualisieren von Szenen Geometrie und Spielzustand basierend auf der verstrichenen Zeit (oder den verstrichenen Zeitschritten) seit dem vorherigen Frame. In diesem Beispiel drehen wir den Cube einfach einmal pro Frame. In einer realen Spielszene enthält diese Methode viel mehr Code zum Überprüfen des Spiel Zustands, zum Aktualisieren von pro-Frame (oder anderen dynamischen) Konstanten Puffern, Geometrie Puffern und anderen in-Memory-Assets entsprechend. Da die Kommunikation zwischen CPU und GPU einen mehr Aufwand verursacht, stellen Sie sicher, dass Sie nur Puffer aktualisieren, die sich seit dem letzten Frame geändert haben. die Konstanten Puffer können nach Bedarf gruppiert oder aufgeteilt werden, um dies effizienter zu gestalten.


```C++
void Renderer::Update()
{
    // Rotate the cube 1 degree per frame.
    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.world,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixRotationY(
                DirectX::XMConvertToRadians(
                    (float) m_frameCount++
                    )
                )
            )
        );

    if (m_frameCount == MAXUINT)  m_frameCount = 0;
}
```



In diesem Fall aktualisiert die **Drehung** den konstanten Puffer mit einer neuen Transformationsmatrix für den Cube. Die Matrix wird während der Vertexshader-Stufe pro Scheitelpunkt multipliziert. Da diese Methode mit jedem Frame aufgerufen wird, ist dies ein guter Ausgangspunkt, um alle Methoden zu aggregieren, die Ihre dynamische Konstante und Vertex-Puffer aktualisieren, oder um andere Vorgänge auszuführen, die die Objekte in der Szene für die Transformation durch die Grafik Pipeline vorbereiten.

## <a name="implement-the-render-method"></a>Implementieren der "Rendering"-Methode

Diese Methode wird nach dem Aufruf von **Update** einmal pro Spiel Schleife aufgerufen. Wie bei **Update** auch, wird die **Rendering** -Methode auch von der Hauptklasse aufgerufen. Dies ist die Methode, bei der die Grafik Pipeline für den Frame erstellt und mithilfe von Methoden auf der [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) -Instanz verarbeitet wird. Dies wird in einem abschließenden [**Verknüpfung id3d11devicecontext aus::D rawindebug-aufgeschachtelt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed). Es ist wichtig zu verstehen, dass dieser Aufruf (oder andere ähnliche **Draw _-Aufrufe, die \* *für _ Verknüpfung id3d11devicecontext aus definiert*** sind) tatsächlich die Pipeline ausführt. Dies gilt insbesondere dann, wenn Direct3D mit der GPU kommuniziert, um den Zeichnungs Zustand festzulegen, jede Pipeline Phase ausführt und die Pixel Ergebnisse in die renderzielpufferressource für die Anzeige durch die Swapkette schreibt. Da die Kommunikation zwischen CPU und GPU einen mehr Aufwand verursacht, kombinieren Sie mehrere Draw-Aufrufe in einem einzigen, wenn dies möglich ist. Dies gilt insbesondere, wenn die Szene viele gerenderte Objekte enthält.


```C++
void Renderer::Render()
{
    // Use the Direct3D device context to draw.
    ID3D11DeviceContext* context = m_deviceResources->GetDeviceContext();

    ID3D11RenderTargetView* renderTarget = m_deviceResources->GetRenderTarget();
    ID3D11DepthStencilView* depthStencil = m_deviceResources->GetDepthStencil();

    context->UpdateSubresource(
        m_pConstantBuffer.Get(),
        0,
        nullptr,
        &m_constantBufferData,
        0,
        0
        );

    // Clear the render target and the z-buffer.
    const float teal [] = { 0.098f, 0.439f, 0.439f, 1.000f };
    context->ClearRenderTargetView(
        renderTarget,
        teal
        );
    context->ClearDepthStencilView(
        depthStencil,
        D3D11_CLEAR_DEPTH | D3D11_CLEAR_STENCIL,
        1.0f,
        0);

    // Set the render target.
    context->OMSetRenderTargets(
        1,
        &renderTarget,
        depthStencil
        );

    // Set up the IA stage by setting the input topology and layout.
    UINT stride = sizeof(VertexPositionColor);
    UINT offset = 0;

    context->IASetVertexBuffers(
        0,
        1,
        m_pVertexBuffer.GetAddressOf(),
        &stride,
        &offset
        );

    context->IASetIndexBuffer(
        m_pIndexBuffer.Get(),
        DXGI_FORMAT_R16_UINT,
        0
        );
    
    context->IASetPrimitiveTopology(
        D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST
        );

    context->IASetInputLayout(m_pInputLayout.Get());

    // Set up the vertex shader stage.
    context->VSSetShader(
        m_pVertexShader.Get(),
        nullptr,
        0
        );

    context->VSSetConstantBuffers(
        0,
        1,
        m_pConstantBuffer.GetAddressOf()
        );

    // Set up the pixel shader stage.
    context->PSSetShader(
        m_pPixelShader.Get(),
        nullptr,
        0
        );

    // Calling Draw tells Direct3D to start sending commands to the graphics device.
    context->DrawIndexed(
        m_indexCount,
        0,
        0
        );
}
```



Es empfiehlt sich, die verschiedenen Grafik Pipeline Stufen für den Kontext in der richtigen Reihenfolge festzulegen. Normalerweise ist die Reihenfolge wie folgt:

-   Aktualisieren konstanter Puffer Ressourcen bei Bedarf mit neuen Daten (mithilfe von Daten aus **Update**).
-   Eingabeassembly (IA): Hier fügen wir den Scheitelpunkt und Index Puffer an, die die Szene Geometrie definieren. Sie müssen jeden Scheitelpunkt und Index Puffer für jedes Objekt in der Szene anfügen. Da dieses Beispiel nur den Cube enthält, ist es recht einfach.
-   Vertex-Shader (VS): Fügen Sie alle Scheitelpunkt-Shader an, mit denen die Daten in den Scheitelpunkt Puffern transformiert werden, und fügen Sie Konstante Puffer für den Vertexshader an.
-   Pixel-Shader (PS): Fügen Sie alle Pixel-Shader an, die pro-Pixel-Vorgänge in der rasterisierten Szene ausführen, und fügen Sie Geräte Ressourcen für den Pixelshader (Konstante Puffer, Texturen usw.) an.
-   Ausgabe Zusammenführung (OM): Dies ist die Phase, in der Pixel gemischt werden, nachdem die Shader abgeschlossen sind. Dies ist eine Ausnahme von der Regel, da Sie Ihre tiefen Schablonen und Renderziele anfügen, bevor Sie eine der anderen Stufen festlegen. Sie haben möglicherweise mehrere Schablonen und Ziele, wenn Sie über zusätzliche Scheitelpunkt-und Pixel-Shader verfügen, die Texturen generieren, wie z. b. Schatten Zuordnungen, Höhen Zuordnungen oder andere samplingverfahren. in diesem Fall benötigt jeder Zeichnungs Durchlauf die entsprechenden Ziele, bevor Sie eine Draw-Funktion aufrufen.

Im letzten Abschnitt ([Arbeiten mit Shadern und Shaderressourcen](work-with-shaders-and-shader-resources.md)) betrachten wir nun die Shader und besprechen, wie Direct3D Sie ausführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Als Nächstes**
</dt> <dt>

[Arbeiten mit Shader und Shaderressourcen](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
