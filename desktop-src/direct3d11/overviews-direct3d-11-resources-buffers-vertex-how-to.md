---
title: Erstellen eines Scheitelpunkt Puffers
description: In diesem Thema wird gezeigt, wie ein statischer Vertex-Puffer, d. h. ein Vertex-Puffer, der nicht geändert wird, initialisiert wird.
ms.assetid: 584a39d1-7629-429a-b451-64b1432cb48f
keywords:
- Vertex-Puffer, erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e0b3d9d8f731b01e7c919105c21c8d150f864a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310436"
---
# <a name="how-to-create-a-vertex-buffer"></a><span data-ttu-id="ca9ee-104">Vorgehensweise: Erstellen eines Scheitelpunkt Puffers</span><span class="sxs-lookup"><span data-stu-id="ca9ee-104">How to: Create a Vertex Buffer</span></span>

<span data-ttu-id="ca9ee-105">[Vertex-Puffer](overviews-direct3d-11-resources-buffers-intro.md) enthalten pro Scheitelpunkt Daten.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-105">[Vertex buffers](overviews-direct3d-11-resources-buffers-intro.md) contain per vertex data.</span></span> <span data-ttu-id="ca9ee-106">In diesem Thema wird gezeigt, wie ein statischer [Vertex-Puffer](overviews-direct3d-11-resources-buffers-intro.md), d. h. ein Vertex-Puffer, der nicht geändert wird, initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-106">This topic shows how to initialize a static [vertex buffer](overviews-direct3d-11-resources-buffers-intro.md), that is, a vertex buffer that does not change.</span></span> <span data-ttu-id="ca9ee-107">Hilfe zur Initialisierung eines nicht statischen Puffers finden Sie im Abschnitt " [Hinweise](#remarks) ".</span><span class="sxs-lookup"><span data-stu-id="ca9ee-107">For help initializing a non-static buffer, see the [remarks](#remarks) section.</span></span>

<span data-ttu-id="ca9ee-108">**So initialisieren Sie einen statischen Scheitelpunkt Puffer**</span><span class="sxs-lookup"><span data-stu-id="ca9ee-108">**To initialize a static vertex buffer**</span></span>

1.  <span data-ttu-id="ca9ee-109">Definieren Sie eine-Struktur, die einen Scheitelpunkt beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-109">Define a structure that describes a vertex.</span></span> <span data-ttu-id="ca9ee-110">Wenn Ihre Scheitelpunkt Daten z. b. Positionsdaten und Farbdaten enthalten, würde die Struktur einen Vektor aufweisen, der die Position und eine andere beschreibt, die die Farbe beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-110">For example, if your vertex data contains position data and color data, your structure would have one vector that describes the position and another that describes the color.</span></span>
2.  <span data-ttu-id="ca9ee-111">Weisen Sie Arbeitsspeicher (mithilfe von malloc oder New) für die Struktur zu, die Sie in Schritt 1 definiert haben.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-111">Allocate memory (using malloc or new) for the structure that you defined in step one.</span></span> <span data-ttu-id="ca9ee-112">Füllen Sie diesen Puffer mit den tatsächlichen Scheitelpunkt Daten, die ihre Geometrie beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-112">Fill this buffer with the actual vertex data that describes your geometry.</span></span>
3.  <span data-ttu-id="ca9ee-113">Erstellen Sie eine Puffer Beschreibung, indem Sie eine [**D3D11- \_ Puffer- \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Debug-Struktur ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-113">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="ca9ee-114">Übergeben Sie das D3D11 \_ Bind \_ -Vertex \_ -pufferflag an den **bindflags** -Member, und übergeben Sie die Größe der Struktur von Schritt 1 an den **bytewidth** -Member.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-114">Pass the D3D11\_BIND\_VERTEX\_BUFFER flag to the **BindFlags** member and pass the size of the structure from step one to the **ByteWidth** member.</span></span>
4.  <span data-ttu-id="ca9ee-115">Erstellen Sie eine Beschreibung der untergeordneten Quelldaten, indem Sie eine [**D3D11 \_ subresource- \_ Daten**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Struktur ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-115">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="ca9ee-116">Der **psysmem** -Member der [**D3D11 \_ subresource- \_ Daten**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Struktur sollte direkt auf die in Schritt 2 erstellten Ressourcen Daten verweisen.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-116">The **pSysMem** member of the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure should point directly to the resource data created in step two.</span></span>
5.  <span data-ttu-id="ca9ee-117">Aufrufen von [**ID3D11Device:: up Buffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) beim Übergeben der [**D3D11- \_ Puffer- \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Debug-Struktur, der [**D3D11 \_ subresource- \_ Daten**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Struktur und der Adresse eines Zeigers auf die [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) -Schnittstelle, die initialisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-117">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="ca9ee-118">Im folgenden Codebeispiel wird veranschaulicht, wie ein Scheitelpunkt Puffer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-118">The following code example demonstrates how to create a vertex buffer.</span></span> <span data-ttu-id="ca9ee-119">In diesem Beispiel wird davon ausgegangen, dass **g \_ pd3dDevice** ein gültiges [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-119">This example assumes that **g\_pd3dDevice** is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object.</span></span>


```
ID3D11Buffer*      g_pVertexBuffer;

// Define the data-type that
// describes a vertex.
struct SimpleVertexCombined
{
    XMFLOAT3 Pos;  
    XMFLOAT3 Col;  
};

// Supply the actual vertex data.
SimpleVertexCombined verticesCombo[] =
{
    XMFLOAT3( 0.0f, 0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.0f, 0.5f ),
    XMFLOAT3( 0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.5f, 0.0f, 0.0f ),
    XMFLOAT3( -0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.5f, 0.0f ),
};

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage            = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
bufferDesc.BindFlags        = D3D11_BIND_VERTEX_BUFFER;
bufferDesc.CPUAccessFlags   = 0;
bufferDesc.MiscFlags        = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = verticesCombo;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the vertex buffer.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer );
    
```



## <a name="remarks"></a><span data-ttu-id="ca9ee-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca9ee-120">Remarks</span></span>

<span data-ttu-id="ca9ee-121">Hier finden Sie einige Möglichkeiten zum Initialisieren eines Scheitelpunkt Puffers, der sich im Laufe der Zeit ändert.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-121">Here are some ways to initialize a vertex buffer that changes over time.</span></span>

1.  <span data-ttu-id="ca9ee-122">Erstellen Sie einen 2. Puffer [**mit D3D11 \_ Usage \_ Staging**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). füllen Sie den zweiten Puffer mit [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**Verknüpfung id3d11devicecontext aus:: unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); verwenden Sie [**Verknüpfung id3d11devicecontext aus:: copyresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) , um aus dem stagingpuffer in den Standard Puffer zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-122">Create a 2nd buffer with [**D3D11\_USAGE\_STAGING**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage); fill the second buffer using [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); use [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) to copy from the staging buffer to the default buffer.</span></span>
2.  <span data-ttu-id="ca9ee-123">Verwenden Sie [**Verknüpfung id3d11devicecontext aus:: updatesubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) zum Kopieren von Daten aus dem Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-123">Use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) to copy data from memory.</span></span>
3.  <span data-ttu-id="ca9ee-124">Erstellen Sie einen Puffer [**mit \_ \_ dynamischem "D3D11 Usage**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)", und füllen Sie ihn mit " [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)", " [**Verknüpfung id3d11devicecontext aus:: unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) " (mit den verwerfen-und noüberschreibungsflags).</span><span class="sxs-lookup"><span data-stu-id="ca9ee-124">Create a buffer with [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), and fill it with [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) (using the Discard and NoOverwrite flags appropriately).</span></span>

<span data-ttu-id="ca9ee-125">\#1 und \# 2 sind nützlich für Inhalt, der sich weniger als einmal pro Frame ändert.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-125">\#1 and \#2 are useful for content that changes less than once per frame.</span></span> <span data-ttu-id="ca9ee-126">Im Allgemeinen werden GPU-Lesevorgänge schnell und CPU-Updates langsamer.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-126">In general, GPU reads will be fast and CPU updates will be slower.</span></span>

<span data-ttu-id="ca9ee-127">\#3 ist nützlich für Inhalte, die sich mehrmals pro Frame ändern.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-127">\#3 is useful for content that changes more than once per frame.</span></span> <span data-ttu-id="ca9ee-128">Im Allgemeinen werden GPU-Lesevorgänge langsamer, CPU-Aktualisierungen werden jedoch schneller ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca9ee-128">In general, GPU reads will be slower, but CPU updates will be faster.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca9ee-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ca9ee-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca9ee-130">Puffer</span><span class="sxs-lookup"><span data-stu-id="ca9ee-130">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="ca9ee-131">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ca9ee-131">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




