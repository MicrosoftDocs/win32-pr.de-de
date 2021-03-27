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
# <a name="how-to-create-a-constant-buffer"></a>Vorgehensweise: Erstellen eines konstanten Puffers

[Konstante Puffer](overviews-direct3d-11-resources-buffers-intro.md) enthalten shaderkonstantendaten. In diesem Thema wird gezeigt, wie ein [konstanter Puffer](overviews-direct3d-11-resources-buffers-intro.md) zur Vorbereitung des Renderings initialisiert wird.

**So initialisieren Sie einen konstanten Puffer**

1.  Definieren Sie eine-Struktur, die die Vertex-Shader-konstantendaten beschreibt.
2.  Weisen Sie der Struktur, die Sie in Schritt 1 definiert haben, Arbeitsspeicher zu. Füllen Sie diesen Puffer mit Vertex-Shader-Konstanten Daten. Sie können " **malloc** " oder " **New** " verwenden, um den Arbeitsspeicher zuzuordnen, oder Sie können Speicherplatz für die Struktur aus dem Stapel zuweisen.
3.  Erstellen Sie eine Puffer Beschreibung, indem Sie eine [**D3D11- \_ Puffer- \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Debug-Struktur ausfüllen. Übergeben Sie das D3D11 \_ Bind \_ Constant \_ -pufferflag an den **bindflags** -Member, und übergeben Sie die Größe der Struktur der Konstanten Puffer Beschreibung in Bytes an den **bytewidth** -Member.

    > [!Note]  
    > Das D3D11 \_ Bind \_ Constant- \_ pufferflag kann nicht mit anderen Flags kombiniert werden.

     

4.  Erstellen Sie eine Beschreibung der untergeordneten Quelldaten, indem Sie eine [**D3D11 \_ subresource- \_ Daten**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Struktur ausfüllen. Der **psysmem** -Member der **D3D11 \_ subresource- \_ Daten** Struktur muss direkt auf die Vertex-Shader-konstantendaten verweisen, die Sie in Schritt 2 erstellt haben.
5.  Aufrufen von [**ID3D11Device:: up Buffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) beim Übergeben der [**D3D11- \_ Puffer- \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Debug-Struktur, der [**D3D11 \_ subresource- \_ Daten**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Struktur und der Adresse eines Zeigers auf die [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) -Schnittstelle, die initialisiert werden soll.

Diese Codebeispiele veranschaulichen, wie ein konstanter Puffer erstellt wird.

In diesem Beispiel wird davon ausgegangen, dass **g \_ pd3dDevice** ein gültiges [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Objekt ist und dass **g \_ pd3dContext** ein gültiges [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Objekt ist.


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



Dieses Beispiel zeigt die zugehörige HLSL-cBuffer-Definition.

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
> Stellen Sie sicher, dass Sie \_ mit dem HLSL-Layout das Layout des vs-Konstanten \_ Puffer Arbeitsspeichers in C++ vergleichen. Informationen dazu, wie das Layout im Arbeitsspeicher von HLSL behandelt wird, finden Sie unter [Packen von Regeln für konstante Variablen](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Puffer](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 