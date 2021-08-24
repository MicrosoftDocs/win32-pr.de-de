---
title: Verwenden dynamischer Ressourcen
description: Sie erstellen und verwenden dynamische Ressourcen, wenn Ihre App Daten in diesen Ressourcen ändern muss. Sie können Texturen und Puffer für die dynamische Verwendung erstellen.
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d85933490d1e3bbbd09cc83720651c4fd634012f8e5aa70562396e87c096ebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633100"
---
# <a name="how-to-use-dynamic-resources"></a>Vorgehensweise: Verwenden dynamischer Ressourcen

**Wichtige APIs**

-   [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [**D3D11-NUTZUNG \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

Sie erstellen und verwenden dynamische Ressourcen, wenn Ihre App Daten in diesen Ressourcen ändern muss. Sie können Texturen und Puffer für die dynamische Verwendung erstellen.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Vorgehensweise: Erstellen einer Textur](overviews-direct3d-11-resources-textures-create.md)
-   [Vorgehensweise: Programmgesteuertes Initialisieren einer Textur](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [Vorgehensweise: Erstellen eines Konstantenpuffers](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a>Voraussetzungen

Es wird davon ausgegangen, dass Sie mit C+ vertraut sind. Sie müssen außerdem mit den grundlegenden Konzepten der Grafikprogrammierung vertraut sein.

## <a name="instructions"></a>Anweisungen

### <a name="step-1-specify-dynamic-usage"></a>Schritt 1: Angeben der dynamischen Nutzung

Wenn Sie möchten, dass Ihre App Änderungen an Ressourcen vornehmen kann, müssen Sie diese Ressourcen beim Erstellen als dynamisch und schreibbar angeben.

**So geben Sie die dynamische Nutzung an**

1.  Geben Sie die Ressourcennutzung als dynamisch an. Geben Sie beispielsweise den Wert [**D3D11 \_ USAGE \_ DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) im **Usage-Member** von [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) für einen Scheitelpunkt- oder Konstantenpuffer und den **D3D11 \_ USAGE \_ DYNAMIC-Wert** im **Usage-Member** von [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) für eine 2D-Textur an.
2.  Geben Sie die Ressource als schreibbar an. Geben Sie beispielsweise den Wert [**D3D11 \_ CPU \_ ACCESS \_ WRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) im **MEMBER CPUAccessFlags** von [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) oder [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)an.
3.  Übergeben Sie die Ressourcenbeschreibung an die Erstellungsfunktion. Übergeben Sie beispielsweise die Adresse von [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) an [**ID3D11Device::CreateBuffer,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) und übergeben Sie die Adresse von [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) an [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).

Hier sehen Sie ein Beispiel für das Erstellen eines dynamischen Scheitelpunktpuffers:


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



### <a name="step-2-change-a-dynamic-resource"></a>Schritt 2: Ändern einer dynamischen Ressource

Wenn Sie eine Ressource beim Erstellen als dynamisch und schreibbar angegeben haben, können Sie später Änderungen an dieser Ressource vornehmen.

**So ändern Sie Daten in einer dynamischen Ressource**

1.  Richten Sie die neuen Daten für die Ressource ein. Deklarieren Sie eine [**D3D11 \_ MAPPED \_ SUBRESOURCE-Typvariable,**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) und initialisieren Sie sie mit 0 (null). Sie verwenden diese Variable, um die Ressource zu ändern.
2.  Deaktivieren Sie den GPU-Zugriff (Graphics Processing Unit) auf die Daten, die Sie ändern möchten, und erhalten Sie einen Zeiger auf den Arbeitsspeicher, der die Daten enthält. Um diesen Zeiger abzurufen, übergeben Sie [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) an den *MapType-Parameter,* wenn Sie [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)aufrufen. Legen Sie diesen Zeiger auf die Adresse der [**D3D11 \_ MAPPED \_ SUBRESOURCE-Variablen**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) aus dem vorherigen Schritt fest.
3.  Schreiben Sie die neuen Daten in den Arbeitsspeicher.
4.  Rufen Sie [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) auf, um den GPU-Zugriff auf die Daten wieder zu aktivieren, wenn Sie mit dem Schreiben der neuen Daten fertig sind.

Hier sehen Sie ein Beispiel für das Ändern eines dynamischen Scheitelpunktpuffers:


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



## <a name="remarks"></a>Hinweise

### <a name="using-dynamic-textures"></a>Verwenden dynamischer Texturen

Es wird empfohlen, nur eine dynamische Textur pro Format und möglicherweise pro Größe zu erstellen. Das Erstellen dynamischer Mipmaps, Cubes und Volumes wird aufgrund des zusätzlichen Mehraufwands bei der Zuordnung jeder Ebene nicht empfohlen. Für Mipmaps können Sie [**D3D11 \_ MAP WRITE \_ \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) nur auf der obersten Ebene angeben. Alle Ebenen werden verworfen, indem nur die oberste Ebene zugeordnet wird. Dieses Verhalten ist für Volumes und Cubes identisch. Für Cubes werden die oberste Ebene und das Gesicht 0 zugeordnet.

### <a name="using-dynamic-buffers"></a>Verwenden dynamischer Puffer

Wenn Sie [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) für einen statischen Scheitelpunktpuffer aufrufen, während die GPU den Puffer verwendet, kommt es zu erheblichen Leistungseinbußen. In diesem Fall muss **Map** warten, bis die GPU das Lesen von Scheitelpunkt- oder Indexdaten aus dem Puffer abgeschlossen hat, bevor **Map** zur aufrufenden App zurückkehren kann, was zu einer erheblichen Verzögerung führt. Das Aufrufen von **Map** und das anschließende Rendern aus einem statischen Puffer mehrmals pro Frame verhindert auch, dass die GPU Renderingbefehle puffert, da befehle abgeschlossen werden müssen, bevor der Kartenzeiger zurückgegeben wird. Ohne gepufferte Befehle bleibt die GPU im Leerlauf, bis die App den Scheitelpunktpuffer oder Indexpuffer auffüllt und einen Renderingbefehl ausgibt.

Im Idealfall würden sich die Scheitelpunkt- oder Indexdaten nie ändern, aber dies ist nicht immer möglich. Es gibt viele Situationen, in denen die App Scheitelpunkt- oder Indizierungsdaten für jeden Frame ändern muss, möglicherweise sogar mehrmals pro Frame. In diesen Situationen wird empfohlen, den Scheitelpunkt oder Indexpuffer mit [**D3D11 \_ USAGE \_ DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)zu erstellen. Dieses Verwendungsflag bewirkt, dass die Laufzeit für häufige Zuordnungsvorgänge optimiert wird. **D3D11 \_ USAGE \_ DYNAMIC** ist nur nützlich, wenn der Puffer häufig zugeordnet wird. Wenn Daten konstant bleiben sollen, platzieren Sie diese Daten in einem statischen Scheitelpunkt oder Indexpuffer.

Um eine Leistungsverbesserung zu erzielen, wenn Sie dynamische Scheitelpunktpuffer verwenden, muss Ihre App [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) mit den entsprechenden [**D3D11 \_ MAP-Werten**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) aufrufen. [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) gibt an, dass die App den alten Scheitelpunkt oder die Indexdaten nicht im Puffer aufbewahren muss. Wenn die GPU weiterhin den Puffer verwendet, wenn Sie **Map** mit **D3D11 \_ MAP WRITE \_ \_ DISCARD** aufrufen, gibt die Laufzeit einen Zeiger auf einen neuen Speicherbereich anstelle der alten Pufferdaten zurück. Dadurch kann die GPU die alten Daten weiterhin verwenden, während die App Daten im neuen Puffer platziert. In der App ist keine zusätzliche Speicherverwaltung erforderlich. Der alte Puffer wird automatisch wiederverwendet oder zerstört, wenn die GPU damit fertig ist.

> [!Note]  
> Wenn Sie einen Puffer mit [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)zuordnen, verwirft die Laufzeit immer den gesamten Puffer. Sie können Informationen nicht in nicht zugeordneten Bereichen des Puffers beibehalten, indem Sie einen Offset ungleich 0 (null) oder ein Feld mit begrenzter Größe angeben.

 

Es gibt Fälle, in denen die Datenmenge, die die App pro Karte speichern muss, klein ist, z. B. das Hinzufügen von vier Scheitelpunkten zum Rendern eines Sprites. [**D3D11 \_ MAP \_ WRITE \_ NO \_ OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) gibt an, dass die App die bereits im dynamischen Puffer verwendeten Daten nicht überschreibt. Der [**Map-Aufruf**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) gibt einen Zeiger auf die alten Daten zurück, sodass die App neue Daten in nicht verwendeten Bereichen des Scheitelpunkts oder Indexpuffers hinzufügen kann. Die App darf keine Scheitelpunkte oder Indizes ändern, die in einem Zeichnen-Vorgang verwendet werden, da sie möglicherweise noch von der GPU verwendet werden. Es wird empfohlen, dass die App dann [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) verwendet, nachdem der dynamische Puffer voll ist, um einen neuen Speicherbereich zu erhalten, der die alten Scheitelpunkt- oder Indexdaten nach Abschluss der GPU verwirft.

Der asynchrone Abfragemechanismus ist nützlich, um zu bestimmen, ob Scheitelpunkte noch von der GPU verwendet werden. Geben Sie nach dem letzten Zeichnen-Aufruf, der die Scheitelpunkte verwendet, eine Abfrage vom Typ [**D3D11 \_ QUERY \_ EVENT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) aus. Die Scheitelpunkte werden nicht mehr verwendet, wenn [**ID3D11DeviceContext::GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) S \_ OK zurückgibt. Wenn Sie einen Puffer mit [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) oder ohne Zuordnungswerte zuordnen, wird immer sichergestellt, dass die Scheitelpunkte ordnungsgemäß mit der GPU synchronisiert werden. Wenn Sie jedoch ohne Zuordnungswerte zuordnen, treten die zuvor beschriebenen Leistungseinbußen auf.

> [!Note]  
> Die Ab Windows 8 verfügbare Direct3D 11.1-Runtime ermöglicht die Zuordnung dynamischer Konstantenpuffer und Shaderressourcensichten (SRVs) dynamischer Puffer mit [**D3D11 \_ MAP WRITE NO \_ \_ \_ OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map). Die Direct3D 11- und früheren Runtimes beschränkten die Zuordnung partieller Updates zu Scheitelpunkt- oder Indexpuffern ohne Überschreibung. Um zu ermitteln, ob ein Direct3D-Gerät diese Features unterstützt, rufen Sie ID3D11Device::CheckFeatureSupport with [**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS (ID3D11Device::CheckFeatureSupport mit D3D11 FEATURE D3D11 OPTIONS)**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)auf. [](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) **CheckFeatureSupport** füllt Elemente einer [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) mit den Features des Geräts auf. Die relevanten Member hier sind **MapNoOverwriteOnDynamicConstantBuffer** und **MapNoOverwriteOnDynamicBufferSRV.**

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




