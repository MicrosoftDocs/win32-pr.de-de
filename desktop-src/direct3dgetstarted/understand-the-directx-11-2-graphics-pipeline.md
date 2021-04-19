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
# <a name="understand-the-direct3d-11-rendering-pipeline"></a><span data-ttu-id="40a0e-104">Grundlegendes zur Direct3D 11-Renderingpipeline</span><span class="sxs-lookup"><span data-stu-id="40a0e-104">Understand the Direct3D 11 rendering pipeline</span></span>

<span data-ttu-id="40a0e-105">Zuvor haben Sie sich mit dem Erstellen eines Fensters beschäftigt, das Sie zum Zeichnen in [Arbeiten mit DirectX-Geräte Ressourcen](work-with-dxgi.md)verwenden können.</span><span class="sxs-lookup"><span data-stu-id="40a0e-105">Previously, you looked at how to create a window you can use for drawing in [Work with DirectX device resources](work-with-dxgi.md).</span></span> <span data-ttu-id="40a0e-106">Nun erfahren Sie, wie Sie die Grafik Pipeline erstellen und wo Sie Sie anschließen können.</span><span class="sxs-lookup"><span data-stu-id="40a0e-106">Now, you learn how to build the graphics pipeline, and where you can hook into it.</span></span>

<span data-ttu-id="40a0e-107">Sie erinnern sich, dass es zwei Direct3D-Schnittstellen gibt, die die Grafik Pipeline definieren: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), das eine virtuelle Darstellung der GPU und ihrer Ressourcen bereitstellt. und [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), das die Grafik Verarbeitung für die Pipeline darstellt.</span><span class="sxs-lookup"><span data-stu-id="40a0e-107">You'll recall that there are two Direct3D interfaces that define the graphics pipeline: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), which provides a virtual representation of the GPU and its resources; and [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), which represents the graphics processing for the pipeline.</span></span> <span data-ttu-id="40a0e-108">In der Regel verwenden Sie eine Instanz von **ID3D11Device** zum Konfigurieren und Abrufen der GPU-Ressourcen, die Sie benötigen, um mit der Verarbeitung der Grafiken in einer Szene zu beginnen, und Sie verwenden **Verknüpfung id3d11devicecontext aus** , um diese Ressourcen in jeder entsprechenden Shader-Phase in der Grafik Pipeline zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="40a0e-108">Typically, you use an instance of **ID3D11Device** to configure and obtain the GPU resources you need to start processing the graphics in a scene, and you use **ID3D11DeviceContext** to process those resources at each appropriate shader stage in the graphics pipeline.</span></span> <span data-ttu-id="40a0e-109">**ID3D11Device** -Methoden werden in der Regel nur selten aufgerufen – d. h. nur, wenn Sie eine Szene einrichten oder wenn das Gerät geändert wird.</span><span class="sxs-lookup"><span data-stu-id="40a0e-109">You usually call **ID3D11Device** methods infrequently—that is, only when you set up a scene or when the device changes.</span></span> <span data-ttu-id="40a0e-110">Auf der anderen Seite wird **Verknüpfung id3d11devicecontext aus** jedes Mal aufgerufen, wenn Sie einen Frame für die Anzeige verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="40a0e-110">On the other hand, you'll call **ID3D11DeviceContext** every time you process a frame for display.</span></span>

<span data-ttu-id="40a0e-111">In diesem Beispiel wird eine minimale Grafik Pipeline erstellt und konfiguriert, die für die Anzeige eines einfachen drehenden, vertexschattierten Cubes geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="40a0e-111">This example creates and configures a minimal graphics pipeline suitable for displaying a simple spinning, vertex-shaded cube.</span></span> <span data-ttu-id="40a0e-112">Es wird ungefähr die kleinste Menge von Ressourcen veranschaulicht, die für die Anzeige notwendig ist.</span><span class="sxs-lookup"><span data-stu-id="40a0e-112">It demonstrates approximately the smallest set of resources necessary for display.</span></span> <span data-ttu-id="40a0e-113">Beachten Sie beim Lesen der Informationen die Einschränkungen des jeweiligen Beispiels, wo Sie es möglicherweise erweitern müssen, um die Szene zu unterstützen, die Sie darstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="40a0e-113">As you read the info here, note the limitations of the given example where you may have to extend it to support the scene you want to render.</span></span>

