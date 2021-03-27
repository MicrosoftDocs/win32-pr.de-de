---
title: Erstellen eines konstanten Puffers
description: In diesem Thema wird gezeigt, wie ein konstanter Puffer zur Vorbereitung des Renderings initialisiert wird.
ms.assetid: 78694ac2-e850-402d-8c99-6afb0bd5d660
keywords:
- konstanter Puffer, erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1abb6718ad223ff389aa0b7ebf10ad1ec8bacd71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729561"
---
# <a name="how-to-create-a-constant-buffer"></a><span data-ttu-id="a53b8-104">Vorgehensweise: Erstellen eines konstanten Puffers</span><span class="sxs-lookup"><span data-stu-id="a53b8-104">How to: Create a Constant Buffer</span></span>

<span data-ttu-id="a53b8-105">[Konstante Puffer](overviews-direct3d-11-resources-buffers-intro.md) enthalten shaderkonstantendaten.</span><span class="sxs-lookup"><span data-stu-id="a53b8-105">[Constant buffers](overviews-direct3d-11-resources-buffers-intro.md) contain shader constant data.</span></span> <span data-ttu-id="a53b8-106">In diesem Thema wird gezeigt, wie ein [konstanter Puffer](overviews-direct3d-11-resources-buffers-intro.md) zur Vorbereitung des Renderings initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a53b8-106">This topic shows how to initialize a [constant buffer](overviews-direct3d-11-resources-buffers-intro.md) in preparation for rendering.</span></span>

<span data-ttu-id="a53b8-107">**So initialisieren Sie einen konstanten Puffer**</span><span class="sxs-lookup"><span data-stu-id="a53b8-107">**To initialize a constant buffer**</span></span>

