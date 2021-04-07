---
description: Das Erstellen von Puffern erfordert das Definieren der Daten, die der Puffer speichert, das Bereitstellen von Initialisierungs Daten und das Einrichten entsprechender Verwendungs-und Bindungsflags. Informationen zum Erstellen von Texturen finden Sie unter Erstellen von Textur Ressourcen (Direct3D 10).
ms.assetid: 9787b153-9301-4a0f-bd6f-21cc6f7fc650
title: Erstellen von Puffer Ressourcen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d711265775c430728fbcffecd364f746580a566
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748513"
---
# <a name="creating-buffer-resources-direct3d-10"></a><span data-ttu-id="713a0-104">Erstellen von Puffer Ressourcen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="713a0-104">Creating Buffer Resources (Direct3D 10)</span></span>

<span data-ttu-id="713a0-105">Das Erstellen von Puffern erfordert das Definieren der Daten, die der Puffer speichert, das Bereitstellen von Initialisierungs Daten und das Einrichten entsprechender Verwendungs-und Bindungsflags.</span><span class="sxs-lookup"><span data-stu-id="713a0-105">Creating buffers requires defining the data that the buffer will store, providing initialization data, and setting up appropriate usage and binding flags.</span></span> <span data-ttu-id="713a0-106">Informationen zum Erstellen von Texturen finden Sie unter [Erstellen von Textur Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).</span><span class="sxs-lookup"><span data-stu-id="713a0-106">To create textures, see [Creating Texture Resources (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).</span></span>

-   [<span data-ttu-id="713a0-107">Erstellen eines Scheitelpunkt Puffers</span><span class="sxs-lookup"><span data-stu-id="713a0-107">Create a Vertex Buffer</span></span>](#create-a-vertex-buffer)
    -   [<span data-ttu-id="713a0-108">Erstellen einer Puffer Beschreibung</span><span class="sxs-lookup"><span data-stu-id="713a0-108">Create a Buffer Description</span></span>](#create-a-buffer-description)
    -   [<span data-ttu-id="713a0-109">Initialisierungs Daten für den Puffer erstellen</span><span class="sxs-lookup"><span data-stu-id="713a0-109">Create the Initialization Data for the Buffer</span></span>](#create-the-initialization-data-for-the-buffer)
    -   [<span data-ttu-id="713a0-110">Erstellen des Puffers</span><span class="sxs-lookup"><span data-stu-id="713a0-110">Create the Buffer</span></span>](#create-the-buffer)
-   [<span data-ttu-id="713a0-111">Erstellen eines Index Puffers</span><span class="sxs-lookup"><span data-stu-id="713a0-111">Create an Index Buffer</span></span>](#create-an-index-buffer)
-   [<span data-ttu-id="713a0-112">Erstellen eines konstanten Puffers</span><span class="sxs-lookup"><span data-stu-id="713a0-112">Create a Constant Buffer</span></span>](#create-a-constant-buffer)
-   [<span data-ttu-id="713a0-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="713a0-113">Related topics</span></span>](#related-topics)

## <a name="create-a-vertex-buffer"></a><span data-ttu-id="713a0-114">Erstellen eines Scheitelpunkt Puffers</span><span class="sxs-lookup"><span data-stu-id="713a0-114">Create a Vertex Buffer</span></span>

<span data-ttu-id="713a0-115">Die Schritte zum Erstellen eines [Scheitelpunkt Puffers](d3d10-graphics-programming-guide-resources-types.md) lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="713a0-115">The steps to creating a [vertex buffer](d3d10-graphics-programming-guide-resources-types.md) are as follows.</span></span>

-   [<span data-ttu-id="713a0-116">Erstellen einer Puffer Beschreibung</span><span class="sxs-lookup"><span data-stu-id="713a0-116">Create a Buffer Description</span></span>](#create-a-buffer-description)
-   [<span data-ttu-id="713a0-117">Initialisierungs Daten für den Puffer erstellen</span><span class="sxs-lookup"><span data-stu-id="713a0-117">Create the Initialization Data for the Buffer</span></span>](#create-the-initialization-data-for-the-buffer)
-   [<span data-ttu-id="713a0-118">Erstellen des Puffers</span><span class="sxs-lookup"><span data-stu-id="713a0-118">Create the Buffer</span></span>](#create-the-buffer)

### <a name="create-a-buffer-description"></a><span data-ttu-id="713a0-119">Erstellen einer Puffer Beschreibung</span><span class="sxs-lookup"><span data-stu-id="713a0-119">Create a Buffer Description</span></span>

<span data-ttu-id="713a0-120">Beim Erstellen eines Scheitelpunkt Puffers wird eine Puffer Beschreibung (siehe [**d3d10 \_ buffer \_**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)Debug) verwendet, um zu definieren, wie Daten im Puffer organisiert werden, wie die Pipeline auf den Puffer zugreifen kann und wie der Puffer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="713a0-120">When creating a vertex buffer, a buffer description (see [**D3D10\_BUFFER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) is used to define how data is organized within the buffer, how the pipeline can access the buffer, and how the buffer will be used.</span></span>

<span data-ttu-id="713a0-121">Im folgenden Beispiel wird veranschaulicht, wie eine Puffer Beschreibung für ein einzelnes Dreieck mit Scheitel Punkten erstellt wird, die Positions-und Farbwerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="713a0-121">The following example demonstrates how to create a buffer description for a single triangle with vertices that contain position and color values.</span></span>


```
struct SimpleVertex
{
    D3DXVECTOR3 Position;  
    D3DXVECTOR3 Color;  
};

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertex ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
```



<span data-ttu-id="713a0-122">In diesem Beispiel wird die Puffer Beschreibung mit fast allen Standardeinstellungen für die [**Verwendung**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), den [**CPU-Zugriff**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) und [**verschiedene Flags**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)initialisiert.</span><span class="sxs-lookup"><span data-stu-id="713a0-122">In this example, the buffer description is initialized with almost all default settings for [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**CPU access**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) and [**miscellaneous flags**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag).</span></span> <span data-ttu-id="713a0-123">Die anderen Einstellungen gelten für das [**Bind-Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) , das die Ressource nur als Vertex-Puffer identifiziert, und die Größe des Puffers.</span><span class="sxs-lookup"><span data-stu-id="713a0-123">The other settings are for the [**bind flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) which identifies the resource as a vertex buffer only, and the size of the buffer.</span></span>

<span data-ttu-id="713a0-124">Die Nutzungs-und CPU-Zugriffsflags sind wichtig für die Leistung.</span><span class="sxs-lookup"><span data-stu-id="713a0-124">The usage and CPU access flags are important for performance.</span></span> <span data-ttu-id="713a0-125">Diese beiden Flags bestimmen, wie oft auf eine Ressource zugegriffen wird, welche Art von Arbeitsspeicher die Ressource in geladen werden kann und welcher Prozessor auf die Ressource zugreifen muss.</span><span class="sxs-lookup"><span data-stu-id="713a0-125">These two flags together determine how often a resource gets accessed, what type of memory the resource could be loaded into, and what processor needs to access the resource.</span></span> <span data-ttu-id="713a0-126">Standardverwendung diese Ressource wird nicht sehr häufig aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="713a0-126">Default usage this resource will not be updated very often.</span></span> <span data-ttu-id="713a0-127">Das Festlegen des CPU-Zugriffs auf 0 bedeutet, dass die CPU die Ressource weder lesen noch schreiben muss.</span><span class="sxs-lookup"><span data-stu-id="713a0-127">Setting CPU access to 0 means that the CPU will not need to either read or write the resource.</span></span> <span data-ttu-id="713a0-128">In Kombination bedeutet dies, dass die Runtime die Ressource in den höchsten Arbeitsspeicher für die GPU laden kann, da die Ressource keinen CPU-Zugriff benötigt.</span><span class="sxs-lookup"><span data-stu-id="713a0-128">Taken in combination, this means that the runtime can load the resource into the highest performing memory for the GPU since the resource does not require CPU access.</span></span>

<span data-ttu-id="713a0-129">Erwartungsgemäß gibt es einen Kompromiss zwischen der optimalen Leistung und der beliebigen Zeit Barrierefreiheit durch beide Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="713a0-129">As expected, there is a tradeoff between best performance and any-time accessibility by either processor.</span></span> <span data-ttu-id="713a0-130">Die Standardverwendung ohne CPU-Zugriff bedeutet beispielsweise, dass die Ressource exklusiv für die GPU verfügbar gemacht werden kann.</span><span class="sxs-lookup"><span data-stu-id="713a0-130">For example, the default usage with no CPU access means that the resource can be made available to the GPU exclusively.</span></span> <span data-ttu-id="713a0-131">Dies kann das Laden der Ressource in den Arbeitsspeicher einschließen, der nicht direkt von der CPU zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="713a0-131">This could include loading the resource into memory not directly accessible by the CPU.</span></span> <span data-ttu-id="713a0-132">Die Ressource kann nur mit [**updatesubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)geändert werden.</span><span class="sxs-lookup"><span data-stu-id="713a0-132">The resource could only be modified with [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).</span></span>

### <a name="create-the-initialization-data-for-the-buffer"></a><span data-ttu-id="713a0-133">Initialisierungs Daten für den Puffer erstellen</span><span class="sxs-lookup"><span data-stu-id="713a0-133">Create the Initialization Data for the Buffer</span></span>

<span data-ttu-id="713a0-134">Ein Puffer ist lediglich eine Auflistung von Elementen und wird als 1D-Array angelegt.</span><span class="sxs-lookup"><span data-stu-id="713a0-134">A buffer is just a collection of elements and is laid out as a 1D array.</span></span> <span data-ttu-id="713a0-135">Demzufolge sind die Speicherplatz Auslastung des System Arbeitsspeichers und der Slice des System Speichers identisch. die Größe der Vertex-Daten Deklaration.</span><span class="sxs-lookup"><span data-stu-id="713a0-135">As a result, the system memory pitch and system memory slice pitch are both the same; the size of the vertex data declaration.</span></span> <span data-ttu-id="713a0-136">Eine Anwendung kann Initialisierungs Daten bereitstellen, wenn ein Puffer mit einer unter [**Quell Beschreibung**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data)erstellt wird, die einen Zeiger auf die eigentlichen Ressourcen Daten enthält und Informationen über die Größe und das Layout der Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="713a0-136">An application can provide initialization data when a buffer is created using a [**subresource description**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), which contains a pointer to the actual resource data and contains information about the size and layout of that data.</span></span>

<span data-ttu-id="713a0-137">Jeder mit der unveränderlichen Verwendung erstellte Puffer (siehe [**d3d10 \_ Usage \_ unveränderliche**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) muss zum Zeitpunkt der Erstellung initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="713a0-137">Any buffer created with immutable usage (see [**D3D10\_USAGE\_IMMUTABLE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) must be initialized at creation time.</span></span> <span data-ttu-id="713a0-138">Puffer, die eines der anderen nutzungsflags verwenden, können nach der Initialisierung mithilfe von [**copyresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**copysubresourceregion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)und [**updatesubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)aktualisiert werden, oder durch Zugriff auf den zugrunde liegenden Speicher mithilfe der [**map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) -Methode.</span><span class="sxs-lookup"><span data-stu-id="713a0-138">Buffers that use any of the other usage flags can be updated after initialization using [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion), and [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource), or by accessing its underlying memory using the [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) method.</span></span>

### <a name="create-the-buffer"></a><span data-ttu-id="713a0-139">Erstellen des Puffers</span><span class="sxs-lookup"><span data-stu-id="713a0-139">Create the Buffer</span></span>

<span data-ttu-id="713a0-140">Wenn Sie die Puffer Beschreibung und die Initialisierungs Daten (optional) verwenden, [**rufen Sie zum**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) Erstellen eines Scheitel Punkts den Scheitelpunkt-Puffer auf.</span><span class="sxs-lookup"><span data-stu-id="713a0-140">Using the buffer description and the initialization data (which is optional) call [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) to create a vertex buffer.</span></span> <span data-ttu-id="713a0-141">Der folgende Code Ausschnitt veranschaulicht, wie ein Scheitelpunkt Puffer aus einem Array von Scheitelpunkt Daten erstellt wird, die von der Anwendung deklariert wurden.</span><span class="sxs-lookup"><span data-stu-id="713a0-141">The following code snippet demonstrates how to create a vertex buffer from an array of vertex data declared by the application.</span></span>


```
struct SimpleVertexCombined
{
    D3DXVECTOR3 Pos;  
    D3DXVECTOR3 Col;  
};


ID3D10InputLayout* g_pVertexLayout = NULL;
ID3D10Buffer*      g_pVertexBuffer[2] = { NULL, NULL };
ID3D10Buffer*      g_pIndexBuffer = NULL;


SimpleVertexCombined verticesCombo[] =
{
    D3DXVECTOR3( 0.0f, 0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.0f, 0.5f ),
    D3DXVECTOR3( 0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.5f, 0.0f, 0.0f ),
    D3DXVECTOR3( -0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.5f, 0.0f ),
};


    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
    
    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = verticesCombo;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer[0] );
```



## <a name="create-an-index-buffer"></a><span data-ttu-id="713a0-142">Erstellen eines Index Puffers</span><span class="sxs-lookup"><span data-stu-id="713a0-142">Create an Index Buffer</span></span>

<span data-ttu-id="713a0-143">Das Erstellen eines Index Puffers ähnelt stark dem Erstellen eines Scheitelpunkt Puffers. mit zwei unterschieden.</span><span class="sxs-lookup"><span data-stu-id="713a0-143">Creating an index buffer is very similar to creating a vertex buffer; with two differences.</span></span> <span data-ttu-id="713a0-144">Ein Index Puffer enthält nur 16-Bit-oder 32-Bit-Daten (anstelle des breiten Bereichs von Formaten, die für einen Vertex-Puffer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="713a0-144">An index buffer contains only 16-bit or 32-bit data (instead of the wide range of formats available to a vertex buffer.</span></span> <span data-ttu-id="713a0-145">Ein Index Puffer erfordert auch ein Index-Buffer-Bindungsflag.</span><span class="sxs-lookup"><span data-stu-id="713a0-145">An index buffer also requires an index-buffer bind flag.</span></span>

<span data-ttu-id="713a0-146">Im folgenden Beispiel wird veranschaulicht, wie ein Index Puffer aus einem Array von Indexdaten erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="713a0-146">The following example demonstrates how to create an index buffer from an array of index data.</span></span>


```
ID3D10Buffer *g_pIndexBuffer = NULL;

    // Create indices
    unsigned int indices[] = { 0, 1, 2 };

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage           = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
    bufferDesc.BindFlags       = D3D10_BIND_INDEX_BUFFER;
    bufferDesc.CPUAccessFlags  = 0;
    bufferDesc.MiscFlags       = 0;

    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = indices;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
    if( FAILED( hr ) )
        return hr;
  
    g_pd3dDevice->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
```



## <a name="create-a-constant-buffer"></a><span data-ttu-id="713a0-147">Erstellen eines konstanten Puffers</span><span class="sxs-lookup"><span data-stu-id="713a0-147">Create a Constant Buffer</span></span>

<span data-ttu-id="713a0-148">Direct3D 10 führt einen konstanten Puffer ein.</span><span class="sxs-lookup"><span data-stu-id="713a0-148">Direct3D 10 introduces a constant buffer.</span></span> <span data-ttu-id="713a0-149">Ein konstanter Puffer oder Shader-Konstantenpuffer ist ein Puffer, der shaderkonstanten enthält.</span><span class="sxs-lookup"><span data-stu-id="713a0-149">A constant buffer, or shader constant buffer, is a buffer that contains shader constants.</span></span> <span data-ttu-id="713a0-150">Hier ist ein Beispiel für das Erstellen eines konstanten Puffers, der aus dem [HLSLWithoutFX10-Beispiel](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)entnommen wurde.</span><span class="sxs-lookup"><span data-stu-id="713a0-150">Here is an example of creating a constant buffer, taken from the [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>


```
ID3D10Buffer*   g_pConstantBuffer10 = NULL;

struct VS_CONSTANT_BUFFER
{
    D3DXMATRIX mWorldViewProj;      //mWorldViewProj will probably be global to all shaders in a project.
                                    //It's a good idea not to move it around between shaders.
    D3DXVECTOR4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                    //fTime may also be global to all shaders in a project.
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};

    D3D10_BUFFER_DESC cbDesc;
    cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
    cbDesc.Usage = D3D10_USAGE_DYNAMIC;
    cbDesc.BindFlags = D3D10_BIND_CONSTANT_BUFFER;
    cbDesc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
    cbDesc.MiscFlags = 0;
    hr = g_pd3dDevice->CreateBuffer( &cbDesc, NULL, &g_pConstantBuffer10 );
    if( FAILED( hr ) )
       return hr;

    g_pd3dDevice->VSSetConstantBuffers( 0, 1, g_pConstantBuffer10 );
```



<span data-ttu-id="713a0-151">Beachten Sie, dass bei Verwendung der [**ID3D10Effect-Schnittstellen**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) Schnittstelle der Prozess des Erstellens, Bindungs-und Auslassen eines konstanten Puffers von der **ID3D10Effect-Schnittstellen** Instanz verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="713a0-151">Note that when using the [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) interface the process of creating, binding and comitting a constant buffer is handled by the **ID3D10Effect Interface** instance.</span></span> <span data-ttu-id="713a0-152">In diesem Fall ist es nur notwendig, die Variable aus dem Effekt mit einer der GetVariable-Methoden (z. b. [**getvariablebyname**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) ) zu erhalten und die Variable mit einer der SetVariable-Methoden (z. b. [**setMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix)) zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="713a0-152">In that case it is only nescesary to get the variable from the effect with one of the GetVariable methods such as [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) and update the variable with one of the SetVariable methods such as [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix).</span></span> <span data-ttu-id="713a0-153">Ein Beispiel für die Verwendung der **ID3D10Effect-Schnittstelle** zum Verwalten eines konstanten Puffers finden Sie unter [Tutorial 7: Textur Zuordnung und Konstantenpuffer](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="713a0-153">For an example of using **ID3D10Effect Interface** to manage a constant buffer see [Tutorial 7: Texture Mapping and Constant Buffers](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="713a0-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="713a0-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="713a0-155">Ressourcen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="713a0-155">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



