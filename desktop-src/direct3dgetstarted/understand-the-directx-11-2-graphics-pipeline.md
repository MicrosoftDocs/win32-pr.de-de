---
title: Grundlegendes zur Direct3D 11-Renderingpipeline
description: Zuvor haben Sie sich angesehen, wie Sie ein Fenster erstellen, das Sie zum Zeichnen in Arbeiten mit DirectX-Geräteressourcen verwenden können. Nun erfahren Sie, wie Sie die Grafikpipeline erstellen und wo Sie sie einbinden können.
ms.assetid: 73cf62d0-7e4f-4e93-aa65-12741588d4fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41a3e0fa7e3f7775c5cd51d49f9867864e7a204975fd982565491a63db829aa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727520"
---
# <a name="understand-the-direct3d-11-rendering-pipeline"></a>Grundlegendes zur Direct3D 11-Renderingpipeline

Zuvor haben Sie sich angesehen, wie Sie ein Fenster erstellen, das Sie zum Zeichnen in [Arbeiten mit DirectX-Geräteressourcen](work-with-dxgi.md)verwenden können. Nun erfahren Sie, wie Sie die Grafikpipeline erstellen und wo Sie sie einbinden können.

Sie werden sich erinnern, dass es zwei Direct3D-Schnittstellen gibt, die die Grafikpipeline definieren: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), die eine virtuelle Darstellung der GPU und ihrer Ressourcen bereitstellt. und [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), die die Grafikverarbeitung für die Pipeline darstellt. In der Regel verwenden Sie eine Instanz von **ID3D11Device,** um die GPU-Ressourcen zu konfigurieren und abzurufen, die Sie benötigen, um mit der Verarbeitung der Grafiken in einer Szene zu beginnen, und sie verwenden **ID3D11DeviceContext,** um diese Ressourcen in jeder geeigneten Shaderphase in der Grafikpipeline zu verarbeiten. In der Regel rufen Sie **die ID3D11Device-Methoden** nur selten auf, d. h. nur, wenn Sie eine Szene einrichten oder das Gerät sich ändert. Auf der anderen Seite rufen Sie **ID3D11DeviceContext** jedes Mal auf, wenn Sie einen Frame für die Anzeige verarbeiten.

In diesem Beispiel wird eine minimale Grafikpipeline erstellt und konfiguriert, die für die Anzeige eines einfachen rotierenden, vertexschattierten Cubes geeignet ist. Es zeigt ungefähr den kleinsten Satz von Ressourcen, die für die Anzeige erforderlich sind. Wenn Sie die Informationen hier lesen, beachten Sie die Einschränkungen des angegebenen Beispiels, in dem Sie sie möglicherweise erweitern müssen, um die Szene zu unterstützen, die Sie rendern möchten.

In diesem Beispiel werden zwei C++-Klassen für Grafiken behandelt: eine Geräteressourcen-Manager-Klasse und eine 3D-Szenenrendererklasse. Dieses Thema konzentriert sich speziell auf den 3D-Szenenrenderer.

## <a name="what-does-the-cube-renderer-do"></a>Was macht der Cuberenderer?

Die Grafikpipeline wird von der 3D-Szenenrendererklasse definiert. Der Szenenrenderer kann folgendes:

-   Definieren Sie konstante Puffer, um Ihre einheitlichen Daten zu speichern.
-   Definieren Sie Scheitelpunktpuffer für die Objektvertexdaten und entsprechende Indexpuffer, damit der Vertex-Shader die Dreiecke ordnungsgemäß durchgehen kann.
-   Erstellen Sie Texturressourcen und Ressourcenansichten.
-   Laden Sie Ihre Shaderobjekte.
-   Aktualisieren Sie die Grafikdaten, um jeden Frame anzuzeigen.
-   Rendern (zeichnen) Sie die Grafiken in der Swapkette.

Die ersten vier Prozesse verwenden in der Regel die [**ID3D11Device-Schnittstellenmethoden**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) zum Initialisieren und Verwalten von Grafikressourcen, und die letzten beiden verwenden die [**ID3D11DeviceContext-Schnittstellenmethoden,**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) um die Grafikpipeline zu verwalten und auszuführen.

