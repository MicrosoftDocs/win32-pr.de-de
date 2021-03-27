---
title: Verwenden dynamischer Ressourcen
description: Sie erstellen und verwenden dynamische Ressourcen, wenn Ihre APP Daten in diesen Ressourcen ändern muss. Sie können für dynamische Verwendung Texturen und Puffer erstellen.
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41e00cda7236040679c7863454e4cc18d81106b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206367"
---
# <a name="how-to-use-dynamic-resources"></a>Gewusst wie: Verwenden von dynamischen Ressourcen

**Wichtige APIs**

-   [**Verknüpfung id3d11devicecontext aus:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [**Verknüpfung id3d11devicecontext aus:: unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [**D3D11- \_ Verwendung**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

Sie erstellen und verwenden dynamische Ressourcen, wenn Ihre APP Daten in diesen Ressourcen ändern muss. Sie können für dynamische Verwendung Texturen und Puffer erstellen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Vorgehensweise: Erstellen einer Textur](overviews-direct3d-11-resources-textures-create.md)
-   [Gewusst wie: Programm gesteuertes Initialisieren einer Textur](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [Vorgehensweise: Erstellen eines konstanten Puffers](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a>Voraussetzungen

Es wird davon ausgegangen, dass Sie mit C+ vertraut sind. Sie müssen außerdem mit den grundlegenden Konzepten der Grafikprogrammierung vertraut sein.

## <a name="instructions"></a>Instructions

### <a name="step-1-specify-dynamic-usage"></a>Schritt 1: Angeben der dynamischen Verwendung

Wenn Sie möchten, dass Ihre APP Änderungen an Ressourcen vornehmen kann, müssen Sie diese Ressourcen als dynamisch und beschreibbar festlegen, wenn Sie Sie erstellen.

**So geben Sie die dynamische Verwendung an**

1.  Geben Sie die Ressourcenverwendung als dynamisch an. Geben Sie z. b. den dynamischen Wert " [**D3D11 \_ \_ Usage**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) " im **Usage** -Member des [**D3D11- \_ Puffers \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) für einen Scheitelpunkt oder Konstanten Puffer an, und geben Sie den dynamischen Wert für die **D3D11- \_ Verwendung \_** im **Usage** -Member von [**D3D11 \_ TEXTURE2D \_ de SC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) für eine 2D-Textur an.
2.  Geben Sie die Ressource als beschreibbar an. Geben Sie z. b. den [**D3D11 \_ CPU \_ Access \_ Write**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) -Wert im **cpuaccessflags** -Member von [**D3D11 \_ buffer \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) oder [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)an.
3.  Übergeben Sie die Ressourcen Beschreibung an die Erstellungs Funktion. Übergeben Sie z. b. die Adresse des [**D3D11- \_ Puffers \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) an [**ID3D11Device:: up Buffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) , und übergeben Sie die Adresse von [**D3D11 \_ TEXTURE2D \_ de SC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) an [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).

Im folgenden finden Sie ein Beispiel für die Erstellung eines dynamischen Scheitelpunkt Puffers:


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

Wenn Sie beim Erstellen eine Ressource als dynamisch und beschreibbar angegeben haben, können Sie später Änderungen an dieser Ressource vornehmen.

**So ändern Sie Daten in einer dynamischen Ressource**

1.  Richten Sie die neuen Daten für die Ressource ein. Deklarieren Sie eine D3D11 zugeordnete unter [**\_ \_ geordnete Quellentyp**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) Variable, und initialisieren Sie Sie mit NULL. Sie verwenden diese Variable, um die Ressource zu ändern.
2.  Deaktivieren Sie den GPU-Zugriff (Graphics Processing Unit) auf die Daten, die Sie ändern möchten, und erhalten Sie einen Zeiger auf den Arbeitsspeicher, der die Daten enthält. Um diesen Zeiger zu erhalten, übergeben Sie [**D3D11 \_ map \_ Write \_ verwerfen**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) an den *maptype* -Parameter, wenn Sie [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)aufrufen. Legen Sie diesen Zeiger auf die Adresse der D3D11 zugeordneten untergeordneten [**\_ \_ Quell**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) Variablen aus dem vorherigen Schritt fest.
3.  Schreiben Sie die neuen Daten in den Arbeitsspeicher.
4.  Aufrufen von [**Verknüpfung id3d11devicecontext aus:: unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) zum erneuten Aktivieren des GPU-Zugriffs auf die Daten, wenn Sie mit dem Schreiben der neuen Daten fertig sind.

Im folgenden finden Sie ein Beispiel für das Ändern eines dynamischen Scheitelpunkt Puffers:


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



## <a name="remarks"></a>Bemerkungen

### <a name="using-dynamic-textures"></a>Verwenden dynamischer Texturen

Es wird empfohlen, nur eine dynamische Textur Pro Format und möglicherweise pro Größe zu erstellen. Das Erstellen dynamischer Mipmaps, Cubes und Volumes ist aufgrund des zusätzlichen Aufwands bei der Zuordnung jeder Ebene nicht empfehlenswert. Für Mipmaps können Sie [**D3D11 \_ map \_ Write \_ verwerfen**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) nur auf der obersten Ebene angeben. Alle Ebenen werden verworfen, indem nur die oberste Ebene abgeordnet wird. Dieses Verhalten ist für Volumes und Cubes identisch. Bei Cubes werden die oberste Ebene und die Vorderseite 0 zugeordnet.

### <a name="using-dynamic-buffers"></a>Verwenden dynamischer Puffer

Wenn Sie die [**Zuordnung auf einem**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) statischen Scheitelpunkt Puffer aufzurufen, während die GPU den Puffer verwendet, erhalten Sie eine beträchtliche Leistungs Einbuße. In dieser Situation muss **map** warten, bis die GPU das Lesen von Vertex-oder Indexdaten aus dem Puffer abgeschlossen hat, bevor **map** an die aufrufende App zurückgegeben werden kann, was zu einer erheblichen Verzögerung führt. Wenn Sie **map** und das anschließende Rendering von einem statischen Puffer mehrmals pro Frame aufrufen, wird außerdem verhindert, dass die GPU renderingbefehle puffert, da Sie vor dem Zurückgeben des Karten Zeigers Befehle beenden muss. Ohne gepufferte Befehle bleibt die GPU im Leerlauf, bis die APP das Ausfüllen des Vertex-Puffers oder Index Puffers abgeschlossen hat und einen Renderingbefehl ausgibt.

Im Idealfall würden sich die Scheitelpunkt-oder Indexdaten nie ändern, aber dies ist nicht immer möglich. Es gibt viele Situationen, in denen die APP den Scheitelpunkt oder Indexdaten jedes Frames ändern muss, vielleicht sogar mehrmals pro Frame. In diesen Fällen wird empfohlen, dass Sie den Scheitelpunkt oder Index Puffer mit [**\_ \_ dynamischer D3D11-Verwendung**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)erstellen. Dieses nutzungsflag bewirkt, dass die Laufzeit bei häufigen Zuordnungs Vorgängen optimiert wird. **D3D11 \_ Die Verwendung von \_ Dynamic** ist nur nützlich, wenn der Puffer häufig zugeordnet wird. Wenn die Daten konstant bleiben sollen, platzieren Sie diese Daten in einem statischen Scheitelpunkt oder Index Puffer.

Um eine Leistungsverbesserung bei der Verwendung dynamischer Scheitelpunkt Puffer zu erhalten, muss Ihre APP [**map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) mit den entsprechenden [**D3D11 \_ map**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) -Werten aufzurufen. [**D3D11 \_ Die \_ Schreib \_ Verwerfungs**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) Zuordnung gibt an, dass die APP die alten Scheitelpunkt-oder Indexdaten nicht im Puffer aufbewahren muss. Wenn die GPU den Puffer weiterhin verwendet, wenn Sie **map** mit **D3D11 \_ map \_ Write \_ verwerfen** verwenden, gibt die Laufzeit einen Zeiger auf einen neuen Speicherbereich anstelle der alten Puffer Daten zurück. Dadurch kann die GPU die alten Daten weiterhin verwenden, während die APP Daten in den neuen Puffer platziert. In der APP ist keine zusätzliche Speicherverwaltung erforderlich. der alte Puffer wird wieder verwendet oder automatisch zerstört, wenn die GPU damit fertig ist.

> [!Note]  
> Wenn Sie einen Puffer mit [**D3D11 \_ map \_ Write \_ verwerfen**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)zuordnen, verwirft die Common Language Runtime immer den gesamten Puffer. Informationen in nicht zugeordneten Bereichen des Puffers können nicht beibehalten werden, indem Sie ein Offset oder ein Feld mit eingeschränkter Größe angeben.

 

Es gibt Fälle, in denen die Datenmenge, die in der APP gespeichert werden muss, klein ist, z. b. das Hinzufügen von vier Vertices zum Rendering eines Sprite. [**D3D11 \_ Map \_ Write \_ No \_ Überschreibung**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) gibt an, dass die APP keine Daten überschreibt, die bereits im dynamischen Puffer verwendet werden. Der [](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) Zuordnungs Befehl gibt einen Zeiger auf die alten Daten zurück, wodurch die APP neue Daten in nicht verwendeten Bereichen des Scheitel Punkts oder Index Puffers hinzufügen kann. Die APP darf keine Scheitel Punkte oder Indizes ändern, die in einem zeichnen-Vorgang verwendet werden, da Sie möglicherweise noch von der GPU verwendet werden. Es wird empfohlen, dass die APP dann [**D3D11 \_ map \_ Write \_ verwerfen**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) verwendet, nachdem der dynamische Puffer voll ist, um einen neuen Arbeitsbereich zu erhalten, der die alten Scheitelpunkt-oder Indexdaten nach Abschluss der GPU verwirft.

Der asynchrone Abfrage Mechanismus ist hilfreich, um zu bestimmen, ob Scheitel Punkte weiterhin von der GPU verwendet werden. Geben Sie nach dem letzten zeichnen-Befehl, der die Scheitel Punkte verwendet, eine Abfrage vom Typ [**D3D11 \_ Query- \_ Ereignis**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) aus. Die Scheitel Punkte werden nicht mehr verwendet, wenn [**Verknüpfung id3d11devicecontext aus:: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) S \_ OK zurückgibt. Wenn Sie einen Puffer mit [**D3D11 \_ map \_ Write \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) oder No Map Values zuordnen, sind Sie immer sicher, dass die Vertices ordnungsgemäß mit der GPU synchronisiert werden. Wenn Sie jedoch die Zuordnung ohne Kartenwerte durchführt, wird die zuvor beschriebene Leistungs Einbuße verursacht.

> [!Note]  
> Die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist, ermöglicht das Zuordnen dynamischer konstanter Puffer und der Shader-Ressourcen Sichten (Srvs) dynamischer Puffer mit [**D3D11 \_ map \_ Write \_ No über \_ Schreiben**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map). Mit den Laufzeiten "Direct3D 11" und "frühere Laufzeiten" wurde die Zuordnung von partiellen Updates zum Scheitelpunkt oder Index Puffer eingeschränkt. Um zu ermitteln, ob ein Direct3D-Gerät diese Features unterstützt, wenden Sie [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) mit [**D3D11 \_ Feature \_ D3D11- \_ Optionen**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)an. **Checkfeaturesupport** füllt Mitglieder einer [**D3D11 \_ Feature \_ Data \_ D3D11 \_ options**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) -Struktur mit den Funktionen des Geräts. Die relevanten Elemente sind " **mapnooverwrite teondynamicconstantbuffer** " und " **mapnooverwrite teondynamicbuffersrv**".

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




