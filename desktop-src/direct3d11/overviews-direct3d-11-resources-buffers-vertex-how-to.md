---
title: Erstellen eines Scheitelpunktpuffers
description: In diesem Thema wird gezeigt, wie sie einen statischen Scheitelpunktpuffer initialisieren, d. h. einen Scheitelpunktpuffer, der sich nicht ändert.
ms.assetid: 584a39d1-7629-429a-b451-64b1432cb48f
keywords:
- Vertexpuffer, erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f919646dfd4e8f714b925606f342db586ff2b8f09690c58698b7dab2635159e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496900"
---
# <a name="how-to-create-a-vertex-buffer"></a>Vorgehensweise: Erstellen eines Scheitelpunktpuffers

[Scheitelpunktpuffer](overviews-direct3d-11-resources-buffers-intro.md) enthalten Daten pro Scheitelpunkt. In diesem Thema wird gezeigt, wie Sie einen statischen [Scheitelpunktpuffer](overviews-direct3d-11-resources-buffers-intro.md)initialisieren, d. h. einen Scheitelpunktpuffer, der sich nicht ändert. Hilfe beim Initialisieren eines nicht statischen Puffers finden Sie im Abschnitt ["Hinweise".](#remarks)

**So initialisieren Sie einen statischen Scheitelpunktpuffer**

1.  Definieren Sie eine -Struktur, die einen Scheitelpunkt beschreibt. Wenn Ihre Scheitelpunktdaten beispielsweise Positionsdaten und Farbdaten enthalten, verfügt Ihre Struktur über einen Vektor, der die Position beschreibt, und einen anderen, der die Farbe beschreibt.
2.  Belegen Sie Arbeitsspeicher (mit malloc oder new) für die Struktur, die Sie in Schritt 1 definiert haben. Füllen Sie diesen Puffer mit den tatsächlichen Scheitelpunktdaten, die Ihre Geometrie beschreiben.
3.  Erstellen Sie eine Pufferbeschreibung, indem Sie eine [**D3D11 \_ BUFFER \_ DESC-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) ausfüllen. Übergeben Sie das BIND VERTEX BUFFER-Flag D3D11 \_ \_ an den \_ **BindFlags-Member,** und übergeben Sie die Größe der Struktur aus Schritt 1 an den **ByteWidth-Member.**
4.  Erstellen Sie eine Beschreibung der Unterressourcendaten, indem Sie eine [**D3D11 \_ SUBRESOURCE \_ DATA-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) ausfüllen. Das **pSysMem-Element** der [**D3D11 \_ SUBRESOURCE \_ DATA-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) sollte direkt auf die in Schritt 2 erstellten Ressourcendaten verweisen.
5.  Rufen Sie [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) auf, während Sie die [**D3D11 \_ BUFFER \_ DESC-Struktur,**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) die [**D3D11 \_ SUBRESOURCE \_ DATA-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) und die Adresse eines Zeigers auf die zu initialisierende [**ID3D11Buffer-Schnittstelle**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) übergeben.

Im folgenden Codebeispiel wird veranschaulicht, wie ein Scheitelpunktpuffer erstellt wird. In diesem Beispiel wird davon ausgegangen, dass **g \_ pd3dDevice** ein gültiges [**ID3D11Device-Objekt**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) ist.


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



## <a name="remarks"></a>Hinweise

Im Folgenden finden Sie einige Möglichkeiten zum Initialisieren eines Scheitelpunktpuffers, der sich im Laufe der Zeit ändert.

1.  Erstellen Sie einen zweiten Puffer mit [**D3D11 \_ USAGE \_ STAGING.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)Füllen Sie den zweiten Puffer mit [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)aus. Verwenden Sie [**ID3D11DeviceContext::CopyResource,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) um aus dem Stagingpuffer in den Standardpuffer zu kopieren.
2.  Verwenden Sie [**ID3D11DeviceContext::UpdateSubresource,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) um Daten aus dem Arbeitsspeicher zu kopieren.
3.  Erstellen Sie einen Puffer mit [**D3D11 \_ USAGE \_ DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), und füllen Sie ihn mit [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) aus (mit den Flags Discard und NoOverwrite entsprechend).

\#1 und \# 2 sind nützlich für Inhalte, die sich weniger als einmal pro Frame ändern. Im Allgemeinen sind GPU-Lesefunktionen schnell, und CPU-Updates sind langsamer.

\#3 ist nützlich für Inhalte, die sich mehr als einmal pro Frame ändern. Im Allgemeinen sind GPU-Lesefunktionen langsamer, CPU-Updates sind jedoch schneller.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Puffer](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Verwenden von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




