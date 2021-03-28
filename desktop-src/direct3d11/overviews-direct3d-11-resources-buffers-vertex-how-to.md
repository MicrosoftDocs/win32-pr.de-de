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
# <a name="how-to-create-a-vertex-buffer"></a>Vorgehensweise: Erstellen eines Scheitelpunkt Puffers

[Vertex-Puffer](overviews-direct3d-11-resources-buffers-intro.md) enthalten pro Scheitelpunkt Daten. In diesem Thema wird gezeigt, wie ein statischer [Vertex-Puffer](overviews-direct3d-11-resources-buffers-intro.md), d. h. ein Vertex-Puffer, der nicht geändert wird, initialisiert wird. Hilfe zur Initialisierung eines nicht statischen Puffers finden Sie im Abschnitt " [Hinweise](#remarks) ".

**So initialisieren Sie einen statischen Scheitelpunkt Puffer**

1.  Definieren Sie eine-Struktur, die einen Scheitelpunkt beschreibt. Wenn Ihre Scheitelpunkt Daten z. b. Positionsdaten und Farbdaten enthalten, würde die Struktur einen Vektor aufweisen, der die Position und eine andere beschreibt, die die Farbe beschreibt.
2.  Weisen Sie Arbeitsspeicher (mithilfe von malloc oder New) für die Struktur zu, die Sie in Schritt 1 definiert haben. Füllen Sie diesen Puffer mit den tatsächlichen Scheitelpunkt Daten, die ihre Geometrie beschreiben.
3.  Erstellen Sie eine Puffer Beschreibung, indem Sie eine [**D3D11- \_ Puffer- \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Debug-Struktur ausfüllen. Übergeben Sie das D3D11 \_ Bind \_ -Vertex \_ -pufferflag an den **bindflags** -Member, und übergeben Sie die Größe der Struktur von Schritt 1 an den **bytewidth** -Member.
4.  Erstellen Sie eine Beschreibung der untergeordneten Quelldaten, indem Sie eine [**D3D11 \_ subresource- \_ Daten**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Struktur ausfüllen. Der **psysmem** -Member der [**D3D11 \_ subresource- \_ Daten**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Struktur sollte direkt auf die in Schritt 2 erstellten Ressourcen Daten verweisen.
5.  Aufrufen von [**ID3D11Device:: up Buffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) beim Übergeben der [**D3D11- \_ Puffer- \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Debug-Struktur, der [**D3D11 \_ subresource- \_ Daten**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Struktur und der Adresse eines Zeigers auf die [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) -Schnittstelle, die initialisiert werden soll.

Im folgenden Codebeispiel wird veranschaulicht, wie ein Scheitelpunkt Puffer erstellt wird. In diesem Beispiel wird davon ausgegangen, dass **g \_ pd3dDevice** ein gültiges [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Objekt ist.


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



## <a name="remarks"></a>Bemerkungen

Hier finden Sie einige Möglichkeiten zum Initialisieren eines Scheitelpunkt Puffers, der sich im Laufe der Zeit ändert.

1.  Erstellen Sie einen 2. Puffer [**mit D3D11 \_ Usage \_ Staging**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). füllen Sie den zweiten Puffer mit [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**Verknüpfung id3d11devicecontext aus:: unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); verwenden Sie [**Verknüpfung id3d11devicecontext aus:: copyresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) , um aus dem stagingpuffer in den Standard Puffer zu kopieren.
2.  Verwenden Sie [**Verknüpfung id3d11devicecontext aus:: updatesubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) zum Kopieren von Daten aus dem Arbeitsspeicher.
3.  Erstellen Sie einen Puffer [**mit \_ \_ dynamischem "D3D11 Usage**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)", und füllen Sie ihn mit " [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)", " [**Verknüpfung id3d11devicecontext aus:: unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) " (mit den verwerfen-und noüberschreibungsflags).

\#1 und \# 2 sind nützlich für Inhalt, der sich weniger als einmal pro Frame ändert. Im Allgemeinen werden GPU-Lesevorgänge schnell und CPU-Updates langsamer.

\#3 ist nützlich für Inhalte, die sich mehrmals pro Frame ändern. Im Allgemeinen werden GPU-Lesevorgänge langsamer, CPU-Aktualisierungen werden jedoch schneller ausgeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Puffer](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