<span data-ttu-id="40a0e-114">In diesem Beispiel werden zwei C++-Klassen für Grafiken behandelt: eine Geräte Ressourcen-Manager-Klasse und eine 3D-Szene-Renderer-Klasse.</span><span class="sxs-lookup"><span data-stu-id="40a0e-114">This example covers two C++ classes for graphics: a device resource manager class, and 3D scene renderer class.</span></span> <span data-ttu-id="40a0e-115">Dieses Thema konzentriert sich speziell auf den 3D-Szenen-Renderer.</span><span class="sxs-lookup"><span data-stu-id="40a0e-115">This topic focuses specifically on the 3D scene renderer.</span></span>

## <a name="what-does-the-cube-renderer-do"></a><span data-ttu-id="40a0e-116">Was macht der Cube-Renderer?</span><span class="sxs-lookup"><span data-stu-id="40a0e-116">What does the cube renderer do?</span></span>

<span data-ttu-id="40a0e-117">Die Grafik Pipeline wird von der 3D-Szene-Renderer-Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="40a0e-117">The graphics pipeline is defined by the 3D scene renderer class.</span></span> <span data-ttu-id="40a0e-118">Der Szenen-Renderer kann:</span><span class="sxs-lookup"><span data-stu-id="40a0e-118">The scene renderer is able to:</span></span>

-   <span data-ttu-id="40a0e-119">Definieren konstanter Puffer zum Speichern der einheitlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="40a0e-119">Define constant buffers to store your uniform data.</span></span>
-   <span data-ttu-id="40a0e-120">Definieren Sie Vertex-Puffer für die Vertex-Objektdaten und die entsprechenden Index Puffer, damit der Vertex-Shader die Dreiecke ordnungsgemäß durchlaufen kann.</span><span class="sxs-lookup"><span data-stu-id="40a0e-120">Define vertex buffers to hold your object vertex data, and corresponding index buffers to enable the vertex shader to walk the triangles correctly.</span></span>
-   <span data-ttu-id="40a0e-121">Erstellen Sie Textur Ressourcen und Ressourcen Ansichten.</span><span class="sxs-lookup"><span data-stu-id="40a0e-121">Create texture resources and resource views.</span></span>
-   <span data-ttu-id="40a0e-122">Laden Sie die Shader-Objekte.</span><span class="sxs-lookup"><span data-stu-id="40a0e-122">Load your shader objects.</span></span>
-   <span data-ttu-id="40a0e-123">Aktualisieren Sie die Grafikdaten, sodass die einzelnen Frames angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="40a0e-123">Update the graphics data to display each frame.</span></span>
-   <span data-ttu-id="40a0e-124">Rendering (zeichnen) der Grafik in der SwapChain.</span><span class="sxs-lookup"><span data-stu-id="40a0e-124">Render (draw) the graphics to the swap chain.</span></span>

<span data-ttu-id="40a0e-125">Die ersten vier Prozesse verwenden normalerweise die [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) -Schnittstellen Methoden zum Initialisieren und Verwalten von Grafik Ressourcen. die letzten beiden Prozesse verwenden die [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) -Schnittstellen Methoden, um die Grafik Pipeline zu verwalten und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="40a0e-125">The first four processes typically use the [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) interface methods for initializing and managing graphics resources, and the last two use the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) interface methods to manage and execute the graphics pipeline.</span></span>

<span data-ttu-id="40a0e-126">Eine Instanz der **Rendererklasse** wird als Element Variable in der Hauptprojekt Klasse erstellt und verwaltet.</span><span class="sxs-lookup"><span data-stu-id="40a0e-126">An instance of the **Renderer** class is created and managed as a member variable on the main project class.</span></span> <span data-ttu-id="40a0e-127">Die **deviceresources** -Instanz wird als frei gegebener Zeiger über mehrere Klassen verwaltet, einschließlich der Hauptprojekt Klasse, der **App** -Ansichts Anbieter Klasse und des **Renderers**.</span><span class="sxs-lookup"><span data-stu-id="40a0e-127">The **DeviceResources** instance is managed as a shared pointer across several classes, including the main project class, the **App** view-provider class, and **Renderer**.</span></span> <span data-ttu-id="40a0e-128">Wenn Sie **Renderer** durch ihre eigene Klasse ersetzen, sollten Sie die **deviceresources** -Instanz auch deklarieren und als frei gegebenes Zeiger Element zuweisen:</span><span class="sxs-lookup"><span data-stu-id="40a0e-128">If you replace **Renderer** with your own class, consider declaring and assigning the **DeviceResources** instance as a shared pointer member as well:</span></span>

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

