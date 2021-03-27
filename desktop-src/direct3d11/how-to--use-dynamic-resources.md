---
title: Verwenden dynamischer Ressourcen
description: Sie erstellen und verwenden dynamische Ressourcen, wenn Ihre APP Daten in diesen Ressourcen ändern muss. Sie können für dynamische Verwendung Texturen und Puffer erstellen.
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41e00cda7236040679c7863454e4cc18d81106b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206367"
---
# <a name="how-to-use-dynamic-resources"></a><span data-ttu-id="a606e-104">Gewusst wie: Verwenden von dynamischen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a606e-104">How to: Use dynamic resources</span></span>

<span data-ttu-id="a606e-105">**Wichtige APIs**</span><span class="sxs-lookup"><span data-stu-id="a606e-105">**Important APIs**</span></span>

-   [<span data-ttu-id="a606e-106">**Verknüpfung id3d11devicecontext aus:: map**</span><span class="sxs-lookup"><span data-stu-id="a606e-106">**ID3D11DeviceContext::Map**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [<span data-ttu-id="a606e-107">**Verknüpfung id3d11devicecontext aus:: unmap**</span><span class="sxs-lookup"><span data-stu-id="a606e-107">**ID3D11DeviceContext::Unmap**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [<span data-ttu-id="a606e-108">**D3D11- \_ Verwendung**</span><span class="sxs-lookup"><span data-stu-id="a606e-108">**D3D11\_USAGE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

<span data-ttu-id="a606e-109">Sie erstellen und verwenden dynamische Ressourcen, wenn Ihre APP Daten in diesen Ressourcen ändern muss.</span><span class="sxs-lookup"><span data-stu-id="a606e-109">You create and use dynamic resources when your app needs to change data in those resources.</span></span> <span data-ttu-id="a606e-110">Sie können für dynamische Verwendung Texturen und Puffer erstellen.</span><span class="sxs-lookup"><span data-stu-id="a606e-110">You can create textures and buffers for dynamic usage.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a606e-111">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="a606e-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a606e-112">Technologien</span><span class="sxs-lookup"><span data-stu-id="a606e-112">Technologies</span></span>

-   [<span data-ttu-id="a606e-113">Vorgehensweise: Erstellen einer Textur</span><span class="sxs-lookup"><span data-stu-id="a606e-113">How to: Create a Texture</span></span>](overviews-direct3d-11-resources-textures-create.md)
-   [<span data-ttu-id="a606e-114">Gewusst wie: Programm gesteuertes Initialisieren einer Textur</span><span class="sxs-lookup"><span data-stu-id="a606e-114">How to: Initialize a Texture Programmatically</span></span>](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [<span data-ttu-id="a606e-115">Vorgehensweise: Erstellen eines konstanten Puffers</span><span class="sxs-lookup"><span data-stu-id="a606e-115">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a><span data-ttu-id="a606e-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="a606e-116">Prerequisites</span></span>

<span data-ttu-id="a606e-117">Es wird davon ausgegangen, dass Sie mit C+ vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="a606e-117">We assume that you are familiar with C++.</span></span> <span data-ttu-id="a606e-118">Sie müssen außerdem mit den grundlegenden Konzepten der Grafikprogrammierung vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="a606e-118">You also need basic experience with graphics programming concepts.</span></span>

## <a name="instructions"></a><span data-ttu-id="a606e-119">Instructions</span><span class="sxs-lookup"><span data-stu-id="a606e-119">Instructions</span></span>

### <a name="step-1-specify-dynamic-usage"></a><span data-ttu-id="a606e-120">Schritt 1: Angeben der dynamischen Verwendung</span><span class="sxs-lookup"><span data-stu-id="a606e-120">Step 1: Specify dynamic usage</span></span>

<span data-ttu-id="a606e-121">Wenn Sie möchten, dass Ihre APP Änderungen an Ressourcen vornehmen kann, müssen Sie diese Ressourcen als dynamisch und beschreibbar festlegen, wenn Sie Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="a606e-121">If you want your app to be able to make changes to resources, you must specify those resources as dynamic and writable when you create them.</span></span>

<span data-ttu-id="a606e-122">**So geben Sie die dynamische Verwendung an**</span><span class="sxs-lookup"><span data-stu-id="a606e-122">**To specify dynamic usage**</span></span>

1.  <span data-ttu-id="a606e-123">Geben Sie die Ressourcenverwendung als dynamisch an.</span><span class="sxs-lookup"><span data-stu-id="a606e-123">Specify the resource usage as dynamic.</span></span> <span data-ttu-id="a606e-124">Geben Sie z. b. den dynamischen Wert " [**D3D11 \_ \_ Usage**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) " im **Usage** -Member des [**D3D11- \_ Puffers \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) für einen Scheitelpunkt oder Konstanten Puffer an, und geben Sie den dynamischen Wert für die **D3D11- \_ Verwendung \_** im **Usage** -Member von [**D3D11 \_ TEXTURE2D \_ de SC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) für eine 2D-Textur an.</span><span class="sxs-lookup"><span data-stu-id="a606e-124">For example, specify the [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) value in the **Usage** member of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) for a vertex or constant buffer and specify the **D3D11\_USAGE\_DYNAMIC** value in the **Usage** member of [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) for a 2D texture.</span></span>
2.  <span data-ttu-id="a606e-125">Geben Sie die Ressource als beschreibbar an.</span><span class="sxs-lookup"><span data-stu-id="a606e-125">Specify the resource as writable.</span></span> <span data-ttu-id="a606e-126">Geben Sie z. b. den [**D3D11 \_ CPU \_ Access \_ Write**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) -Wert im **cpuaccessflags** -Member von [**D3D11 \_ buffer \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) oder [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)an.</span><span class="sxs-lookup"><span data-stu-id="a606e-126">For example, specify the [**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) value in the **CPUAccessFlags** member of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) or [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).</span></span>
3.  <span data-ttu-id="a606e-127">Übergeben Sie die Ressourcen Beschreibung an die Erstellungs Funktion.</span><span class="sxs-lookup"><span data-stu-id="a606e-127">Pass the resource description to the creation function.</span></span> <span data-ttu-id="a606e-128">Übergeben Sie z. b. die Adresse des [**D3D11- \_ Puffers \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) an [**ID3D11Device:: up Buffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) , und übergeben Sie die Adresse von [**D3D11 \_ TEXTURE2D \_ de SC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) an [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).</span><span class="sxs-lookup"><span data-stu-id="a606e-128">For example, pass the address of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) to [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) and pass the address of [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) to [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).</span></span>

<span data-ttu-id="a606e-129">Im folgenden finden Sie ein Beispiel für die Erstellung eines dynamischen Scheitelpunkt Puffers:</span><span class="sxs-lookup"><span data-stu-id="a606e-129">Here is an example of creating a dynamic vertex buffer:</span></span>


```C++
    // Create a vertex buffer for a triangle.

    float2 triangleVertices[] =
    {
        float2(-0.5f, -0.5f),
        float2(0.0f, 0.5f),
        float2(0.5f, -0.5f),
    };

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(float2)* ARRAYSIZE(triangleVertices);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;
    vertexBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
    vertexBufferDesc.MiscFlags = 0;
    vertexBufferDesc.StructureByteStride = 0;

    D3D11_SUBRESOURCE_DATA vertexBufferData;
    vertexBufferData.pSysMem = triangleVertices;
    vertexBufferData.SysMemPitch = 0;
    vertexBufferData.SysMemSlicePitch = 0;

    DX::ThrowIfFailed(
        m_d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        &vertexBufferData,
        &vertexBuffer2
        )
        );

```



### <a name="step-2-change-a-dynamic-resource"></a><span data-ttu-id="a606e-130">Schritt 2: Ändern einer dynamischen Ressource</span><span class="sxs-lookup"><span data-stu-id="a606e-130">Step 2: Change a dynamic resource</span></span>

<span data-ttu-id="a606e-131">Wenn Sie beim Erstellen eine Ressource als dynamisch und beschreibbar angegeben haben, können Sie später Änderungen an dieser Ressource vornehmen.</span><span class="sxs-lookup"><span data-stu-id="a606e-131">If you specified a resource as dynamic and writable when you created it, you can later make changes to that resource.</span></span>

<span data-ttu-id="a606e-132">**So ändern Sie Daten in einer dynamischen Ressource**</span><span class="sxs-lookup"><span data-stu-id="a606e-132">**To change data in a dynamic resource**</span></span>

1.  <span data-ttu-id="a606e-133">Richten Sie die neuen Daten für die Ressource ein.</span><span class="sxs-lookup"><span data-stu-id="a606e-133">Set up the new data for the resource.</span></span> <span data-ttu-id="a606e-134">Deklarieren Sie eine D3D11 zugeordnete unter [**\_ \_ geordnete Quellentyp**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) Variable, und initialisieren Sie Sie mit NULL.</span><span class="sxs-lookup"><span data-stu-id="a606e-134">Declare a [**D3D11\_MAPPED\_SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) type variable and initialize it to zero.</span></span> <span data-ttu-id="a606e-135">Sie verwenden diese Variable, um die Ressource zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a606e-135">You'll use this variable to change the resource.</span></span>
2.  <span data-ttu-id="a606e-136">Deaktivieren Sie den GPU-Zugriff (Graphics Processing Unit) auf die Daten, die Sie ändern möchten, und erhalten Sie einen Zeiger auf den Arbeitsspeicher, der die Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="a606e-136">Disable graphics processing unit (GPU) access to the data that you want to change and get a pointer to the memory that contains the data.</span></span> <span data-ttu-id="a606e-137">Um diesen Zeiger zu erhalten, übergeben Sie [**D3D11 \_ map \_ Write \_ verwerfen**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) an den *maptype* -Parameter, wenn Sie [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a606e-137">To get this pointer, pass [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) to the *MapType* parameter when you call [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span> <span data-ttu-id="a606e-138">Legen Sie diesen Zeiger auf die Adresse der D3D11 zugeordneten untergeordneten [**\_ \_ Quell**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) Variablen aus dem vorherigen Schritt fest.</span><span class="sxs-lookup"><span data-stu-id="a606e-138">Set this pointer to the address of the [**D3D11\_MAPPED\_SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) variable from the previous step.</span></span>
3.  <span data-ttu-id="a606e-139">Schreiben Sie die neuen Daten in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a606e-139">Write the new data to the memory.</span></span>
4.  <span data-ttu-id="a606e-140">Aufrufen von [**Verknüpfung id3d11devicecontext aus:: unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) zum erneuten Aktivieren des GPU-Zugriffs auf die Daten, wenn Sie mit dem Schreiben der neuen Daten fertig sind.</span><span class="sxs-lookup"><span data-stu-id="a606e-140">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) to reenable GPU access to the data when you're finished writing the new data.</span></span>

<span data-ttu-id="a606e-141">Im folgenden finden Sie ein Beispiel für das Ändern eines dynamischen Scheitelpunkt Puffers:</span><span class="sxs-lookup"><span data-stu-id="a606e-141">Here is an example of changing a dynamic vertex buffer:</span></span>


```C++
// This might get called as the result of a click event to double the size of the triangle.
void TriangleRenderer::MapDoubleVertices()
{
    D3D11_MAPPED_SUBRESOURCE mappedResource;
    ZeroMemory(&mappedResource, sizeof(D3D11_MAPPED_SUBRESOURCE));
    float2 vertices[] =
    {
        float2(-1.0f, -1.0f),
        float2(0.0f, 1.0f),
        float2(1.0f, -1.0f),
    };
    //  Disable GPU access to the vertex buffer data.
    auto m_d3dContext = m_deviceResources->GetD3DDeviceContext();
    m_d3dContext->Map(vertexBuffer2.Get(), 0, D3D11_MAP_WRITE_DISCARD, 0, &mappedResource);
    //  Update the vertex buffer here.
    memcpy(mappedResource.pData, vertices, sizeof(vertices));
    //  Reenable GPU access to the vertex buffer data.
    m_d3dContext->Unmap(vertexBuffer2.Get(), 0);
}
```



## <a name="remarks"></a><span data-ttu-id="a606e-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a606e-142">Remarks</span></span>

### <a name="using-dynamic-textures"></a><span data-ttu-id="a606e-143">Verwenden dynamischer Texturen</span><span class="sxs-lookup"><span data-stu-id="a606e-143">Using dynamic textures</span></span>

<span data-ttu-id="a606e-144">Es wird empfohlen, nur eine dynamische Textur Pro Format und möglicherweise pro Größe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a606e-144">We recommend that you create only one dynamic texture per format and possibly per size.</span></span> <span data-ttu-id="a606e-145">Das Erstellen dynamischer Mipmaps, Cubes und Volumes ist aufgrund des zusätzlichen Aufwands bei der Zuordnung jeder Ebene nicht empfehlenswert.</span><span class="sxs-lookup"><span data-stu-id="a606e-145">We don't recommend creating dynamic mipmaps, cubes, and volumes because of the additional overhead in mapping every level.</span></span> <span data-ttu-id="a606e-146">Für Mipmaps können Sie [**D3D11 \_ map \_ Write \_ verwerfen**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) nur auf der obersten Ebene angeben.</span><span class="sxs-lookup"><span data-stu-id="a606e-146">For mipmaps, you can specify [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) only on the top level.</span></span> <span data-ttu-id="a606e-147">Alle Ebenen werden verworfen, indem nur die oberste Ebene abgeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="a606e-147">All levels are discarded by mapping just the top level.</span></span> <span data-ttu-id="a606e-148">Dieses Verhalten ist für Volumes und Cubes identisch.</span><span class="sxs-lookup"><span data-stu-id="a606e-148">This behavior is the same for volumes and cubes.</span></span> <span data-ttu-id="a606e-149">Bei Cubes werden die oberste Ebene und die Vorderseite 0 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a606e-149">For cubes, the top level and face 0 are mapped.</span></span>

### <a name="using-dynamic-buffers"></a><span data-ttu-id="a606e-150">Verwenden dynamischer Puffer</span><span class="sxs-lookup"><span data-stu-id="a606e-150">Using dynamic buffers</span></span>

<span data-ttu-id="a606e-151">Wenn Sie die [**Zuordnung auf einem**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) statischen Scheitelpunkt Puffer aufzurufen, während die GPU den Puffer verwendet, erhalten Sie eine beträchtliche Leistungs Einbuße.</span><span class="sxs-lookup"><span data-stu-id="a606e-151">When you call [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) on a static vertex buffer while the GPU is using the buffer, you get a significant performance penalty.</span></span> <span data-ttu-id="a606e-152">In dieser Situation muss **map** warten, bis die GPU das Lesen von Vertex-oder Indexdaten aus dem Puffer abgeschlossen hat, bevor **map** an die aufrufende App zurückgegeben werden kann, was zu einer erheblichen Verzögerung führt.</span><span class="sxs-lookup"><span data-stu-id="a606e-152">In this situation, **Map** must wait until the GPU is finished reading vertex or index data from the buffer before **Map** can return to the calling app, which causes a significant delay.</span></span> <span data-ttu-id="a606e-153">Wenn Sie **map** und das anschließende Rendering von einem statischen Puffer mehrmals pro Frame aufrufen, wird außerdem verhindert, dass die GPU renderingbefehle puffert, da Sie vor dem Zurückgeben des Karten Zeigers Befehle beenden muss.</span><span class="sxs-lookup"><span data-stu-id="a606e-153">Calling **Map** and then rendering from a static buffer several times per frame also prevents the GPU from buffering rendering commands because it must finish commands before returning the map pointer.</span></span> <span data-ttu-id="a606e-154">Ohne gepufferte Befehle bleibt die GPU im Leerlauf, bis die APP das Ausfüllen des Vertex-Puffers oder Index Puffers abgeschlossen hat und einen Renderingbefehl ausgibt.</span><span class="sxs-lookup"><span data-stu-id="a606e-154">Without buffered commands, the GPU remains idle until after the app is finished filling the vertex buffer or index buffer and issues a rendering command.</span></span>

<span data-ttu-id="a606e-155">Im Idealfall würden sich die Scheitelpunkt-oder Indexdaten nie ändern, aber dies ist nicht immer möglich.</span><span class="sxs-lookup"><span data-stu-id="a606e-155">Ideally the vertex or index data would never change, but this is not always possible.</span></span> <span data-ttu-id="a606e-156">Es gibt viele Situationen, in denen die APP den Scheitelpunkt oder Indexdaten jedes Frames ändern muss, vielleicht sogar mehrmals pro Frame.</span><span class="sxs-lookup"><span data-stu-id="a606e-156">There are many situations where the app needs to change vertex or index data every frame, perhaps even multiple times per frame.</span></span> <span data-ttu-id="a606e-157">In diesen Fällen wird empfohlen, dass Sie den Scheitelpunkt oder Index Puffer mit [**\_ \_ dynamischer D3D11-Verwendung**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)erstellen.</span><span class="sxs-lookup"><span data-stu-id="a606e-157">For these situations, we recommend that you create the vertex or index buffer with [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span></span> <span data-ttu-id="a606e-158">Dieses nutzungsflag bewirkt, dass die Laufzeit bei häufigen Zuordnungs Vorgängen optimiert wird.</span><span class="sxs-lookup"><span data-stu-id="a606e-158">This usage flag causes the runtime to optimize for frequent map operations.</span></span> <span data-ttu-id="a606e-159">**D3D11 \_ Die Verwendung von \_ Dynamic** ist nur nützlich, wenn der Puffer häufig zugeordnet wird. Wenn die Daten konstant bleiben sollen, platzieren Sie diese Daten in einem statischen Scheitelpunkt oder Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="a606e-159">**D3D11\_USAGE\_DYNAMIC** is only useful when the buffer is mapped frequently; if data is to remain constant, place that data in a static vertex or index buffer.</span></span>

<span data-ttu-id="a606e-160">Um eine Leistungsverbesserung bei der Verwendung dynamischer Scheitelpunkt Puffer zu erhalten, muss Ihre APP [**map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) mit den entsprechenden [**D3D11 \_ map**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) -Werten aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a606e-160">To receive a performance improvement when you use dynamic vertex buffers, your app must call [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) with the appropriate [**D3D11\_MAP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) values.</span></span> <span data-ttu-id="a606e-161">[**D3D11 \_ Die \_ Schreib \_ Verwerfungs**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) Zuordnung gibt an, dass die APP die alten Scheitelpunkt-oder Indexdaten nicht im Puffer aufbewahren muss.</span><span class="sxs-lookup"><span data-stu-id="a606e-161">[**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indicates that the app doesn't need to keep the old vertex or index data in the buffer.</span></span> <span data-ttu-id="a606e-162">Wenn die GPU den Puffer weiterhin verwendet, wenn Sie **map** mit **D3D11 \_ map \_ Write \_ verwerfen** verwenden, gibt die Laufzeit einen Zeiger auf einen neuen Speicherbereich anstelle der alten Puffer Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="a606e-162">If the GPU is still using the buffer when you call **Map** with **D3D11\_MAP\_WRITE\_DISCARD**, the runtime returns a pointer to a new region of memory instead of the old buffer data.</span></span> <span data-ttu-id="a606e-163">Dadurch kann die GPU die alten Daten weiterhin verwenden, während die APP Daten in den neuen Puffer platziert.</span><span class="sxs-lookup"><span data-stu-id="a606e-163">This allows the GPU to continue using the old data while the app places data in the new buffer.</span></span> <span data-ttu-id="a606e-164">In der APP ist keine zusätzliche Speicherverwaltung erforderlich. der alte Puffer wird wieder verwendet oder automatisch zerstört, wenn die GPU damit fertig ist.</span><span class="sxs-lookup"><span data-stu-id="a606e-164">No additional memory management is required in the app; the old buffer is reused or destroyed automatically when the GPU is finished with it.</span></span>

> [!Note]  
> <span data-ttu-id="a606e-165">Wenn Sie einen Puffer mit [**D3D11 \_ map \_ Write \_ verwerfen**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)zuordnen, verwirft die Common Language Runtime immer den gesamten Puffer.</span><span class="sxs-lookup"><span data-stu-id="a606e-165">When you map a buffer with [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), the runtime always discards the entire buffer.</span></span> <span data-ttu-id="a606e-166">Informationen in nicht zugeordneten Bereichen des Puffers können nicht beibehalten werden, indem Sie ein Offset oder ein Feld mit eingeschränkter Größe angeben.</span><span class="sxs-lookup"><span data-stu-id="a606e-166">You can't preserve info in unmapped areas of the buffer by specifying a nonzero offset or limited size field.</span></span>

 

<span data-ttu-id="a606e-167">Es gibt Fälle, in denen die Datenmenge, die in der APP gespeichert werden muss, klein ist, z. b. das Hinzufügen von vier Vertices zum Rendering eines Sprite.</span><span class="sxs-lookup"><span data-stu-id="a606e-167">There are cases where the amount of data the app needs to store per map is small, such as adding four vertices to render a sprite.</span></span> <span data-ttu-id="a606e-168">[**D3D11 \_ Map \_ Write \_ No \_ Überschreibung**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) gibt an, dass die APP keine Daten überschreibt, die bereits im dynamischen Puffer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a606e-168">[**D3D11\_MAP\_WRITE\_NO\_OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indicates that the app will not overwrite data already in use in the dynamic buffer.</span></span> <span data-ttu-id="a606e-169">Der [](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) Zuordnungs Befehl gibt einen Zeiger auf die alten Daten zurück, wodurch die APP neue Daten in nicht verwendeten Bereichen des Scheitel Punkts oder Index Puffers hinzufügen kann.</span><span class="sxs-lookup"><span data-stu-id="a606e-169">The [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) call will return a pointer to the old data, which will allow the app to add new data in unused regions of the vertex or index buffer.</span></span> <span data-ttu-id="a606e-170">Die APP darf keine Scheitel Punkte oder Indizes ändern, die in einem zeichnen-Vorgang verwendet werden, da Sie möglicherweise noch von der GPU verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a606e-170">The app must not modify vertices or indices that are used in a draw operation as they might still be in use by the GPU.</span></span> <span data-ttu-id="a606e-171">Es wird empfohlen, dass die APP dann [**D3D11 \_ map \_ Write \_ verwerfen**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) verwendet, nachdem der dynamische Puffer voll ist, um einen neuen Arbeitsbereich zu erhalten, der die alten Scheitelpunkt-oder Indexdaten nach Abschluss der GPU verwirft.</span><span class="sxs-lookup"><span data-stu-id="a606e-171">We recommend that the app then use [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) after the dynamic buffer is full to receive a new region of memory, which discards the old vertex or index data after the GPU is finished.</span></span>

<span data-ttu-id="a606e-172">Der asynchrone Abfrage Mechanismus ist hilfreich, um zu bestimmen, ob Scheitel Punkte weiterhin von der GPU verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a606e-172">The asynchronous query mechanism is useful to determine if vertices are still in use by the GPU.</span></span> <span data-ttu-id="a606e-173">Geben Sie nach dem letzten zeichnen-Befehl, der die Scheitel Punkte verwendet, eine Abfrage vom Typ [**D3D11 \_ Query- \_ Ereignis**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) aus.</span><span class="sxs-lookup"><span data-stu-id="a606e-173">Issue a query of type [**D3D11\_QUERY\_EVENT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) after the last draw call that uses the vertices.</span></span> <span data-ttu-id="a606e-174">Die Scheitel Punkte werden nicht mehr verwendet, wenn [**Verknüpfung id3d11devicecontext aus:: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) S \_ OK zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a606e-174">The vertices are no longer in use when [**ID3D11DeviceContext::GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) returns S\_OK.</span></span> <span data-ttu-id="a606e-175">Wenn Sie einen Puffer mit [**D3D11 \_ map \_ Write \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) oder No Map Values zuordnen, sind Sie immer sicher, dass die Vertices ordnungsgemäß mit der GPU synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a606e-175">When you map a buffer with [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) or no map values, you are always guaranteed that the vertices are synchronized properly with the GPU.</span></span> <span data-ttu-id="a606e-176">Wenn Sie jedoch die Zuordnung ohne Kartenwerte durchführt, wird die zuvor beschriebene Leistungs Einbuße verursacht.</span><span class="sxs-lookup"><span data-stu-id="a606e-176">But, when you map without map values, you will incur the performance penalty described earlier.</span></span>

> [!Note]  
> <span data-ttu-id="a606e-177">Die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist, ermöglicht das Zuordnen dynamischer konstanter Puffer und der Shader-Ressourcen Sichten (Srvs) dynamischer Puffer mit [**D3D11 \_ map \_ Write \_ No über \_ Schreiben**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map).</span><span class="sxs-lookup"><span data-stu-id="a606e-177">The Direct3D 11.1 runtime, which is available starting with Windows 8, enables mapping dynamic constant buffers and shader resource views (SRVs) of dynamic buffers with [**D3D11\_MAP\_WRITE\_NO\_OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map).</span></span> <span data-ttu-id="a606e-178">Mit den Laufzeiten "Direct3D 11" und "frühere Laufzeiten" wurde die Zuordnung von partiellen Updates zum Scheitelpunkt oder Index Puffer eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="a606e-178">The Direct3D 11 and earlier runtimes limited no-overwrite partial-update mapping to vertex or index buffers.</span></span> <span data-ttu-id="a606e-179">Um zu ermitteln, ob ein Direct3D-Gerät diese Features unterstützt, wenden Sie [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) mit [**D3D11 \_ Feature \_ D3D11- \_ Optionen**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)an.</span><span class="sxs-lookup"><span data-stu-id="a606e-179">To determine if a Direct3D device supports these features, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).</span></span> <span data-ttu-id="a606e-180">**Checkfeaturesupport** füllt Mitglieder einer [**D3D11 \_ Feature \_ Data \_ D3D11 \_ options**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) -Struktur mit den Funktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="a606e-180">**CheckFeatureSupport** fills members of a [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) structure with the device's features.</span></span> <span data-ttu-id="a606e-181">Die relevanten Elemente sind " **mapnooverwrite teondynamicconstantbuffer** " und " **mapnooverwrite teondynamicbuffersrv**".</span><span class="sxs-lookup"><span data-stu-id="a606e-181">The relevant members here are **MapNoOverwriteOnDynamicConstantBuffer** and **MapNoOverwriteOnDynamicBufferSRV**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a606e-182">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a606e-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a606e-183">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="a606e-183">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




