---
title: Erstellen eines Index Puffers
description: In diesem Thema wird gezeigt, wie ein Index Puffer zur Vorbereitung des Renderings initialisiert wird.
ms.assetid: 4b33d32a-27fd-4652-87ac-3b7268881f89
keywords:
- Index Puffer, erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c4c99639748876a5f5fd84e546aaf299885c76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207077"
---
# <a name="how-to-create-an-index-buffer"></a><span data-ttu-id="01670-104">Vorgehensweise: Erstellen eines Index Puffers</span><span class="sxs-lookup"><span data-stu-id="01670-104">How to: Create an Index Buffer</span></span>

<span data-ttu-id="01670-105">[Index Puffer](overviews-direct3d-11-resources-buffers-intro.md) enthalten Indexdaten.</span><span class="sxs-lookup"><span data-stu-id="01670-105">[Index buffers](overviews-direct3d-11-resources-buffers-intro.md) contain index data.</span></span> <span data-ttu-id="01670-106">In diesem Thema wird gezeigt, wie ein [Index Puffer](overviews-direct3d-11-resources-buffers-intro.md) zur Vorbereitung des Renderings initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="01670-106">This topic shows how to initialize an [index buffer](overviews-direct3d-11-resources-buffers-intro.md) in preparation for rendering.</span></span>

<span data-ttu-id="01670-107">**So initialisieren Sie einen Index Puffer**</span><span class="sxs-lookup"><span data-stu-id="01670-107">**To initialize an index buffer**</span></span>

1.  <span data-ttu-id="01670-108">Erstellen Sie einen Puffer, der die Indexinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="01670-108">Create a buffer that contains your index information.</span></span>
2.  <span data-ttu-id="01670-109">Erstellen Sie eine Puffer Beschreibung, indem Sie eine [**D3D11- \_ Puffer- \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Debug-Struktur ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="01670-109">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="01670-110">Übergeben Sie das D3D11 \_ Bind \_ Index \_ buffer-Flag an den **bindflags** -Member, und übergeben Sie die Größe des Puffers in Bytes an den **bytewidth** -Member.</span><span class="sxs-lookup"><span data-stu-id="01670-110">Pass the D3D11\_BIND\_INDEX\_BUFFER flag to the **BindFlags** member and pass the size of the buffer in bytes to the **ByteWidth** member.</span></span>
3.  <span data-ttu-id="01670-111">Erstellen Sie eine Beschreibung der untergeordneten Quelldaten, indem Sie eine [**D3D11 \_ subresource- \_ Daten**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Struktur ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="01670-111">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="01670-112">Der **psysmem** -Member sollte direkt auf die in Schritt 1 erstellten Indexdaten verweisen.</span><span class="sxs-lookup"><span data-stu-id="01670-112">The **pSysMem** member should point directly to the index data created in step one.</span></span>
4.  <span data-ttu-id="01670-113">Aufrufen von [**ID3D11Device:: up Buffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) beim Übergeben der [**D3D11- \_ Puffer- \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Debug-Struktur, der [**D3D11 \_ subresource- \_ Daten**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Struktur und der Adresse eines Zeigers auf die [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) -Schnittstelle, die initialisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="01670-113">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="01670-114">Im folgenden Codebeispiel wird veranschaulicht, wie ein Index Puffer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="01670-114">The following code example demonstrates how to create an index buffer.</span></span> <span data-ttu-id="01670-115">In diesem Beispiel wird angenommen, dass</span><span class="sxs-lookup"><span data-stu-id="01670-115">This example assumes that</span></span>


```
g_pd3dDevice
```



<span data-ttu-id="01670-116">ist ein gültiges [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Objekt, das</span><span class="sxs-lookup"><span data-stu-id="01670-116">is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object and that</span></span>


```
g_pd3dContext
```



<span data-ttu-id="01670-117">ist ein gültiges [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="01670-117">is a valid [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>


```
ID3D11Buffer *g_pIndexBuffer = NULL;

// Create indices.
unsigned int indices[] = { 0, 1, 2 };

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage           = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
bufferDesc.BindFlags       = D3D11_BIND_INDEX_BUFFER;
bufferDesc.CPUAccessFlags  = 0;
bufferDesc.MiscFlags       = 0;

// Define the resource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = indices;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer with the device.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
if( FAILED( hr ) )
    return hr;

// Set the buffer.
g_pd3dContext->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
    
```



## <a name="related-topics"></a><span data-ttu-id="01670-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="01670-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01670-119">Puffer</span><span class="sxs-lookup"><span data-stu-id="01670-119">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="01670-120">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="01670-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




