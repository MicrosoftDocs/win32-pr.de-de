---
description: Das Erstellen von Puffern erfordert das Definieren der Daten, die der Puffer speichert, das Bereitstellen von Initialisierungs Daten und das Einrichten entsprechender Verwendungs-und Bindungsflags. Informationen zum Erstellen von Texturen finden Sie unter Erstellen von Textur Ressourcen (Direct3D 10).
ms.assetid: 9787b153-9301-4a0f-bd6f-21cc6f7fc650
title: Erstellen von Puffer Ressourcen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d711265775c430728fbcffecd364f746580a566
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748513"
---
# <a name="creating-buffer-resources-direct3d-10"></a>Erstellen von Puffer Ressourcen (Direct3D 10)

Das Erstellen von Puffern erfordert das Definieren der Daten, die der Puffer speichert, das Bereitstellen von Initialisierungs Daten und das Einrichten entsprechender Verwendungs-und Bindungsflags. Informationen zum Erstellen von Texturen finden Sie unter [Erstellen von Textur Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).

-   [Erstellen eines Scheitelpunkt Puffers](#create-a-vertex-buffer)
    -   [Erstellen einer Puffer Beschreibung](#create-a-buffer-description)
    -   [Initialisierungs Daten für den Puffer erstellen](#create-the-initialization-data-for-the-buffer)
    -   [Erstellen des Puffers](#create-the-buffer)
-   [Erstellen eines Index Puffers](#create-an-index-buffer)
-   [Erstellen eines konstanten Puffers](#create-a-constant-buffer)
-   [Zugehörige Themen](#related-topics)

## <a name="create-a-vertex-buffer"></a>Erstellen eines Scheitelpunkt Puffers

Die Schritte zum Erstellen eines [Scheitelpunkt Puffers](d3d10-graphics-programming-guide-resources-types.md) lauten wie folgt.

-   [Erstellen einer Puffer Beschreibung](#create-a-buffer-description)
-   [Initialisierungs Daten für den Puffer erstellen](#create-the-initialization-data-for-the-buffer)
-   [Erstellen des Puffers](#create-the-buffer)

### <a name="create-a-buffer-description"></a>Erstellen einer Puffer Beschreibung

Beim Erstellen eines Scheitelpunkt Puffers wird eine Puffer Beschreibung (siehe [**d3d10 \_ buffer \_**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)Debug) verwendet, um zu definieren, wie Daten im Puffer organisiert werden, wie die Pipeline auf den Puffer zugreifen kann und wie der Puffer verwendet wird.

Im folgenden Beispiel wird veranschaulicht, wie eine Puffer Beschreibung für ein einzelnes Dreieck mit Scheitel Punkten erstellt wird, die Positions-und Farbwerte enthalten.


```
struct SimpleVertex
{
    D3DXVECTOR3 Position;  
    D3DXVECTOR3 Color;  
};

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertex ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
```



In diesem Beispiel wird die Puffer Beschreibung mit fast allen Standardeinstellungen für die [**Verwendung**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), den [**CPU-Zugriff**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) und [**verschiedene Flags**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)initialisiert. Die anderen Einstellungen gelten für das [**Bind-Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) , das die Ressource nur als Vertex-Puffer identifiziert, und die Größe des Puffers.

Die Nutzungs-und CPU-Zugriffsflags sind wichtig für die Leistung. Diese beiden Flags bestimmen, wie oft auf eine Ressource zugegriffen wird, welche Art von Arbeitsspeicher die Ressource in geladen werden kann und welcher Prozessor auf die Ressource zugreifen muss. Standardverwendung diese Ressource wird nicht sehr häufig aktualisiert. Das Festlegen des CPU-Zugriffs auf 0 bedeutet, dass die CPU die Ressource weder lesen noch schreiben muss. In Kombination bedeutet dies, dass die Runtime die Ressource in den höchsten Arbeitsspeicher für die GPU laden kann, da die Ressource keinen CPU-Zugriff benötigt.

Erwartungsgemäß gibt es einen Kompromiss zwischen der optimalen Leistung und der beliebigen Zeit Barrierefreiheit durch beide Prozessoren. Die Standardverwendung ohne CPU-Zugriff bedeutet beispielsweise, dass die Ressource exklusiv für die GPU verfügbar gemacht werden kann. Dies kann das Laden der Ressource in den Arbeitsspeicher einschließen, der nicht direkt von der CPU zugänglich ist. Die Ressource kann nur mit [**updatesubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)geändert werden.

### <a name="create-the-initialization-data-for-the-buffer"></a>Initialisierungs Daten für den Puffer erstellen

Ein Puffer ist lediglich eine Auflistung von Elementen und wird als 1D-Array angelegt. Demzufolge sind die Speicherplatz Auslastung des System Arbeitsspeichers und der Slice des System Speichers identisch. die Größe der Vertex-Daten Deklaration. Eine Anwendung kann Initialisierungs Daten bereitstellen, wenn ein Puffer mit einer unter [**Quell Beschreibung**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data)erstellt wird, die einen Zeiger auf die eigentlichen Ressourcen Daten enthält und Informationen über die Größe und das Layout der Daten enthält.

Jeder mit der unveränderlichen Verwendung erstellte Puffer (siehe [**d3d10 \_ Usage \_ unveränderliche**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) muss zum Zeitpunkt der Erstellung initialisiert werden. Puffer, die eines der anderen nutzungsflags verwenden, können nach der Initialisierung mithilfe von [**copyresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**copysubresourceregion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)und [**updatesubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)aktualisiert werden, oder durch Zugriff auf den zugrunde liegenden Speicher mithilfe der [**map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) -Methode.

### <a name="create-the-buffer"></a>Erstellen des Puffers

Wenn Sie die Puffer Beschreibung und die Initialisierungs Daten (optional) verwenden, [**rufen Sie zum**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) Erstellen eines Scheitel Punkts den Scheitelpunkt-Puffer auf. Der folgende Code Ausschnitt veranschaulicht, wie ein Scheitelpunkt Puffer aus einem Array von Scheitelpunkt Daten erstellt wird, die von der Anwendung deklariert wurden.


```
struct SimpleVertexCombined
{
    D3DXVECTOR3 Pos;  
    D3DXVECTOR3 Col;  
};


ID3D10InputLayout* g_pVertexLayout = NULL;
ID3D10Buffer*      g_pVertexBuffer[2] = { NULL, NULL };
ID3D10Buffer*      g_pIndexBuffer = NULL;


SimpleVertexCombined verticesCombo[] =
{
    D3DXVECTOR3( 0.0f, 0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.0f, 0.5f ),
    D3DXVECTOR3( 0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.5f, 0.0f, 0.0f ),
    D3DXVECTOR3( -0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.5f, 0.0f ),
};


    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
    
    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = verticesCombo;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer[0] );
```



## <a name="create-an-index-buffer"></a>Erstellen eines Index Puffers

Das Erstellen eines Index Puffers ähnelt stark dem Erstellen eines Scheitelpunkt Puffers. mit zwei unterschieden. Ein Index Puffer enthält nur 16-Bit-oder 32-Bit-Daten (anstelle des breiten Bereichs von Formaten, die für einen Vertex-Puffer verfügbar sind. Ein Index Puffer erfordert auch ein Index-Buffer-Bindungsflag.

Im folgenden Beispiel wird veranschaulicht, wie ein Index Puffer aus einem Array von Indexdaten erstellt wird.


```
ID3D10Buffer *g_pIndexBuffer = NULL;

    // Create indices
    unsigned int indices[] = { 0, 1, 2 };

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage           = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
    bufferDesc.BindFlags       = D3D10_BIND_INDEX_BUFFER;
    bufferDesc.CPUAccessFlags  = 0;
    bufferDesc.MiscFlags       = 0;

    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = indices;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
    if( FAILED( hr ) )
        return hr;
  
    g_pd3dDevice->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
```



## <a name="create-a-constant-buffer"></a>Erstellen eines konstanten Puffers

Direct3D 10 führt einen konstanten Puffer ein. Ein konstanter Puffer oder Shader-Konstantenpuffer ist ein Puffer, der shaderkonstanten enthält. Hier ist ein Beispiel für das Erstellen eines konstanten Puffers, der aus dem [HLSLWithoutFX10-Beispiel](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)entnommen wurde.


```
ID3D10Buffer*   g_pConstantBuffer10 = NULL;

struct VS_CONSTANT_BUFFER
{
    D3DXMATRIX mWorldViewProj;      //mWorldViewProj will probably be global to all shaders in a project.
                                    //It's a good idea not to move it around between shaders.
    D3DXVECTOR4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                    //fTime may also be global to all shaders in a project.
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};

    D3D10_BUFFER_DESC cbDesc;
    cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
    cbDesc.Usage = D3D10_USAGE_DYNAMIC;
    cbDesc.BindFlags = D3D10_BIND_CONSTANT_BUFFER;
    cbDesc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
    cbDesc.MiscFlags = 0;
    hr = g_pd3dDevice->CreateBuffer( &cbDesc, NULL, &g_pConstantBuffer10 );
    if( FAILED( hr ) )
       return hr;

    g_pd3dDevice->VSSetConstantBuffers( 0, 1, g_pConstantBuffer10 );
```



Beachten Sie, dass bei Verwendung der [**ID3D10Effect-Schnittstellen**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) Schnittstelle der Prozess des Erstellens, Bindungs-und Auslassen eines konstanten Puffers von der **ID3D10Effect-Schnittstellen** Instanz verarbeitet wird. In diesem Fall ist es nur notwendig, die Variable aus dem Effekt mit einer der GetVariable-Methoden (z. b. [**getvariablebyname**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) ) zu erhalten und die Variable mit einer der SetVariable-Methoden (z. b. [**setMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix)) zu aktualisieren. Ein Beispiel für die Verwendung der **ID3D10Effect-Schnittstelle** zum Verwalten eines konstanten Puffers finden Sie unter [Tutorial 7: Textur Zuordnung und Konstantenpuffer](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