<span data-ttu-id="40a0e-129">Übergeben Sie den Zeiger einfach an den Klassenkonstruktor (oder eine andere Initialisierungs Methode), nachdem die **deviceresources** -Instanz in der **Initialize** -Methode der **App** -Klasse erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="40a0e-129">Just pass the pointer into the class constructor (or other initialization method) after the **DeviceResources** instance is created in the **Initialize** method of the **App** class.</span></span> <span data-ttu-id="40a0e-130">Sie können auch eine **schwache \_ ptr** -Referenz übergeben, wenn Sie stattdessen möchten, dass Ihre Hauptklasse die **deviceresources** -Instanz vollständig besitzt.</span><span class="sxs-lookup"><span data-stu-id="40a0e-130">You can also pass a **weak\_ptr** reference if, instead, you want your main class to completely own the **DeviceResources** instance.</span></span>

## <a name="create-the-cube-renderer"></a><span data-ttu-id="40a0e-131">Erstellen des Cube-Renderers</span><span class="sxs-lookup"><span data-stu-id="40a0e-131">Create the cube renderer</span></span>

<span data-ttu-id="40a0e-132">In diesem Beispiel ordnen wir die Szene-Renderer-Klasse mit den folgenden Methoden an:</span><span class="sxs-lookup"><span data-stu-id="40a0e-132">In this example, we organize the scene renderer class with the following methods:</span></span>