Eine Instanz der **Rendererklasse** wird als Membervariable für die Hauptprojektklasse erstellt und verwaltet. Die **DeviceResources-Instanz** wird als freigegebener Zeiger für mehrere Klassen verwaltet, einschließlich der Hauptprojektklasse, der App-Ansichtsanbieterklasse und des **Renderers**.  Wenn Sie **Renderer** durch Ihre eigene Klasse ersetzen, sollten Sie erwägen, die **DeviceResources-Instanz** auch als freigegebenen Zeigermember zu deklarieren und zuzuweisen:

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

Übergeben Sie einfach den Zeiger an den Klassenkonstruktor (oder eine andere Initialisierungsmethode), nachdem die **DeviceResources-Instanz** in der **Initialize-Methode** der **App-Klasse** erstellt wurde. Sie können auch einen **schwachen \_ ptr-Verweis** übergeben, wenn Ihre Hauptklasse stattdessen die **DeviceResources-Instanz** vollständig besitzen soll.

## <a name="create-the-cube-renderer"></a>Erstellen des Cuberenderers

In diesem Beispiel organisieren wir die Szenenrendererklasse mit den folgenden Methoden:

-   **CreateDeviceDependentResources:** Wird immer dann aufgerufen, wenn die Szene initialisiert oder neu gestartet werden muss. Diese Methode lädt Ihre anfänglichen Scheitelpunktdaten, Texturen, Shader und andere Ressourcen und erstellt die anfänglichen Konstanten- und Scheitelpunktpuffer. In der Regel erfolgt der Großteil der Arbeit hier mit [**ID3D11Device-Methoden,**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) nicht mit [**ID3D11DeviceContext-Methoden.**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2)
-   **CreateWindowSizeDependentResources:** Wird aufgerufen, wenn sich der Fensterzustand ändert, z. B. wenn sich die Größe ändert oder die Ausrichtung geändert wird. Diese Methode erstellt Transformationsmatrizen neu, z. B. die für Ihre Kamera.
-   **Update:** Wird in der Regel von dem Teil des Programms aufgerufen, der den unmittelbaren Spielzustand verwaltet. In diesem Beispiel wird es einfach aus der **Main-Klasse** aufgerufen. Lassen Sie diese Methode aus allen Spielzustandsinformationen lesen, die sich auf das Rendering auswirken, z. B. Aktualisierungen der Objektposition oder Animationsframes, sowie aus allen globalen Spieldaten wie Lichtpegeln oder Änderungen an der Spielmechanik. Diese Eingaben werden verwendet, um die Pro-Frame-Konstantenpuffer und Objektdaten zu aktualisieren.
-   **Render:** Wird in der Regel aus dem Teil des Programms aufgerufen, der die Spielschleife verwaltet. in diesem Fall wird sie aus der **Main-Klasse** aufgerufen. Diese Methode erstellt die Grafikpipeline: Sie bindet Shader, Puffer und Ressourcen an Shaderstufen und ruft Zeichnungen für den aktuellen Frame auf.

Diese Methoden bilden den Textkörper des Verhaltens zum Rendern einer Szene mit Direct3D unter Verwendung Ihrer Objekte. Wenn Sie dieses Beispiel um eine neue Renderingklasse erweitern, deklarieren Sie es in der Hauptprojektklasse. Dies ist also:

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

zu

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

Beachten Sie auch hier, dass in diesem Beispiel davon ausgegangen wird, dass die Methoden in Ihrer Implementierung die gleichen Signaturen aufweisen. Wenn sich die Signaturen  geändert haben, überprüfen Sie die Main-Schleife, und nehmen Sie die Änderungen entsprechend vor.

Sehen wir uns die Methoden für das Szenenrendering genauer an.

## <a name="create-device-dependent-resources"></a>Erstellen von geräteabhängigen Ressourcen

**CreateDeviceDependentResources** konsolidiert alle Vorgänge zum Initialisieren der Szene und ihrer Ressourcen mit [**id3D11Device-Aufrufen.**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) Bei dieser Methode wird davon ausgegangen, dass das Direct3D-Gerät soeben für eine Szene initialisiert (oder neu erstellt) wurde. Es erstellt alle szenenspezifischen Grafikressourcen neu oder lädt sie neu, z. B. die Vertex- und Pixel-Shader, den Scheitelpunkt- und Indexpuffer für Objekte und alle anderen Ressourcen (z. B. als Texturen und die entsprechenden Ansichten).

Beispielcode für **CreateDeviceDependentResources:**


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



