---
title: Ersten Einstieg in die Input-Assembler Phase
description: Zum Initialisieren der Eingabe-Assembler-Phase (IA) müssen einige Schritte ausgeführt werden.
ms.assetid: 84c0ca29-2356-4b7f-98ee-ff1758edc540
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901b3facfef781e3f44acf75bee737f280dece55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390559"
---
# <a name="getting-started-with-the-input-assembler-stage"></a><span data-ttu-id="738cc-103">Ersten Einstieg in die Input-Assembler Phase</span><span class="sxs-lookup"><span data-stu-id="738cc-103">Getting Started with the Input-Assembler Stage</span></span>

<span data-ttu-id="738cc-104">Zum Initialisieren der Eingabe-Assembler-Phase (IA) müssen einige Schritte ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="738cc-104">There are a few steps necessary to initialize the input-assembler (IA) stage.</span></span> <span data-ttu-id="738cc-105">Beispielsweise müssen Sie Puffer Ressourcen mit den Vertex-Daten erstellen, die von der Pipeline benötigt werden, und Sie können die IA-Phase, in der die Puffer sind, und die Art der Daten angeben, die aus den Daten zusammengestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="738cc-105">For example, you need to create buffer resources with the vertex data that the pipeline needs, tell the IA stage where the buffers are and what type of data they contain, and specify the type of primitives to assemble from the data.</span></span>

<span data-ttu-id="738cc-106">In diesem Thema werden die grundlegenden Schritte zum Einrichten der IA-Phase beschrieben, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="738cc-106">The basic steps involved in setting up the IA stage, shown in the following table, are covered in this topic.</span></span>