-   <span data-ttu-id="40a0e-133">**Createdevicedependentresources**: wird aufgerufen, wenn die Szene initialisiert oder neu gestartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="40a0e-133">**CreateDeviceDependentResources**: Called whenever the scene must be initialized or restarted.</span></span> <span data-ttu-id="40a0e-134">Diese Methode lädt Ihre anfänglichen Scheitelpunkt Daten, Texturen, Shader und andere Ressourcen und erstellt die anfängliche Konstante und den Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="40a0e-134">This method loads your initial vertex data, textures, shaders, and other resources, and constructs the initial constant and vertex buffers.</span></span> <span data-ttu-id="40a0e-135">Der größte Teil der Arbeit erfolgt in der Regel mit [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) -Methoden, nicht mit [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="40a0e-135">Typically, most of the work here is done with [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) methods, not [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) methods.</span></span>
-   <span data-ttu-id="40a0e-136">**Createwindowsizedependentresources**: wird immer dann aufgerufen, wenn sich der Fenster Zustand ändert, z. b. bei einer Größenänderung oder bei einer Änderung der Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="40a0e-136">**CreateWindowSizeDependentResources**: Called whenever the window state changes, such as when resizing occurs or when orientation changes.</span></span> <span data-ttu-id="40a0e-137">Mit dieser Methode werden Transformations Matrizen neu erstellt, z. b. die der Kamera.</span><span class="sxs-lookup"><span data-stu-id="40a0e-137">This method rebuilds transform matrices, such as those for your camera.</span></span>
-   <span data-ttu-id="40a0e-138">**Update**: wird normalerweise von dem Teil des Programms aufgerufen, der den unmittelbaren Spielzustand verwaltet. in diesem Beispiel wird es nur aus der **Haupt** Klasse aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="40a0e-138">**Update**: Typically called from the part of the program that manages immediate game state; in this example, we just call it from the **Main** class.</span></span> <span data-ttu-id="40a0e-139">Lassen Sie diese Methode aus beliebigen Spiel Zustandsinformationen lesen, die sich auf das Rendering auswirken, wie z. b. Aktualisierungen der Objektposition oder Animations Rahmen, sowie auf alle globalen Spieldaten wie leichte Ebenen oder Änderungen an der Spielphysik.</span><span class="sxs-lookup"><span data-stu-id="40a0e-139">Have this method read from any game-state information that affects rendering, such as updates to object position or animation frames, plus any global game data like light levels or changes to game physics.</span></span> <span data-ttu-id="40a0e-140">Diese Eingaben werden verwendet, um die pro-Frame-Konstante Puffer und Objektdaten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="40a0e-140">These inputs are used to update the per-frame constant buffers and object data.</span></span>
-   <span data-ttu-id="40a0e-141">**Rendering**: wird normalerweise von dem Teil des Programms aufgerufen, der die Spiel Schleife verwaltet. in diesem Fall wird Sie von der **Haupt** Klasse aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="40a0e-141">**Render**: Typically called from the part of the program that manages the game loop; in this case, it's called from the **Main** class.</span></span> <span data-ttu-id="40a0e-142">Diese Methode erstellt die Grafik Pipeline: Sie bindet Shader, bindet Puffer und Ressourcen an shaderstufen und ruft die Zeichnung für den aktuellen Frame auf.</span><span class="sxs-lookup"><span data-stu-id="40a0e-142">This method constructs the graphics pipeline: it binds shaders, binds buffers and resources to shader stages, and invokes drawing for the current frame.</span></span>

<span data-ttu-id="40a0e-143">Diese Methoden umfassen den Hauptteil der Verhaltensweisen zum Rendern einer Szene mit Direct3D mithilfe Ihrer Assets.</span><span class="sxs-lookup"><span data-stu-id="40a0e-143">These methods comprise the body of behaviors for rendering a scene with Direct3D using your assets.</span></span> <span data-ttu-id="40a0e-144">Wenn Sie dieses Beispiel mit einer neuen Renderingklasse erweitern, deklarieren Sie es in der Hauptprojekt Klasse.</span><span class="sxs-lookup"><span data-stu-id="40a0e-144">If you extend this example with a new rendering class, declare it on the main project class.</span></span> <span data-ttu-id="40a0e-145">So:</span><span class="sxs-lookup"><span data-stu-id="40a0e-145">So this:</span></span>

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

<span data-ttu-id="40a0e-146">zu</span><span class="sxs-lookup"><span data-stu-id="40a0e-146">becomes this:</span></span>

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

<span data-ttu-id="40a0e-147">Beachten Sie, dass in diesem Beispiel davon ausgegangen wird, dass die-Methoden in ihrer Implementierung die gleichen Signaturen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="40a0e-147">Again, note that this example assumes that the methods have the same signatures in your implementation.</span></span> <span data-ttu-id="40a0e-148">Wenn sich die Signaturen geändert haben, überprüfen Sie die **Haupt** Schleife, und nehmen Sie die Änderungen entsprechend vor.</span><span class="sxs-lookup"><span data-stu-id="40a0e-148">If the signatures have changed, review the **Main** loop and make the changes accordingly.</span></span>

<span data-ttu-id="40a0e-149">Betrachten wir nun die Szenen Rendering-Methoden ausführlicher.</span><span class="sxs-lookup"><span data-stu-id="40a0e-149">Let's take a look at scene-rendering methods in more detail.</span></span>

## <a name="create-device-dependent-resources"></a><span data-ttu-id="40a0e-150">Geräte abhängige Ressourcen erstellen</span><span class="sxs-lookup"><span data-stu-id="40a0e-150">Create device dependent resources</span></span>

<span data-ttu-id="40a0e-151">**Createdevicedependentresources** konsolidiert alle Vorgänge zum Initialisieren der Szene und ihrer Ressourcen mithilfe von [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) -aufrufen.</span><span class="sxs-lookup"><span data-stu-id="40a0e-151">**CreateDeviceDependentResources** consolidates all the operations for initializing the scene and its resources using [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) calls.</span></span> <span data-ttu-id="40a0e-152">Bei dieser Methode wird davon ausgegangen, dass das Direct3D-Gerät soeben für eine Szene initialisiert wurde (oder neu erstellt wurde).</span><span class="sxs-lookup"><span data-stu-id="40a0e-152">This method assumes that the Direct3D device has just been initialized (or has been recreated) for a scene.</span></span> <span data-ttu-id="40a0e-153">Es erstellt alle Szenen spezifischen Grafik Ressourcen, z. b. den Scheitelpunkt und die Pixel-Shader, den Vertex-und Index Puffer für Objekte und alle anderen Ressourcen (z. b. als Texturen und zugehörige Sichten) neu und lädt diese neu.</span><span class="sxs-lookup"><span data-stu-id="40a0e-153">It recreates or reloads all scene-specific graphics resources, such as the vertex and pixel shaders, the vertex and index buffers for objects, and any other resources (for example, as textures and their corresponding views).</span></span>

<span data-ttu-id="40a0e-154">Hier ist Beispielcode für **createdevicedependentresources**:</span><span class="sxs-lookup"><span data-stu-id="40a0e-154">Here's example code for **CreateDeviceDependentResources**:</span></span>


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



<span data-ttu-id="40a0e-155">Jedes Mal, wenn Sie Ressourcen von Datenträgern laden – Ressourcen wie z. b. kompilierte Shader-Objektdateien (CSO oder. CSO) oder Texturen –, führen Sie dies asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="40a0e-155">Any time you load resources from disk—resources like compiled shader object (CSO, or .cso) files or textures—do so asynchronously.</span></span> <span data-ttu-id="40a0e-156">Dies ermöglicht es Ihnen, andere Aufgaben gleichzeitig auszuführen (z. b. andere Einrichtungs Aufgaben), und da die Hauptschleife nicht blockiert ist, können Sie die Anzeige für den Benutzer visuell interessant machen (z. b. eine ladende Animation für das Spiel).</span><span class="sxs-lookup"><span data-stu-id="40a0e-156">This allows you to keep other work going at the same time (like other setup tasks), and because the main loop isn't blocked you can keep displaying something visually interesting to the user (like a loading animation for your game).</span></span> <span data-ttu-id="40a0e-157">In diesem Beispiel wird die parallelcurrency:: Tasks-API verwendet, die ab Windows 8 verfügbar ist. Beachten Sie die Lambda-Syntax, die zum Kapseln asynchroner Lade Tasks verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40a0e-157">This example uses the Concurrency::Tasks API that is available starting in Windows 8; note the lambda syntax used to encapsulate asynchronous loading tasks.</span></span> <span data-ttu-id="40a0e-158">Diese Lambdas stellen die Funktionen dar, die außerhalb des Threads aufgerufen werden. Daher wird ein Zeiger auf das aktuelle Klassenobjekt (**this**) explizit aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="40a0e-158">These lambdas represent the functions called off-thread, so a pointer to the current class object (**this**) is explicitly captured.</span></span>

<span data-ttu-id="40a0e-159">Im folgenden finden Sie ein Beispiel dafür, wie Sie den Shader-Bytecode laden können:</span><span class="sxs-lookup"><span data-stu-id="40a0e-159">Here's an example of how you can load shader bytecode:</span></span>


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



<span data-ttu-id="40a0e-160">Im folgenden finden Sie ein Beispiel zum Erstellen von Scheitelpunkt-und Index Puffern:</span><span class="sxs-lookup"><span data-stu-id="40a0e-160">Here's an example of how to create vertex and index buffers:</span></span>


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



<span data-ttu-id="40a0e-161">In diesem Beispiel werden keine Netzen oder Texturen geladen.</span><span class="sxs-lookup"><span data-stu-id="40a0e-161">This example does not load any meshes or textures.</span></span> <span data-ttu-id="40a0e-162">Sie müssen die Methoden zum Laden der Mesh-und Textur Typen erstellen, die für das Spiel spezifisch sind, und Sie asynchron aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="40a0e-162">You must create the methods for loading the mesh and texture types that are specific to your game, and call them asynchronously.</span></span>

<span data-ttu-id="40a0e-163">Füllen Sie hier auch die anfänglichen Werte für Ihre pro-Szene-Konstanten Puffer auf.</span><span class="sxs-lookup"><span data-stu-id="40a0e-163">Populate initial values for your per-scene constant buffers here, too.</span></span> <span data-ttu-id="40a0e-164">Beispiele für den pro-Szene-Konstantenpuffer sind fixierte Lichter oder andere statische Szenen Elemente und-Daten.</span><span class="sxs-lookup"><span data-stu-id="40a0e-164">Examples of per-scene constant buffer include fixed lights, or other static scene elements and data.</span></span>

## <a name="implement-the-createwindowsizedependentresources-method"></a><span data-ttu-id="40a0e-165">Implementieren der createwindowsizedependentresources-Methode</span><span class="sxs-lookup"><span data-stu-id="40a0e-165">Implement the CreateWindowSizeDependentResources method</span></span>

<span data-ttu-id="40a0e-166">Die **createwindowsizedependentresources** -Methoden werden jedes Mal aufgerufen, wenn die Fenstergröße, die Ausrichtung oder die Auflösung geändert wird.</span><span class="sxs-lookup"><span data-stu-id="40a0e-166">**CreateWindowSizeDependentResources** methods are called every time the window size, orientation, or resolution changes.</span></span>

<span data-ttu-id="40a0e-167">Fenstergrößen Ressourcen werden wie folgt aktualisiert: die statische Nachrichten Prozedur ruft eines von mehreren möglichen Ereignissen ab, das auf eine Änderung des Fenster Zustands hinweist.</span><span class="sxs-lookup"><span data-stu-id="40a0e-167">Window size resources are updated like so: The static message proc gets one of several possible events indicating a change in window state.</span></span> <span data-ttu-id="40a0e-168">Die Hauptschleife wird dann über das Ereignis informiert und ruft **createwindowsizedependentresources** auf der Hauptklassen Instanz auf, die dann die **createwindowsizedependentresources** -Implementierung in der Scene Renderer-Klasse aufruft.</span><span class="sxs-lookup"><span data-stu-id="40a0e-168">Your main loop is then informed about the event and calls **CreateWindowSizeDependentResources** on the main class instance, which then calls the **CreateWindowSizeDependentResources** implementation on the scene renderer class.</span></span>

<span data-ttu-id="40a0e-169">Der primäre Auftrag dieser Methode besteht darin, sicherzustellen, dass die visuellen Elemente aufgrund einer Änderung der Fenster Eigenschaften nicht verwirrt oder ungültig werden.</span><span class="sxs-lookup"><span data-stu-id="40a0e-169">The primary job of this method is to make sure the visuals don't become confused or invalid because of a change in window properties.</span></span> <span data-ttu-id="40a0e-170">In diesem Beispiel aktualisieren wir die Projekt Matrizen mit einem neuen Feld der Ansicht (FOV) für das Fenster mit der Größe oder der Umgestaltung.</span><span class="sxs-lookup"><span data-stu-id="40a0e-170">In this example, we update the project matrices with a new field of view (FOV) for the resized or reoriented window.</span></span>

<span data-ttu-id="40a0e-171">Wir haben bereits den Code zum Erstellen von Fenster Ressourcen in **deviceresources** gesehen, d. h. die Swapkette (mit dem Hintergrund Puffer) und die renderzielsicht.</span><span class="sxs-lookup"><span data-stu-id="40a0e-171">We already saw the code for creating window resources in **DeviceResources** - that was the swap chain (with back buffer) and render target view.</span></span> <span data-ttu-id="40a0e-172">So erstellt der Renderer Seitenverhältnis abhängige Transformationen:</span><span class="sxs-lookup"><span data-stu-id="40a0e-172">Here's how the renderer creates aspect ratio-dependent transforms:</span></span>


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



<span data-ttu-id="40a0e-173">Wenn in Ihrer Szene ein bestimmtes Layout von Komponenten vorhanden ist, die vom Seitenverhältnis abhängig sind, ist dies der Ort, an dem Sie entsprechend dem Seitenverhältnis neu angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="40a0e-173">If your scene has a specific layout of components that depends on the aspect ratio, this is the place to rearrange them to match that aspect ratio.</span></span> <span data-ttu-id="40a0e-174">Möglicherweise möchten Sie die Konfiguration des Verhaltens nach der Verarbeitung auch hier ändern.</span><span class="sxs-lookup"><span data-stu-id="40a0e-174">You may want to change the configuration of post-processing behavior here also.</span></span>

## <a name="implement-the-update-method"></a><span data-ttu-id="40a0e-175">Implementieren der Update-Methode</span><span class="sxs-lookup"><span data-stu-id="40a0e-175">Implement the Update method</span></span>

<span data-ttu-id="40a0e-176">Die **Update** -Methode wird einmal pro Spiel Schleife aufgerufen. in diesem Beispiel wird Sie von der-Methode der Main-Klasse mit demselben Namen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="40a0e-176">The **Update** method is called once per game loop - in this example, it is called by the main class's method of the same name.</span></span> <span data-ttu-id="40a0e-177">Es hat einen einfachen Zweck: Aktualisieren von Szenen Geometrie und Spielzustand basierend auf der verstrichenen Zeit (oder den verstrichenen Zeitschritten) seit dem vorherigen Frame.</span><span class="sxs-lookup"><span data-stu-id="40a0e-177">It has a simple purpose: update scene geometry and game state based on the amount of elapsed time (or elapsed time steps) since the previous frame.</span></span> <span data-ttu-id="40a0e-178">In diesem Beispiel drehen wir den Cube einfach einmal pro Frame.</span><span class="sxs-lookup"><span data-stu-id="40a0e-178">In this example, we simply rotate the cube once per frame.</span></span> <span data-ttu-id="40a0e-179">In einer realen Spielszene enthält diese Methode viel mehr Code zum Überprüfen des Spiel Zustands, zum Aktualisieren von pro-Frame (oder anderen dynamischen) Konstanten Puffern, Geometrie Puffern und anderen in-Memory-Assets entsprechend.</span><span class="sxs-lookup"><span data-stu-id="40a0e-179">In a real game scene, this method contains a lot more code for checking game state, updating per-frame (or other dynamic) constant buffers, geometry buffers, and other in-memory assets accordingly.</span></span> <span data-ttu-id="40a0e-180">Da die Kommunikation zwischen CPU und GPU einen mehr Aufwand verursacht, stellen Sie sicher, dass Sie nur Puffer aktualisieren, die sich seit dem letzten Frame geändert haben. die Konstanten Puffer können nach Bedarf gruppiert oder aufgeteilt werden, um dies effizienter zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="40a0e-180">Since communication between the CPU and GPU incurs overhead, make sure you only update buffers that have actually changed since the last frame - your constant buffers can be grouped, or split up, as needed to make this more efficient.</span></span>


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



<span data-ttu-id="40a0e-181">In diesem Fall aktualisiert die **Drehung** den konstanten Puffer mit einer neuen Transformationsmatrix für den Cube.</span><span class="sxs-lookup"><span data-stu-id="40a0e-181">In this case, **Rotate** updates the constant buffer with a new transformation matrix for the cube.</span></span> <span data-ttu-id="40a0e-182">Die Matrix wird während der Vertexshader-Stufe pro Scheitelpunkt multipliziert.</span><span class="sxs-lookup"><span data-stu-id="40a0e-182">The matrix will be multiplied per-vertex during the vertex shader stage.</span></span> <span data-ttu-id="40a0e-183">Da diese Methode mit jedem Frame aufgerufen wird, ist dies ein guter Ausgangspunkt, um alle Methoden zu aggregieren, die Ihre dynamische Konstante und Vertex-Puffer aktualisieren, oder um andere Vorgänge auszuführen, die die Objekte in der Szene für die Transformation durch die Grafik Pipeline vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="40a0e-183">Since this method is called with every frame, this is a good place to aggregate any methods that update your dynamic constant and vertex buffers, or to perform any other operations that prepare the objects in the scene for transformation by the graphics pipeline.</span></span>

## <a name="implement-the-render-method"></a><span data-ttu-id="40a0e-184">Implementieren der "Rendering"-Methode</span><span class="sxs-lookup"><span data-stu-id="40a0e-184">Implement the Render method</span></span>

<span data-ttu-id="40a0e-185">Diese Methode wird nach dem Aufruf von **Update** einmal pro Spiel Schleife aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="40a0e-185">This method is called once per game loop after calling **Update**.</span></span> <span data-ttu-id="40a0e-186">Wie bei **Update** auch, wird die **Rendering** -Methode auch von der Hauptklasse aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="40a0e-186">Like **Update**, the **Render** method is also called from the main class.</span></span> <span data-ttu-id="40a0e-187">Dies ist die Methode, bei der die Grafik Pipeline für den Frame erstellt und mithilfe von Methoden auf der [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) -Instanz verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="40a0e-187">This is the method where the graphics pipeline is constructed and processed for the frame using methods on the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) instance.</span></span> <span data-ttu-id="40a0e-188">Dies wird in einem abschließenden [**Verknüpfung id3d11devicecontext aus::D rawindebug-aufgeschachtelt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed).</span><span class="sxs-lookup"><span data-stu-id="40a0e-188">This culminates in a final call to [**ID3D11DeviceContext::DrawIndexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed).</span></span> <span data-ttu-id="40a0e-189">Es ist wichtig zu verstehen, dass dieser Aufruf (oder andere ähnliche **Draw _-Aufrufe, die \* *für _ Verknüpfung id3d11devicecontext aus definiert*** sind) tatsächlich die Pipeline ausführt.</span><span class="sxs-lookup"><span data-stu-id="40a0e-189">It’s important to understand that this call (or other similar \**Draw\**_ calls defined on _\* ID3D11DeviceContext\*\*) actually executes the pipeline.</span></span> <span data-ttu-id="40a0e-190">Dies gilt insbesondere dann, wenn Direct3D mit der GPU kommuniziert, um den Zeichnungs Zustand festzulegen, jede Pipeline Phase ausführt und die Pixel Ergebnisse in die renderzielpufferressource für die Anzeige durch die Swapkette schreibt.</span><span class="sxs-lookup"><span data-stu-id="40a0e-190">Specifically, this is when Direct3D communicates with the GPU to set drawing state, runs each pipeline stage, and writes the pixel results into the render-target buffer resource for display by the swap chain.</span></span> <span data-ttu-id="40a0e-191">Da die Kommunikation zwischen CPU und GPU einen mehr Aufwand verursacht, kombinieren Sie mehrere Draw-Aufrufe in einem einzigen, wenn dies möglich ist. Dies gilt insbesondere, wenn die Szene viele gerenderte Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="40a0e-191">Since communication between the CPU and GPU incurs overhead, combine multiple draw calls into a single one if you can, especially if your scene has a lot of rendered objects.</span></span>


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