Jedes Mal, wenn Sie Ressourcen von einem Datenträger laden – z. B. kompilierte Shaderobjektdateien (CSO oder CSO) oder Texturen – tun Sie dies asynchron. Dadurch können Sie andere Aufgaben gleichzeitig ausführen (wie andere Setupaufgaben), und da die Hauptschleife nicht blockiert ist, können Sie dem Benutzer weiterhin etwas visuell Interessantes anzeigen (z. B. eine Ladeanimation für Ihr Spiel). In diesem Beispiel wird die Concurrency::Tasks-API verwendet, die ab Windows 8 verfügbar ist. Beachten Sie die Lambdasyntax, die zum Kapseln asynchroner Ladetasks verwendet wird. Diese Lambdas stellen die Funktionen dar, die als off-thread bezeichnet werden, sodass ein Zeiger auf das aktuelle Klassenobjekt (**this**) explizit erfasst wird.

Hier ist ein Beispiel dafür, wie Sie Shader-Bytecode laden können:


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



Hier ist ein Beispiel für das Erstellen von Scheitelpunkt- und Indexpuffern:


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



In diesem Beispiel werden keine Gittergitter oder Texturen geladen. Sie müssen die Methoden zum Laden der Gitternetz- und Texturtypen erstellen, die für Ihr Spiel spezifisch sind, und sie asynchron aufrufen.

Füllen Sie hier auch die Anfangswerte für Die Pro-Szene-Konstantenpuffer auf. Beispiele für konstanten Puffer pro Szene sind feste Beleuchtung oder andere statische Szenenelemente und Daten.

## <a name="implement-the-createwindowsizedependentresources-method"></a>Implementieren der CreateWindowSizeDependentResources-Methode

**CreateWindowSizeDependentResources-Methoden** werden jedes Mal aufgerufen, wenn sich die Fenstergröße, -ausrichtung oder -auflösung ändert.

Fenstergrößenressourcen werden wie folgt aktualisiert: Die statische Nachrichtenprozage ruft eines von mehreren möglichen Ereignissen ab, die auf eine Änderung des Fensterzustands hinweisen. Ihre Hauptschleife wird dann über das Ereignis informiert und ruft **CreateWindowSizeDependentResources** für die Hauptklasseninstanz auf, die dann die **CreateWindowSizeDependentResources-Implementierung** in der Szenenrendererklasse aufruft.

Der primäre Auftrag dieser Methode besteht darin, sicherzustellen, dass die Visuals aufgrund einer Änderung der Fenstereigenschaften nicht verwechselt oder ungültig werden. In diesem Beispiel aktualisieren wir die Projektmatrizen mit einem neuen Sichtfeld (FOV) für das geänderte oder neu ausgerichtete Fenster.

Wir haben bereits den Code zum Erstellen von Fensterressourcen in **DeviceResources** gesehen, bei dem es sich um die Swapkette (mit Hintergrundpuffer) und die Renderzielansicht handelte. So erstellt der Renderer seitenverhältnisabhängige Transformationen:


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



Wenn Ihre Szene über ein bestimmtes Layout von Komponenten verfügt, das vom Seitenverhältnis abhängt, ist dies der Ort, an dem sie neu angeordnet werden, um dieses Seitenverhältnis zuzuordnen. Möglicherweise möchten Sie auch hier die Konfiguration des Verhaltens nach der Verarbeitung ändern.

## <a name="implement-the-update-method"></a>Implementieren der Update-Methode

Die **Update-Methode** wird einmal pro Spielschleife aufgerufen. In diesem Beispiel wird sie von der -Methode der Hauptklasse mit dem gleichen Namen aufgerufen. Es hat einen einfachen Zweck: Aktualisierung der Szenengeometrie und des Spielzustands basierend auf der Menge der verstrichenen Zeit (oder der verstrichenen Zeitschritte) seit dem vorherigen Frame. In diesem Beispiel drehen wir den Würfel einfach einmal pro Frame. In einer echten Spielszene enthält diese Methode viel mehr Code zum Überprüfen des Spielzustands, zum Aktualisieren von konstanten Puffern pro Frame (oder anderen dynamischen Puffern), Geometriepuffern und anderen In-Memory-Ressourcen entsprechend. Da die Kommunikation zwischen CPU und GPU mehr Aufwand verursacht, stellen Sie sicher, dass Sie nur Puffer aktualisieren, die sich seit dem letzten Frame tatsächlich geändert haben. Ihre konstanten Puffer können nach Bedarf gruppiert oder aufgeteilt werden, um dies effizienter zu gestalten.


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