| <span data-ttu-id="738cc-107">Schritt</span><span class="sxs-lookup"><span data-stu-id="738cc-107">Step</span></span>                                                                                    | <span data-ttu-id="738cc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="738cc-108">Description</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="738cc-109">Eingabepuffer erstellen</span><span class="sxs-lookup"><span data-stu-id="738cc-109">Create Input Buffers</span></span>](#create-input-buffers)                                           | <span data-ttu-id="738cc-110">Erstellen und initialisieren Sie Eingabepuffer mit eingegebenen Scheitelpunkt Daten.</span><span class="sxs-lookup"><span data-stu-id="738cc-110">Create and initialize input buffers with input vertex data.</span></span>                                           |
| [<span data-ttu-id="738cc-111">Erstellen des Input-Layout Objekts</span><span class="sxs-lookup"><span data-stu-id="738cc-111">Create the Input-Layout Object</span></span>](#create-the-input-layout-object)                       | <span data-ttu-id="738cc-112">Legen Sie fest, wie die Vertex-Puffer Daten mithilfe eines Input-Layout-Objekts in die IA-Phase gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="738cc-112">Define how the vertex buffer data will be streamed into the IA stage by using an input-layout object.</span></span> |
| [<span data-ttu-id="738cc-113">Binden von Objekten an die Input-Assembler-Phase</span><span class="sxs-lookup"><span data-stu-id="738cc-113">Bind Objects to the Input-Assembler Stage</span></span>](#bind-objects-to-the-input-assembler-stage) | <span data-ttu-id="738cc-114">Binden Sie die erstellten Objekte (Eingabepuffer und das Eingabe Layout-Objekt) an die IA-Stufe.</span><span class="sxs-lookup"><span data-stu-id="738cc-114">Bind the created objects (input buffers and the input-layout object) to the IA stage.</span></span>                 |
| [<span data-ttu-id="738cc-115">Geben Sie den primitiven Typ an.</span><span class="sxs-lookup"><span data-stu-id="738cc-115">Specify the Primitive Type</span></span>](#specify-the-primitive-type)                               | <span data-ttu-id="738cc-116">Bestimmen Sie, wie die Scheitel Punkte in primitive assembliert werden.</span><span class="sxs-lookup"><span data-stu-id="738cc-116">Identify how the vertices will be assembled into primitives.</span></span>                                          |
| [<span data-ttu-id="738cc-117">Draw-Methoden aufrufen</span><span class="sxs-lookup"><span data-stu-id="738cc-117">Call Draw Methods</span></span>](#call-draw-methods)                                                 | <span data-ttu-id="738cc-118">Senden Sie die Daten, die an die IA-Phase gebunden sind, über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="738cc-118">Send the data bound to the IA stage through the pipeline.</span></span>                                             |



 

<span data-ttu-id="738cc-119">Nachdem Sie diese Schritte verstanden haben, fahren Sie [mit der Verwendung System-Generated Werte](d3d10-graphics-programming-guide-input-assembler-stage-using.md)fort.</span><span class="sxs-lookup"><span data-stu-id="738cc-119">After you understand these steps, move on to [Using System-Generated Values](d3d10-graphics-programming-guide-input-assembler-stage-using.md).</span></span>

## <a name="create-input-buffers"></a><span data-ttu-id="738cc-120">Eingabepuffer erstellen</span><span class="sxs-lookup"><span data-stu-id="738cc-120">Create Input Buffers</span></span>

<span data-ttu-id="738cc-121">Es gibt zwei Typen von Eingabe Puffern: [Vertex-Puffer](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) und Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="738cc-121">There are two types of input buffers: [vertex buffers](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and index buffers.</span></span> <span data-ttu-id="738cc-122">Vertex-Puffer stellen Scheitelpunkt Daten für die IA-Phase bereit.</span><span class="sxs-lookup"><span data-stu-id="738cc-122">Vertex buffers supply vertex data to the IA stage.</span></span> <span data-ttu-id="738cc-123">Index Puffer sind optional. Sie stellen Indizes für Vertices aus dem Scheitelpunkt Puffer bereit.</span><span class="sxs-lookup"><span data-stu-id="738cc-123">Index buffers are optional; they provide indices to vertices from the vertex buffer.</span></span> <span data-ttu-id="738cc-124">Sie können einen oder mehrere Vertex-Puffer und optional einen Index Puffer erstellen.</span><span class="sxs-lookup"><span data-stu-id="738cc-124">You may create one or more vertex buffers and, optionally, an index buffer.</span></span>

<span data-ttu-id="738cc-125">Nachdem Sie die Puffer Ressourcen erstellt haben, müssen Sie ein Eingabe Layoutobjekt erstellen, um das Datenlayout der IA-Phase zu beschreiben. Anschließend müssen Sie die Puffer Ressourcen an die IA-Phase binden.</span><span class="sxs-lookup"><span data-stu-id="738cc-125">After you create the buffer resources, you need to create an input-layout object to describe the data layout to the IA stage, and then you need to bind the buffer resources to the IA stage.</span></span> <span data-ttu-id="738cc-126">Das Erstellen und Binden von Puffern ist nicht erforderlich, wenn die Shader keine Puffer verwenden.</span><span class="sxs-lookup"><span data-stu-id="738cc-126">Creating and binding buffers is not necessary if your shaders don't use buffers.</span></span> <span data-ttu-id="738cc-127">Ein Beispiel für einen einfachen Vertex und einen PixelShader, der ein einzelnes Dreieck zeichnet, finden [Sie unter Verwenden der Input-Assembler Phase ohne Puffer](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="738cc-127">For an example of a simple vertex and pixel shader that draws a single triangle, see [Using the Input-Assembler Stage without Buffers](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).</span></span>

<span data-ttu-id="738cc-128">Hilfe zum Erstellen eines Scheitelpunkt Puffers finden Sie unter [Erstellen eines Scheitelpunkt Puffers](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span><span class="sxs-lookup"><span data-stu-id="738cc-128">For help with creating a vertex buffer, see [Create a Vertex Buffer](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span> <span data-ttu-id="738cc-129">Hilfe zum Erstellen eines Index Puffers finden Sie unter Erstellen eines Index Puffers.</span><span class="sxs-lookup"><span data-stu-id="738cc-129">For help with creating an index buffer, see Create an Index Buffer.</span></span>

## <a name="create-the-input-layout-object"></a><span data-ttu-id="738cc-130">Erstellen des Input-Layout Objekts</span><span class="sxs-lookup"><span data-stu-id="738cc-130">Create the Input-Layout Object</span></span>

<span data-ttu-id="738cc-131">Das Input-Layout-Objekt kapselt den Eingabe Zustand der IA-Stufe.</span><span class="sxs-lookup"><span data-stu-id="738cc-131">The input-layout object encapsulates the input state of the IA stage.</span></span> <span data-ttu-id="738cc-132">Dies schließt eine Beschreibung der Eingabedaten ein, die an die IA-Phase gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="738cc-132">This includes a description of the input data that is bound to the IA stage.</span></span> <span data-ttu-id="738cc-133">Die Daten werden aus dem Arbeitsspeicher von einem oder mehreren Scheitel Punkten aus dem Arbeitsspeicher in die IA-Phase gestreamt.</span><span class="sxs-lookup"><span data-stu-id="738cc-133">The data is streamed into the IA stage from memory, from one or more vertex buffers.</span></span> <span data-ttu-id="738cc-134">Die Beschreibung identifiziert die Eingabedaten, die von einem oder mehreren Scheitelpunkt Puffern gebunden werden, und gibt der Laufzeit die Möglichkeit, die Eingabe Datentypen mit den Eingabeparameter Typen von Shader zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="738cc-134">The description identifies the input data that is bound from one or more vertex buffers and gives the runtime the ability to check the input data types against the shader input parameter types.</span></span> <span data-ttu-id="738cc-135">Bei dieser Typüberprüfung wird nicht nur überprüft, ob die Typen kompatibel sind, sondern auch, dass jedes der Elemente, die der Shader benötigt, in den Puffer Ressourcen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="738cc-135">This type checking not only verifies that the types are compatible, but also that each of the elements that the shader requires is available in the buffer resources.</span></span>

<span data-ttu-id="738cc-136">Ein eingabelayoutobjekt wird aus einem Array von Eingabe Element Beschreibungen und einem Zeiger auf den kompilierten Shader erstellt (siehe [**ID3D11Device:: ":: samateinputlayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)").</span><span class="sxs-lookup"><span data-stu-id="738cc-136">An input-layout object is created from an array of input-element descriptions and a pointer to the compiled shader (see [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)).</span></span> <span data-ttu-id="738cc-137">Das Array enthält mindestens ein Eingabe Element. jedes input-Element beschreibt ein einzelnes Vertex-Data-Element aus einem einzelnen Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="738cc-137">The array contains one or more input elements; each input element describes a single vertex-data element from a single vertex buffer.</span></span> <span data-ttu-id="738cc-138">Der vollständige Satz der Eingabeelementbeschreibungen dient der Beschreibung aller Vertex-Datenelemente von sämtlichen Vertex-Puffern, die an die IA-Phase gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="738cc-138">The entire set of input-element descriptions describes all of the vertex-data elements from all of the vertex buffers that will be bound to the IA stage.</span></span>

<span data-ttu-id="738cc-139">Die folgende layoutbeschreibung beschreibt einen einzelnen Vertex-Puffer, der drei Scheitelpunkt-Datenelemente enthält:</span><span class="sxs-lookup"><span data-stu-id="738cc-139">The following layout description describes a single vertex buffer that contains three vertex-data elements:</span></span>


```
D3D11_INPUT_ELEMENT_DESC layout[] =
{
    { L"POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT, 0, 12, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
};
```



<span data-ttu-id="738cc-140">In einer Eingabe Element Beschreibung werden die einzelnen Elemente eines Scheitel Punkts in einem Vertex-Puffer, einschließlich Größe, Typ, Speicherort und Zweck, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="738cc-140">An input-element description describes each element contained by a single vertex in a vertex buffer, including size, type, location, and purpose.</span></span> <span data-ttu-id="738cc-141">Jede Zeile identifiziert den Datentyp mithilfe der Semantik, des semantischen Indexes und des Datenformats.</span><span class="sxs-lookup"><span data-stu-id="738cc-141">Each row identifies the type of data by using the semantic, the semantic index, and the data format.</span></span> <span data-ttu-id="738cc-142">Eine [Semantik](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) ist eine Text Zeichenfolge, die angibt, wie die Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="738cc-142">A [semantic](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) is a text string that identifies how the data will be used.</span></span> <span data-ttu-id="738cc-143">In diesem Beispiel identifiziert die erste Zeile 3-Komponenten Positionsdaten (z. b.*XYZ*). die zweite Zeile identifiziert Textur Daten mit 2 Komponenten (z. b.*UV*). und die dritte Zeile identifiziert normale Daten.</span><span class="sxs-lookup"><span data-stu-id="738cc-143">In this example, the first row identifies 3-component position data (*xyz*, for example); the second row identifies 2-component texture data (*UV*, for example); and the third row identifies normal data.</span></span>

<span data-ttu-id="738cc-144">In diesem Beispiel für eine Eingabe Element Beschreibung ist der semantische Index (der zweite Parameter) für alle drei Zeilen auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="738cc-144">In this example of an input-element description, the semantic index (which is the second parameter) is set to zero for all three rows.</span></span> <span data-ttu-id="738cc-145">Der semantische Index hilft dabei, zwischen zwei Zeilen zu unterscheiden, die dieselbe Semantik verwenden.</span><span class="sxs-lookup"><span data-stu-id="738cc-145">The semantic index helps distinguish between two rows that use the same semantics.</span></span> <span data-ttu-id="738cc-146">Da in diesem Beispiel keine ähnliche Semantik vorhanden ist, kann der semantische Index auf den Standardwert 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="738cc-146">Since there are no similar semantics in this example, the semantic index can be set to its default value, zero.</span></span>

<span data-ttu-id="738cc-147">Der dritte Parameter ist das *Format*.</span><span class="sxs-lookup"><span data-stu-id="738cc-147">The third parameter is the *format*.</span></span> <span data-ttu-id="738cc-148">Das Format (siehe [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) gibt die Anzahl der Komponenten pro Element und den-Datentyp an, der die Größe der Daten für jedes Element definiert.</span><span class="sxs-lookup"><span data-stu-id="738cc-148">The format (see [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) specifies the number of components per element, and the data type, which defines the size of the data for each element.</span></span> <span data-ttu-id="738cc-149">Das Format kann zum Zeitpunkt der Ressourcen Erstellung vollständig eingegeben werden, oder Sie können eine Ressource mit einem **DXGI- \_ Format** erstellen, das die Anzahl der Komponenten in einem Element identifiziert, der Datentyp jedoch nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="738cc-149">The format can be fully typed at the time of resource creation, or you may create a resource by using a **DXGI\_FORMAT**, which identifies the number of components in an element, but leaves the data type undefined.</span></span>

### <a name="input-slots"></a><span data-ttu-id="738cc-150">Eingabe Slots</span><span class="sxs-lookup"><span data-stu-id="738cc-150">Input Slots</span></span>

<span data-ttu-id="738cc-151">Daten werden in der IA-Phase durch Eingaben aufgerufen, die als *Eingabe Slots* bezeichnet werden, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="738cc-151">Data enters the IA stage through inputs called *input slots*, as shown in the following illustration.</span></span> <span data-ttu-id="738cc-152">Die IA-Phase verfügt über *n* Eingabe Slots, die so konzipiert sind, dass Sie bis zu *n* Vertex-Puffer aufnehmen können, die Eingabedaten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="738cc-152">The IA stage has *n* input slots, which are designed to accommodate up to *n* vertex buffers that provide input data.</span></span> <span data-ttu-id="738cc-153">Jeder Vertex-Puffer muss einem anderen Slot zugewiesen werden. Diese Informationen werden in der Eingabe Layout-Deklaration gespeichert, wenn das Eingabe Layout-Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="738cc-153">Each vertex buffer must be assigned to a different slot; this information is stored in the input-layout declaration when the input-layout object is created.</span></span> <span data-ttu-id="738cc-154">Sie können auch einen Offset vom Anfang jedes Puffers bis zum ersten zu lesenden Element im Puffer angeben.</span><span class="sxs-lookup"><span data-stu-id="738cc-154">You may also specify an offset from the start of each buffer to the first element in the buffer to be read.</span></span>

![Abbildung der Eingabe Slots für die IA-Phase](images/d3d10-ia-slots.png)

<span data-ttu-id="738cc-156">Die nächsten zwei Parameter sind der *Eingabe Slot* und der *Eingabe Offset*.</span><span class="sxs-lookup"><span data-stu-id="738cc-156">The next two parameters are the *input slot* and the *input offset*.</span></span> <span data-ttu-id="738cc-157">Wenn Sie mehrere Puffer verwenden, können Sie diese an einen oder mehrere Eingabe Slots binden.</span><span class="sxs-lookup"><span data-stu-id="738cc-157">When you use multiple buffers, you can bind them to one or more input slots.</span></span> <span data-ttu-id="738cc-158">Der Eingabe Offset ist die Anzahl von Bytes zwischen dem Anfang des Puffers und dem Anfang der Daten.</span><span class="sxs-lookup"><span data-stu-id="738cc-158">The input offset is the number of bytes between the start of the buffer and the beginning of the data.</span></span>

### <a name="reusing-input-layout-objects"></a><span data-ttu-id="738cc-159">Wieder verwenden von Input-Layout Objekten</span><span class="sxs-lookup"><span data-stu-id="738cc-159">Reusing Input-Layout Objects</span></span>

<span data-ttu-id="738cc-160">Jedes Eingabe Layout-Objekt wird basierend auf einer shadersignatur erstellt. Dadurch kann die API die Input-Layout-Object-Elemente anhand der Shader-Input-Signatur überprüfen, um sicherzustellen, dass eine genaue Entsprechung von Typen und Semantik vorliegt.</span><span class="sxs-lookup"><span data-stu-id="738cc-160">Each input-layout object is created based on a shader signature; this allows the API to validate the input-layout-object elements against the shader-input signature to make sure that there is an exact match of types and semantics.</span></span> <span data-ttu-id="738cc-161">Sie können ein einzelnes Eingabe Layout-Objekt für viele Shader erstellen, sofern alle Shader-Eingabe Signaturen genau übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="738cc-161">You can create a single input-layout object for many shaders, as long as all of the shader-input signatures exactly match.</span></span>

## <a name="bind-objects-to-the-input-assembler-stage"></a><span data-ttu-id="738cc-162">Binden von Objekten an die Input-Assembler-Phase</span><span class="sxs-lookup"><span data-stu-id="738cc-162">Bind Objects to the Input-Assembler Stage</span></span>

<span data-ttu-id="738cc-163">Nachdem Sie Vertex-Puffer Ressourcen und ein Eingabe Layoutobjekt erstellt haben, können Sie Sie durch Aufrufen von [**Verknüpfung id3d11devicecontext aus:: iasetvertexbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) und [**Verknüpfung id3d11devicecontext aus:: iasetinputlayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout)an die IA-Phase binden.</span><span class="sxs-lookup"><span data-stu-id="738cc-163">After you create vertex buffer resources and an input layout object, you can bind them to the IA stage by calling [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) and [**ID3D11DeviceContext::IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).</span></span> <span data-ttu-id="738cc-164">Das folgende Beispiel zeigt die Bindung eines einzelnen Scheitelpunkt Puffers und ein Eingabe Layout-Objekt an die IA-Phase:</span><span class="sxs-lookup"><span data-stu-id="738cc-164">The following example shows the binding of a single vertex buffer and an input-layout object to the IA stage:</span></span>


```
UINT stride = sizeof( SimpleVertex );
UINT offset = 0;
g_pd3dDevice->IASetVertexBuffers( 
    0,                // the first input slot for binding
    1,                // the number of buffers in the array
    &g_pVertexBuffer, // the array of vertex buffers
    &stride,          // array of stride values, one for each buffer
    &offset );        // array of offset values, one for each buffer

// Set the input layout
g_pd3dDevice->IASetInputLayout( g_pVertexLayout );
```



<span data-ttu-id="738cc-165">Die Bindung des Eingabe-Layoutobjekte erfordert nur einen Zeiger auf das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="738cc-165">Binding the input-layout object only requires a pointer to the object.</span></span>

<span data-ttu-id="738cc-166">Im vorherigen Beispiel ist ein einzelner Scheitelpunkt Puffer gebunden. mehrere Vertex-Puffer können jedoch durch einen einzelnen-Befehl an [**Verknüpfung id3d11devicecontext aus:: iasetvertexbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers)gebunden werden, und der folgende Code zeigt einen solchen Aufrufs, um drei Scheitelpunkt Puffer zu binden:</span><span class="sxs-lookup"><span data-stu-id="738cc-166">In the preceding example, a single vertex buffer is bound; however, multiple vertex buffers can be bound by a single call to [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers), and the following code shows such a call to bind three vertex buffers:</span></span>


```
UINT strides[3];
strides[0] = sizeof(SimpleVertex1);
strides[1] = sizeof(SimpleVertex2);
strides[2] = sizeof(SimpleVertex3);
UINT offsets[3] = { 0, 0, 0 };
g_pd3dDevice->IASetVertexBuffers( 
    0,                 //first input slot for binding
    3,                 //number of buffers in the array
    &g_pVertexBuffers, //array of three vertex buffers
    &strides,          //array of stride values, one for each buffer
    &offsets );        //array of offset values, one for each buffer
```



<span data-ttu-id="738cc-167">Ein Index Puffer wird durch Aufrufen von [**Verknüpfung id3d11devicecontext aus:: iasetindexbuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer)an die IA-Phase gebunden.</span><span class="sxs-lookup"><span data-stu-id="738cc-167">An index buffer is bound to the IA stage by calling [**ID3D11DeviceContext::IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).</span></span>

## <a name="specify-the-primitive-type"></a><span data-ttu-id="738cc-168">Geben Sie den primitiven Typ an.</span><span class="sxs-lookup"><span data-stu-id="738cc-168">Specify the Primitive Type</span></span>

<span data-ttu-id="738cc-169">Nachdem die Eingabepuffer gebunden wurden, muss der IA-Phase mitgeteilt werden, wie die Scheitel Punkte in primitive assembliert werden.</span><span class="sxs-lookup"><span data-stu-id="738cc-169">After the input buffers have been bound, the IA stage must be told how to assemble the vertices into primitives.</span></span> <span data-ttu-id="738cc-170">Dies erfolgt durch das Angeben des [primitiven Typs](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) durch Aufrufen von [**Verknüpfung id3d11devicecontext aus:: iasetprimitivetopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); der folgende Code ruft diese Funktion auf, um die Daten als Dreiecks Liste ohne Informationen zu definieren:</span><span class="sxs-lookup"><span data-stu-id="738cc-170">This is done by specifying the [primitive type](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) by calling [**ID3D11DeviceContext::IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); the following code calls this function to define the data as a triangle list without adjacency:</span></span>


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



<span data-ttu-id="738cc-171">Der Rest der primitiven Typen wird in [**D3D \_ primitive \_ Topologie**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="738cc-171">The rest of the primitive types are listed in [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).</span></span>

## <a name="call-draw-methods"></a><span data-ttu-id="738cc-172">Draw-Methoden aufrufen</span><span class="sxs-lookup"><span data-stu-id="738cc-172">Call Draw Methods</span></span>

<span data-ttu-id="738cc-173">Nachdem Eingabe Ressourcen an die Pipeline gebunden wurden, ruft eine Anwendung eine Draw-Methode auf, um primitive zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="738cc-173">After input resources have been bound to the pipeline, an application calls a draw method to render primitives.</span></span> <span data-ttu-id="738cc-174">Es gibt mehrere Draw-Methoden, die in der folgenden Tabelle aufgeführt sind: Einige verwenden Index Puffer, einige Instanzdaten und einige Verwendungs Daten aus der Streaming-Output-Phase als Eingabe für die Eingabe-Assembler-Phase.</span><span class="sxs-lookup"><span data-stu-id="738cc-174">There are several draw methods, which are shown in the following table; some use index buffers, some use instance data, and some reuse data from the streaming-output stage as input to the input-assembler stage.</span></span>



| <span data-ttu-id="738cc-175">Draw-Methoden</span><span class="sxs-lookup"><span data-stu-id="738cc-175">Draw Methods</span></span>                                                                                  | <span data-ttu-id="738cc-176">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="738cc-176">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="738cc-177">**Verknüpfung id3d11devicecontext aus::D RAW**</span><span class="sxs-lookup"><span data-stu-id="738cc-177">**ID3D11DeviceContext::Draw**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | <span data-ttu-id="738cc-178">Zeichnen Sie nicht indizierte, nicht instanzierte primitive.</span><span class="sxs-lookup"><span data-stu-id="738cc-178">Draw non-indexed, non-instanced primitives.</span></span>                                                            |
| [<span data-ttu-id="738cc-179">**Verknüpfung id3d11devicecontext aus::D rawinstanzierte**</span><span class="sxs-lookup"><span data-stu-id="738cc-179">**ID3D11DeviceContext::DrawInstanced**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | <span data-ttu-id="738cc-180">Zeichnen Sie nicht indizierte, instanzierte primitive.</span><span class="sxs-lookup"><span data-stu-id="738cc-180">Draw non-indexed, instanced primitives.</span></span>                                                                |
| [<span data-ttu-id="738cc-181">**Verknüpfung id3d11devicecontext aus::D rawindebug**</span><span class="sxs-lookup"><span data-stu-id="738cc-181">**ID3D11DeviceContext::DrawIndexed**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | <span data-ttu-id="738cc-182">Zeichnen Sie indizierte, nicht instanzierte primitive.</span><span class="sxs-lookup"><span data-stu-id="738cc-182">Draw indexed, non-instanced primitives.</span></span>                                                                |
| [<span data-ttu-id="738cc-183">**Verknüpfung id3d11devicecontext aus::D rawindexedinstangeleitet**</span><span class="sxs-lookup"><span data-stu-id="738cc-183">**ID3D11DeviceContext::DrawIndexedInstanced**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | <span data-ttu-id="738cc-184">Zeichnen Sie indizierte, instanzierte primitive.</span><span class="sxs-lookup"><span data-stu-id="738cc-184">Draw indexed, instanced primitives.</span></span>                                                                    |
| [<span data-ttu-id="738cc-185">**Verknüpfung id3d11devicecontext aus::D rawauto**</span><span class="sxs-lookup"><span data-stu-id="738cc-185">**ID3D11DeviceContext::DrawAuto**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | <span data-ttu-id="738cc-186">Zeichnen Sie nicht indizierte, nicht instanzierte primitive aus den Eingabedaten, die aus der Streaming-Output-Phase stammen.</span><span class="sxs-lookup"><span data-stu-id="738cc-186">Draw non-indexed, non-instanced primitives from input data that comes from the streaming-output stage.</span></span> |



 

<span data-ttu-id="738cc-187">Jede Draw-Methode rendert einen einzelnen Topologietyp.</span><span class="sxs-lookup"><span data-stu-id="738cc-187">Each draw method renders a single topology type.</span></span> <span data-ttu-id="738cc-188">Während des Renderings werden unvollständige primitive (solche ohne ausreichenden Scheitel Punkte, fehlende Indizes, partielle primitive usw.) automatisch verworfen.</span><span class="sxs-lookup"><span data-stu-id="738cc-188">During rendering, incomplete primitives (those without enough vertices, lacking indices, partial primitives, and so on) are silently discarded.</span></span>

## <a name="related-topics"></a><span data-ttu-id="738cc-189">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="738cc-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="738cc-190">Eingabe-Assembler-Phase</span><span class="sxs-lookup"><span data-stu-id="738cc-190">Input-Assembler Stage</span></span>](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 