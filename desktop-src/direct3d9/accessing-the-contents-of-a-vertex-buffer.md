---
description: Vertex-Puffer Objekte ermöglichen Anwendungen den direkten Zugriff auf den für Scheitelpunkt Daten zugewiesenen Arbeitsspeicher.
ms.assetid: 63d255b7-fa7d-411b-9cdb-52113f30c933
title: Zugreifen auf den Inhalt eines Scheitelpunkt Puffers (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1b5e4a4986e064d3736f83567f5dd6d479d0dbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346439"
---
# <a name="accessing-the-contents-of-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="5f6dd-103">Zugreifen auf den Inhalt eines Scheitelpunkt Puffers (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5f6dd-103">Accessing the Contents of a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="5f6dd-104">Vertex-Puffer Objekte ermöglichen Anwendungen den direkten Zugriff auf den für Scheitelpunkt Daten zugewiesenen Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-104">Vertex buffer objects enable applications to directly access the memory allocated for vertex data.</span></span> <span data-ttu-id="5f6dd-105">Sie können einen Zeiger auf den Vertex-Pufferspeicher abrufen, indem Sie die [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) -Methode aufrufen und dann nach Bedarf auf den Speicher zugreifen, um den Puffer mit neuen Scheitelpunkt Daten zu füllen oder um bereits enthaltene Daten zu lesen.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-105">You can retrieve a pointer to vertex buffer memory by calling the [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) method, and then accessing the memory as needed to fill the buffer with new vertex data or to read any data it already contains.</span></span> <span data-ttu-id="5f6dd-106">Die **IDirect3DVertexBuffer9:: Lock** -Methode akzeptiert vier Parameter.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-106">The **IDirect3DVertexBuffer9::Lock** method accepts four parameters.</span></span> <span data-ttu-id="5f6dd-107">Der erste, *offsetToLock*, ist der Offset in den Scheitelpunkt Daten.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-107">The first, *OffsetToLock*, is the offset into the vertex data.</span></span> <span data-ttu-id="5f6dd-108">Der zweite Parameter ist die Größe der Scheitelpunkt Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-108">The second parameter is the size, measured in bytes, of the vertex data.</span></span> <span data-ttu-id="5f6dd-109">Der dritte akzeptierte Parameter ist die Adresse eines Zeigers, der auf die Scheitelpunkt Daten zeigt, wenn der-Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-109">The third parameter accepted is the address of a pointer that points to the vertex data, if the call succeeds.</span></span>

<span data-ttu-id="5f6dd-110">Der letzte Parameter, *Flags*, teilt dem System mit, wie der Arbeitsspeicher gesperrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-110">The last parameter, *Flags*, tells the system how the memory should be locked.</span></span> <span data-ttu-id="5f6dd-111">Geben Sie Konstanten für den *Flags* -Parameter entsprechend der Art und Weise an, wie auf die Vertex-Daten zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-111">Specify constants for the *Flags* parameter according to the way the vertex data will be accessed.</span></span> <span data-ttu-id="5f6dd-112">Stellen Sie sicher, dass der für [**D3DUSAGE**](d3dusage.md) gewählte Wert mit dem für [D3DLOCK](d3dlock.md)ausgewählten Wert übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-112">Make sure the value chosen for [**D3DUSAGE**](d3dusage.md) matches the value chosen for [D3DLOCK](d3dlock.md).</span></span> <span data-ttu-id="5f6dd-113">Wenn Sie z. b. einen Vertex-Puffer nur mit Schreibzugriff erstellen, ist es nicht sinnvoll, die Daten zu lesen, indem Sie D3DLOCK Read \_ only angeben.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-113">For example, if you are creating a vertex buffer with write access only, it doesn't make sense to try to read the data by specifying D3DLOCK\_READONLY.</span></span> <span data-ttu-id="5f6dd-114">Durch die Verwendung dieser Flags kann der Treiber den Speicher sperren und die beste Leistung bereitstellen, wenn der angeforderte Zugriffstyp vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-114">Wisely using these flags allows the driver to lock the memory and provide the best performance, given the requested access type.</span></span>

<span data-ttu-id="5f6dd-115">Nachdem Sie das Ausfüllen oder Lesen der Scheitelpunkt Daten abgeschlossen haben, können Sie die [**IDirect3DVertexBuffer9:: Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) -Methode wie im folgenden Codebeispiel gezeigt abrufen.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-115">After you finish filling or reading the vertex data, call the [**IDirect3DVertexBuffer9::Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) method, as shown in the following code example.</span></span>


```
// This code example assumes the g_pVB is a variable of type 
//   LPDIRECT3DVERTEXBUFFER9 and that g_Vertices has been  
//   properly initialized with vertices

// Lock the buffer to gain access to the vertices 
VOID* pVertices;

if(FAILED(g_pVB->Lock(0, sizeof(g_Vertices), 
        (BYTE**)&pVertices, 0 ) ) ) 
    return E_FAIL;

memcpy(pVertices, g_Vertices, sizeof(g_Vertices));
g_pVB->Unlock();
```



<span data-ttu-id="5f6dd-116">Wenn Sie einen Vertex-Puffer mit dem \_ Flag D3DUSAGE Write only erstellen, verwenden Sie nicht das Sperr Kennzeichen D3DLOCK Read \_ only.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-116">If you create a vertex buffer with the D3DUSAGE\_WRITEONLY flag, do not use the D3DLOCK\_READONLY locking flag.</span></span> <span data-ttu-id="5f6dd-117">Verwenden Sie das D3DLOCK-Flag "schreibgeschützt", \_ Wenn die Anwendung nur aus dem Vertex-Pufferspeicher gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-117">Use the D3DLOCK\_READONLY flag if your application will read only from the vertex buffer memory.</span></span> <span data-ttu-id="5f6dd-118">Das Einschließen dieses Flags ermöglicht Direct3D, seine internen Prozeduren zu optimieren, um die Effizienz zu verbessern, da der Zugriff auf den Arbeitsspeicher schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-118">Including this flag enables Direct3D to optimize its internal procedures to improve efficiency, given that access to the memory will be read-only.</span></span>

<span data-ttu-id="5f6dd-119">Weitere [](performance-optimizations.md) Informationen zur Verwendung \_ von D3DLOCK DISCARD oder D3DLOCK \_ noüberschreitungen für den flags-Parameter von [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)finden Sie unter Verwenden von dynamischen Scheitelpunkt-und Index Puffern.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-119">See [Using Dynamic Vertex and Index Buffers](performance-optimizations.md) for information about using D3DLOCK\_DISCARD or D3DLOCK\_NOOVERWRITE for the Flags parameter of [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock).</span></span>

<span data-ttu-id="5f6dd-120">Stellen Sie in C++ sicher, dass die Anwendung ordnungsgemäß auf den zugeordneten Speicher zugreift, da Sie direkt auf den für den Vertex-Puffer reservierten Arbeitsspeicher zugreifen.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-120">In C++, because you directly access the memory allocated for the vertex buffer, make sure your application properly accesses the allocated memory.</span></span> <span data-ttu-id="5f6dd-121">Andernfalls riskieren Sie, dass der Arbeitsspeicher ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-121">Otherwise, you risk rendering that memory invalid.</span></span> <span data-ttu-id="5f6dd-122">Verwenden Sie den Schritt des Vertex-Formats, das Ihre Anwendung verwendet, um von einem Scheitelpunkt im zugewiesenen Puffer zu einem anderen zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-122">Use the stride of the vertex format that your application uses to move from one vertex in the allocated buffer to another.</span></span> <span data-ttu-id="5f6dd-123">Der Vertex-Pufferspeicher ist ein einfaches Array von Vertices, das in "f" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-123">The vertex buffer memory is a simple array of vertices specified in FVF.</span></span> <span data-ttu-id="5f6dd-124">Verwenden Sie den Schritt der von Ihnen definierten Scheitelpunkt Format Struktur.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-124">Use the stride of whatever vertex format structure you define.</span></span> <span data-ttu-id="5f6dd-125">Sie können den Schritt jedes Scheitel Punkts zur Laufzeit berechnen, indem Sie die in der Vertex-Puffer Beschreibung enthaltene [D3DFVF](d3dfvf.md) untersuchen.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-125">You can calculate the stride of each vertex at run time by examining the [D3DFVF](d3dfvf.md) contained in the vertex buffer description.</span></span> <span data-ttu-id="5f6dd-126">In der folgenden Tabelle wird die Größe der einzelnen Scheitelpunkt Komponenten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-126">The following table shows the size for each vertex component.</span></span>



| <span data-ttu-id="5f6dd-127">Vertex-formatflag</span><span class="sxs-lookup"><span data-stu-id="5f6dd-127">Vertex Format Flag</span></span> | <span data-ttu-id="5f6dd-128">Size</span><span class="sxs-lookup"><span data-stu-id="5f6dd-128">Size</span></span>              |
|--------------------|-------------------|
| <span data-ttu-id="5f6dd-129">D3DFVF \_ diffuses</span><span class="sxs-lookup"><span data-stu-id="5f6dd-129">D3DFVF\_DIFFUSE</span></span>    | <span data-ttu-id="5f6dd-130">sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="5f6dd-130">sizeof(DWORD)</span></span>     |
| <span data-ttu-id="5f6dd-131">D3DFVF \_ Normal</span><span class="sxs-lookup"><span data-stu-id="5f6dd-131">D3DFVF\_NORMAL</span></span>     | <span data-ttu-id="5f6dd-132">sizeof (float) x 3</span><span class="sxs-lookup"><span data-stu-id="5f6dd-132">sizeof(float) x 3</span></span> |
| <span data-ttu-id="5f6dd-133">D3DFVF \_ Glanz</span><span class="sxs-lookup"><span data-stu-id="5f6dd-133">D3DFVF\_SPECULAR</span></span>   | <span data-ttu-id="5f6dd-134">sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="5f6dd-134">sizeof(DWORD)</span></span>     |
| <span data-ttu-id="5f6dd-135">D3DFVF \_ texn</span><span class="sxs-lookup"><span data-stu-id="5f6dd-135">D3DFVF\_TEXn</span></span>       | <span data-ttu-id="5f6dd-136">sizeof (float) x n</span><span class="sxs-lookup"><span data-stu-id="5f6dd-136">sizeof(float) x n</span></span> |
| <span data-ttu-id="5f6dd-137">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="5f6dd-137">D3DFVF\_XYZ</span></span>        | <span data-ttu-id="5f6dd-138">sizeof (float) x 3</span><span class="sxs-lookup"><span data-stu-id="5f6dd-138">sizeof(float) x 3</span></span> |
| <span data-ttu-id="5f6dd-139">D3DFVF \_ xyzrhw</span><span class="sxs-lookup"><span data-stu-id="5f6dd-139">D3DFVF\_XYZRHW</span></span>     | <span data-ttu-id="5f6dd-140">sizeof (float) x 4</span><span class="sxs-lookup"><span data-stu-id="5f6dd-140">sizeof(float) x 4</span></span> |



 

<span data-ttu-id="5f6dd-141">Die Anzahl der im Vertex-Format vorhandenen Texturkoordinaten wird durch die D3DFVF \_ tex n-Flags beschrieben (wobei n für einen Wert zwischen 0 und 8 steht).</span><span class="sxs-lookup"><span data-stu-id="5f6dd-141">The number of texture coordinates present in the vertex format is described by the D3DFVF\_TEX n flags (where n is a value from 0 to 8).</span></span> <span data-ttu-id="5f6dd-142">Multiplizieren Sie die Anzahl der Texturkoordinaten Sätze um die Größe eines Satzes von Texturkoordinaten, der von einem bis vier Gleit Komma Zahlen reichen kann, um den für diese Anzahl von Texturkoordinaten erforderlichen Arbeitsspeicher zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-142">Multiply the number of texture coordinate sets by the size of one set of texture coordinates, which can range from one to four floats, to calculate the memory required for that number of texture coordinates.</span></span>

<span data-ttu-id="5f6dd-143">Verwenden Sie den gesamten vertexstride, um den Speicher Zeiger nach Bedarf zu erhöhen und zu verringern, um auf bestimmte Scheitel Punkte zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-143">Use the total vertex stride to increment and decrement the memory pointer as needed to access particular vertices.</span></span>

## <a name="retrieving-vertex-buffer-descriptions"></a><span data-ttu-id="5f6dd-144">Abrufen von Vertex-Puffer Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5f6dd-144">Retrieving Vertex Buffer Descriptions</span></span>

<span data-ttu-id="5f6dd-145">Sie können Informationen zu einem Vertex-Puffer abrufen, indem Sie die [**IDirect3DVertexBuffer9:: getdesc**](/windows/desktop/api) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-145">You can retrieve information about a vertex buffer by calling the [**IDirect3DVertexBuffer9::GetDesc**](/windows/desktop/api) method.</span></span> <span data-ttu-id="5f6dd-146">Diese Methode füllt die Member der [**D3DVERTEXBUFFER \_ DESC**](d3dvertexbuffer-desc.md) -Struktur mit Informationen über den Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="5f6dd-146">This method fills the members of the [**D3DVERTEXBUFFER\_DESC**](d3dvertexbuffer-desc.md) structure with information about the vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f6dd-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5f6dd-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f6dd-148">Vertex-Puffer</span><span class="sxs-lookup"><span data-stu-id="5f6dd-148">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