In diesem Fall aktualisiert **Rotieren** den Konstantenpuffer mit einer neuen Transformationsmatrix für den Cube. Die Matrix wird während der Vertex-Shaderphase pro Scheitelpunkt multipliziert. Da diese Methode mit jedem Frame aufgerufen wird, ist dies ein guter Ort, um alle Methoden zu aggregieren, die Ihre dynamischen Konstanten- und Scheitelpunktpuffer aktualisieren, oder um andere Vorgänge auszuführen, die die Objekte in der Szene für die Transformation durch die Grafikpipeline vorbereiten.

## <a name="implement-the-render-method"></a>Implementieren der Render-Methode

Diese Methode wird einmal pro Spielschleife aufgerufen, nachdem **Update** aufgerufen wurde. Wie **update** wird auch die **Render-Methode** aus der Main-Klasse aufgerufen. Dies ist die Methode, bei der die Grafikpipeline mithilfe von Methoden auf der [**ID3D11DeviceContext-Instanz**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) für den Frame erstellt und verarbeitet wird. Dies führt zu einem abschließenden Aufruf von [**ID3D11DeviceContext::D rawIndexed.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed) Es ist wichtig zu verstehen, dass dieser Aufruf (oder andere ähnliche **\* *Draw_-Aufrufe,* die für _ ID3D11DeviceContext definiert sind)** die Pipeline tatsächlich ausführt. Dies gilt insbesondere, wenn Direct3D mit der GPU kommuniziert, um den Zeichnungszustand festzulegen, jede Pipelinephase ausführt und die Pixelergebnisse zur Anzeige durch die Swapkette in die Renderzielpufferressource schreibt. Da die Kommunikation zwischen CPU und GPU mehr Aufwand verursacht, kombinieren Sie mehrere Zeichnen-Aufrufe in einem einzigen, wenn Sie dies können, insbesondere, wenn Ihre Szene über viele gerenderte Objekte verfügt.


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



Es ist eine bewährte Methode, die verschiedenen Grafikpipelinestufen für den Kontext in der richtigen Reihenfolge festzulegen. In der Regel lautet die Reihenfolge:

-   Aktualisieren Sie konstante Pufferressourcen bei Bedarf mit neuen Daten (mithilfe von Daten aus **Update**).
-   Eingabeassembly (IA): Hier fügen wir den Scheitelpunkt und die Indexpuffer an, die die Szenengeometrie definieren. Sie müssen jeden Scheitelpunkt und Indexpuffer für jedes Objekt in der Szene anfügen. Da dieses Beispiel nur über den Cube verfügt, ist er ziemlich einfach.
-   Vertex-Shader (VS): Fügen Sie alle Vertex-Shader an, die die Daten in den Scheitelpunktpuffern transformieren, und fügen Sie konstante Puffer für den Vertex-Shader an.
-   Pixel-Shader (PS): Fügen Sie alle Pixel-Shader an, die pixelbasierte Vorgänge in der rasterisierten Szene ausführen, und fügen Sie Geräteressourcen für den Pixelshader an (konstante Puffer, Texturen usw.).
-   Ausgabezusammenführung (Output Merger, OM): Dies ist die Phase, in der Pixel kombiniert werden, nachdem die Shader abgeschlossen sind. Dies ist eine Ausnahme von der Regel, da Sie Ihre Tiefenschablonen und Renderziele anfügen, bevor Sie eine der anderen Phasen festlegen. Möglicherweise verfügen Sie über mehrere Schablonen und Ziele, wenn Sie über zusätzliche Scheitelpunkt- und Pixel-Shader verfügen, die Texturen wie Schattenkarten, Höhenkarten oder andere Samplingtechniken generieren. In diesem Fall benötigt jeder Zeichnungsdurchlauf die entsprechenden Ziele, bevor Sie eine Draw-Funktion aufrufen.

Als Nächstes betrachten wir im letzten Abschnitt[(Arbeiten mit Shadern und Shaderressourcen)](work-with-shaders-and-shader-resources.md)die Shader und erläutern, wie Direct3D sie ausführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Als Nächstes**
</dt> <dt>

[Arbeiten mit Shadern und Shaderressourcen](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