<span data-ttu-id="40a0e-192">Es empfiehlt sich, die verschiedenen Grafik Pipeline Stufen für den Kontext in der richtigen Reihenfolge festzulegen.</span><span class="sxs-lookup"><span data-stu-id="40a0e-192">It's good practice to set the various graphics pipeline stages on the context in order.</span></span> <span data-ttu-id="40a0e-193">Normalerweise ist die Reihenfolge wie folgt:</span><span class="sxs-lookup"><span data-stu-id="40a0e-193">Typically, the order is:</span></span>

-   <span data-ttu-id="40a0e-194">Aktualisieren konstanter Puffer Ressourcen bei Bedarf mit neuen Daten (mithilfe von Daten aus **Update**).</span><span class="sxs-lookup"><span data-stu-id="40a0e-194">Refresh constant buffer resources with new data as needed (using data from **Update**).</span></span>
-   <span data-ttu-id="40a0e-195">Eingabeassembly (IA): Hier fügen wir den Scheitelpunkt und Index Puffer an, die die Szene Geometrie definieren.</span><span class="sxs-lookup"><span data-stu-id="40a0e-195">Input assembly (IA): This is where we attach the vertex and index buffers that define the scene geometry.</span></span> <span data-ttu-id="40a0e-196">Sie müssen jeden Scheitelpunkt und Index Puffer für jedes Objekt in der Szene anfügen.</span><span class="sxs-lookup"><span data-stu-id="40a0e-196">You need to attach each vertex and index buffer for each object in the scene.</span></span> <span data-ttu-id="40a0e-197">Da dieses Beispiel nur den Cube enthält, ist es recht einfach.</span><span class="sxs-lookup"><span data-stu-id="40a0e-197">Because this example has just the cube, it's pretty simple.</span></span>
-   <span data-ttu-id="40a0e-198">Vertex-Shader (VS): Fügen Sie alle Scheitelpunkt-Shader an, mit denen die Daten in den Scheitelpunkt Puffern transformiert werden, und fügen Sie Konstante Puffer für den Vertexshader an.</span><span class="sxs-lookup"><span data-stu-id="40a0e-198">Vertex shader (VS): Attach any vertex shaders that will transform the data in the vertex buffers, and attach constant buffers for the vertex shader.</span></span>
-   <span data-ttu-id="40a0e-199">Pixel-Shader (PS): Fügen Sie alle Pixel-Shader an, die pro-Pixel-Vorgänge in der rasterisierten Szene ausführen, und fügen Sie Geräte Ressourcen für den Pixelshader (Konstante Puffer, Texturen usw.) an.</span><span class="sxs-lookup"><span data-stu-id="40a0e-199">Pixel shader (PS): Attach any pixel shaders that will perform per-pixel operations in the rasterized scene, and attach device resources for the pixel shader (constant buffers, textures, and so on).</span></span>
-   <span data-ttu-id="40a0e-200">Ausgabe Zusammenführung (OM): Dies ist die Phase, in der Pixel gemischt werden, nachdem die Shader abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="40a0e-200">Output merger (OM): This is the stage where pixels are blended, after the shaders are finished.</span></span> <span data-ttu-id="40a0e-201">Dies ist eine Ausnahme von der Regel, da Sie Ihre tiefen Schablonen und Renderziele anfügen, bevor Sie eine der anderen Stufen festlegen.</span><span class="sxs-lookup"><span data-stu-id="40a0e-201">This is an exception to the rule, because you attach your depth stencils and render targets before setting any of the other stages.</span></span> <span data-ttu-id="40a0e-202">Sie haben möglicherweise mehrere Schablonen und Ziele, wenn Sie über zusätzliche Scheitelpunkt-und Pixel-Shader verfügen, die Texturen generieren, wie z. b. Schatten Zuordnungen, Höhen Zuordnungen oder andere samplingverfahren. in diesem Fall benötigt jeder Zeichnungs Durchlauf die entsprechenden Ziele, bevor Sie eine Draw-Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="40a0e-202">You may have multiple stencils and targets if you have additional vertex and pixel shaders that generate textures such as shadow maps, height maps, or other sampling techniques - in this case, each drawing pass will need the appropriate target(s) set before you call a draw function.</span></span>

<span data-ttu-id="40a0e-203">Im letzten Abschnitt ([Arbeiten mit Shadern und Shaderressourcen](work-with-shaders-and-shader-resources.md)) betrachten wir nun die Shader und besprechen, wie Direct3D Sie ausführt.</span><span class="sxs-lookup"><span data-stu-id="40a0e-203">Next, in the final section ([Work with shaders and shader resources](work-with-shaders-and-shader-resources.md)), we'll look at the shaders and discuss how Direct3D executes them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40a0e-204">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="40a0e-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="40a0e-205">**Als Nächstes**</span><span class="sxs-lookup"><span data-stu-id="40a0e-205">**Up next**</span></span>
</dt> <dt>

[<span data-ttu-id="40a0e-206">Arbeiten mit Shader und Shaderressourcen</span><span class="sxs-lookup"><span data-stu-id="40a0e-206">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