1.  <span data-ttu-id="a53b8-108">Definieren Sie eine-Struktur, die die Vertex-Shader-konstantendaten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a53b8-108">Define a structure that describes the vertex shader constant data.</span></span>
2.  <span data-ttu-id="a53b8-109">Weisen Sie der Struktur, die Sie in Schritt 1 definiert haben, Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="a53b8-109">Allocate memory for the structure that you defined in step one.</span></span> <span data-ttu-id="a53b8-110">Füllen Sie diesen Puffer mit Vertex-Shader-Konstanten Daten.</span><span class="sxs-lookup"><span data-stu-id="a53b8-110">Fill this buffer with vertex shader constant data.</span></span> <span data-ttu-id="a53b8-111">Sie können " **malloc** " oder " **New** " verwenden, um den Arbeitsspeicher zuzuordnen, oder Sie können Speicherplatz für die Struktur aus dem Stapel zuweisen.</span><span class="sxs-lookup"><span data-stu-id="a53b8-111">You can use **malloc** or **new** to allocate the memory, or you can allocate memory for the structure from the stack.</span></span>
3.  <span data-ttu-id="a53b8-112">Erstellen Sie eine Puffer Beschreibung, indem Sie eine [**D3D11- \_ Puffer- \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Debug-Struktur ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="a53b8-112">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="a53b8-113">Übergeben Sie das D3D11 \_ Bind \_ Constant \_ -pufferflag an den **bindflags** -Member, und übergeben Sie die Größe der Struktur der Konstanten Puffer Beschreibung in Bytes an den **bytewidth** -Member.</span><span class="sxs-lookup"><span data-stu-id="a53b8-113">Pass the D3D11\_BIND\_CONSTANT\_BUFFER flag to the **BindFlags** member and pass the size of the constant buffer description structure in bytes to the **ByteWidth** member.</span></span>

    > [!Note]  
    > <span data-ttu-id="a53b8-114">Das D3D11 \_ Bind \_ Constant- \_ pufferflag kann nicht mit anderen Flags kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="a53b8-114">The D3D11\_BIND\_CONSTANT\_BUFFER flag cannot be combined with any other flags.</span></span>

     

4.  <span data-ttu-id="a53b8-115">Erstellen Sie eine Beschreibung der untergeordneten Quelldaten, indem Sie eine [**D3D11 \_ subresource- \_ Daten**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Struktur ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="a53b8-115">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="a53b8-116">Der **psysmem** -Member der **D3D11 \_ subresource- \_ Daten** Struktur muss direkt auf die Vertex-Shader-konstantendaten verweisen, die Sie in Schritt 2 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="a53b8-116">The **pSysMem** member of the **D3D11\_SUBRESOURCE\_DATA** structure must point directly to the vertex shader constant data that you created in step two.</span></span>
5.  <span data-ttu-id="a53b8-117">Aufrufen von [**ID3D11Device:: up Buffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) beim Übergeben der [**D3D11- \_ Puffer- \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Debug-Struktur, der [**D3D11 \_ subresource- \_ Daten**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Struktur und der Adresse eines Zeigers auf die [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) -Schnittstelle, die initialisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a53b8-117">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="a53b8-118">Diese Codebeispiele veranschaulichen, wie ein konstanter Puffer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a53b8-118">These code examples demonstrate how to create a constant buffer.</span></span>

<span data-ttu-id="a53b8-119">In diesem Beispiel wird davon ausgegangen, dass **g \_ pd3dDevice** ein gültiges [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Objekt ist und dass **g \_ pd3dContext** ein gültiges [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="a53b8-119">This example assumes that **g\_pd3dDevice** is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object and that **g\_pd3dContext** is a valid [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>


```C++
ID3D11Buffer*   g_pConstantBuffer11 = NULL;

// Define the constant data used to communicate with shaders.
struct VS_CONSTANT_BUFFER
{
    XMFLOAT4X4 mWorldViewProj;                              
    XMFLOAT4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                                            
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
} VS_CONSTANT_BUFFER;

// Supply the vertex shader constant data.
VS_CONSTANT_BUFFER VsConstData;
VsConstData.mWorldViewProj = {...};
VsConstData.vSomeVectorThatMayBeNeededByASpecificShader = XMFLOAT4(1,2,3,4);
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader = 3.0f;
VsConstData.fTime = 1.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader2 = 2.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader3 = 4.0f;

// Fill in a buffer description.
D3D11_BUFFER_DESC cbDesc;
cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
cbDesc.Usage = D3D11_USAGE_DYNAMIC;
cbDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;
cbDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
cbDesc.MiscFlags = 0;
cbDesc.StructureByteStride = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = &VsConstData;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer.
hr = g_pd3dDevice->CreateBuffer( &cbDesc, &InitData, 
                                 &g_pConstantBuffer11 );

if( FAILED( hr ) )
   return hr;

// Set the buffer.
g_pd3dContext->VSSetConstantBuffers( 0, 1, &g_pConstantBuffer11 );
    
```



<span data-ttu-id="a53b8-120">Dieses Beispiel zeigt die zugehörige HLSL-cBuffer-Definition.</span><span class="sxs-lookup"><span data-stu-id="a53b8-120">This example shows the associated HLSL cbuffer definition.</span></span>

``` syntax
cbuffer VS_CONSTANT_BUFFER : register(b0)
{
    matrix mWorldViewProj;
    float4  vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};
```

> [!Note]  
> <span data-ttu-id="a53b8-121">Stellen Sie sicher, dass Sie \_ mit dem HLSL-Layout das Layout des vs-Konstanten \_ Puffer Arbeitsspeichers in C++ vergleichen.</span><span class="sxs-lookup"><span data-stu-id="a53b8-121">Make sure to match the VS\_CONSTANT\_BUFFER memory layout in C++ with the HLSL layout.</span></span> <span data-ttu-id="a53b8-122">Informationen dazu, wie das Layout im Arbeitsspeicher von HLSL behandelt wird, finden Sie unter [Packen von Regeln für konstante Variablen](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span><span class="sxs-lookup"><span data-stu-id="a53b8-122">For info about how HLSL handles layout in memory, see [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a53b8-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a53b8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a53b8-124">Puffer</span><span class="sxs-lookup"><span data-stu-id="a53b8-124">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="a53b8-125">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="a53b8-125">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 