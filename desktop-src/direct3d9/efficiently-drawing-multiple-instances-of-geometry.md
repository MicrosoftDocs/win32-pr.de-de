---
description: Bei einer Szene, die viele Objekte enthält, die dieselbe Geometrie verwenden, können Sie viele Instanzen dieser Geometrie mit unterschiedlicher Ausrichtung, Größe, Farben usw. mit einer erheblich besseren Leistung erstellen, indem Sie die Menge an Daten verringern, die Sie für den Renderer bereitstellen müssen.
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: Effizientes Zeichnen mehrerer Instanzen von Geometry (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9981dff913b704fca5e6b211b57e3647fddd28c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860094"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a>Effizientes Zeichnen mehrerer Instanzen von Geometry (Direct3D 9)

Bei einer Szene, die viele Objekte enthält, die dieselbe Geometrie verwenden, können Sie viele Instanzen dieser Geometrie mit unterschiedlicher Ausrichtung, Größe, Farben usw. mit einer erheblich besseren Leistung erstellen, indem Sie die Menge an Daten verringern, die Sie für den Renderer bereitstellen müssen.

Dies kann durch die Verwendung von zwei Techniken erreicht werden: das erste zum Zeichnen der indizierten Geometrie und das zweite für die nicht indizierte Geometrie. Beide Verfahren verwenden zwei Scheitelpunkt Puffer: einen für die Bereitstellung von Geometriedaten und einen für die Bereitstellung von pro-Objekt-Instanzdaten. Bei den Instanzdaten kann es sich um eine Vielzahl von Informationen handeln, wie z. b. eine Transformation, Farbdaten oder Beleuchtungs Daten, was Sie in einer Scheitelpunkt Deklaration beschreiben können. Wenn viele Instanzen der Geometrie mit diesen Techniken gezeichnet werden, kann die Menge an Daten, die an den Renderer gesendet werden, drastisch reduziert werden.

-   [Zeichnen der indizierten Geometrie](#drawing-indexed-geometry)
    -   [Vergleich der indizierten Geometrie Leistung](#indexed-geometry-performance-comparison)
-   [Zeichnen von nicht indizierten Geometrie](#drawing-non-indexed-geometry)
    -   [Vergleich der nicht indizierten Geometrie Leistung](#non-indexed-geometry-performance-comparison)
-   [Zugehörige Themen](#related-topics)

## <a name="drawing-indexed-geometry"></a>Zeichnen der indizierten Geometrie

Der Vertex-Puffer enthält pro-Vertex-Daten, die durch eine Scheitelpunkt Deklaration definiert werden. Angenommen, ein Teil eines Scheitel Punkts enthält Geometry-Daten, und ein Teil jedes Scheitel Punkts enthält Objektinstanzdaten, wie in der folgenden Abbildung dargestellt.

![Diagramm eines Scheitelpunkt Puffers für die indizierte Geometrie](images/drawingmultipleinstances.png)

Diese Technik erfordert ein Gerät, das das 3 \_ 0-Vertex-Shader-Modell unterstützt. Diese Methode funktioniert mit jedem programmierbaren Shader, aber nicht mit der Fixed-Funktions Pipeline.

Für die oben gezeigten Scheitelpunkt Puffer sind hier die entsprechenden Vertex-Puffer Deklarationen aufgeführt:


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



Diese Deklarationen definieren zwei Scheitelpunkt Puffer. Die erste Deklaration (für Stream 0, angegeben durch die Nullen in Spalte 1) definiert die Geometry-Daten, die aus folgenden Elementen bestehen: Position, normal, Tangens, Binormal und Texturkoordinaten Daten.

Die zweite Deklaration (für Stream 1, die durch die in Spalte 1 angegeben ist) definiert die Instanzdaten pro Objekt. Jede Instanz wird von Gleit Komma Zahlen der 4 4-Komponente und einer Farbe mit vier Komponenten definiert. Die ersten vier Werte können verwendet werden, um eine 4 x 4-Matrix zu initialisieren, was bedeutet, dass diese Daten jede Instanz der Geometrie eindeutig anpassen, positionieren und drehen. Die ersten vier Komponenten verwenden eine Texturkoordinaten Semantik, die in diesem Fall "Dies ist eine allgemeine vier-Komponenten-Zahl" bedeutet. Wenn Sie in einer Scheitelpunkt Deklaration beliebige Daten verwenden, verwenden Sie eine Texturkoordinaten Semantik, um Sie zu markieren. Das letzte Element im Stream wird für Farbdaten verwendet. Dies kann im Vertex-Shader angewendet werden, um jeder Instanz eine eindeutige Farbe zu geben.

Vor dem Rendering müssen Sie [**setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) aufrufen, um die Vertex-Puffer Datenströme an das Gerät zu binden. Es folgt ein Beispiel, das beide Scheitel Punkte bindet:


```
// Set up the geometry data stream
pd3dDevice->SetStreamSourceFreq(0,
    (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
    D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1,
    (D3DSTREAMSOURCE_INSTANCEDATA | 1));
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
    D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



[**Setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) verwendet [D3DSTREAMSOURCE \_ indexeddata](other-direct3d-constants.md) , um die indizierten Geometriedaten zu identifizieren. In diesem Fall enthält Stream 0 die indizierten Daten, die die Objekt Geometrie beschreiben. Dieser Wert wird logisch mit der Anzahl der zu zeichnenden Instanzen der Geometrie kombiniert.

Beachten Sie, dass D3DSTREAMSOURCE \_ indexeddata und die Anzahl der zu zeichnenden Instanzen immer im Stream NULL festgelegt werden müssen.

Im zweiten Befehl verwendet [**setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) [D3DSTREAMSOURCE \_ InstanceData](other-direct3d-constants.md) , um den Stream zu identifizieren, der die Instanzdaten enthält. Dieser Wert wird logisch mit 1 kombiniert, da jeder Scheitelpunkt einen Satz von Instanzdaten enthält.

Mit den letzten zwei Aufrufen von [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) werden die Vertex-Puffer Zeiger an das Gerät gebunden.

Wenn Sie das Rendering der Instanzdaten abgeschlossen haben, stellen Sie sicher, dass die vertexstreamfrequenz auf den Standardzustand zurückgesetzt wird (der keine Instanziierung verwendet). Da in diesem Beispiel zwei Streams verwendet werden, legen Sie beide Streams wie unten dargestellt fest:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a>Vergleich der indizierten Geometrie Leistung

Es ist zwar nicht möglich, eine einzelne Schlussfolgerung zu treffen, wie viel diese Technik die Renderingzeit in jeder Anwendung reduzieren könnte, aber berücksichtigen Sie den Unterschied in der Menge der Daten, die in die Laufzeit gestreamt werden, sowie die Anzahl der Zustandsänderungen, die bei Verwendung der instanziierungsmethode reduziert werden. Diese Rendering-Sequenz nutzt das Zeichnen mehrerer Instanzen derselben Geometrie:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set up the geometry data stream
    pd3dDevice->SetStreamSourceFreq(0,
                (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1,
                (D3DSTREAMSOURCE_INSTANCEDATA | 1));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



Beachten Sie, dass die Renderschleife einmal aufgerufen wird, die Geometry-Daten einmal gestreamt werden und n Instanzen einmal gestreamt werden. Diese nächste Rendering-Sequenz ist identisch mit der Funktionalität, aber Sie nutzt nicht die Instanziierung:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));


        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }                             
    
    pd3dDevice->EndScene();
}
```



Beachten Sie, dass die gesamte Renderschleife durch eine zweite Schleife umschließt, um jedes Objekt zu zeichnen. Nun werden die Geometry-Daten in den Renderer n-Mal (anstatt einmal) gestreamt, und alle Pipeline Zustände können auch redundant für jedes gezeichnete Objekt festgelegt werden. Diese Rendering-Sequenz ist sehr wahrscheinlich bedeutend langsamer. Beachten Sie auch, dass sich die Parameter für [**drawindexedprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) nicht zwischen den beiden Rendering-Schleifen geändert haben.

## <a name="drawing-non-indexed-geometry"></a>Zeichnen von nicht indizierten Geometrie

Beim [Zeichnen indizierter Geometrie](#drawing-indexed-geometry)wurden Vertex-Puffer so konfiguriert, dass mehrere Instanzen der indizierten Geometrie mit größerer Effizienz gezeichnet werden. Sie können auch [**setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) verwenden, um eine nicht indizierte Geometrie zu zeichnen. Hierfür ist ein anderes Vertex-Puffer Layout erforderlich, das über unterschiedliche Einschränkungen verfügt. Um die nicht indizierte Geometrie zu zeichnen, bereiten Sie die Scheitelpunkt Puffer wie das folgende Diagramm vor.

![Diagramm eines Scheitelpunkt Puffers für nicht indizierte Geometrie](images/olderstyleinstancing.png)

Diese Technik wird von der Hardwarebeschleunigung auf keinem Gerät unterstützt. Sie wird nur von der Verarbeitung von Software Scheitel Punkten unterstützt und funktioniert nur mit [vs \_ 3 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) -Shadern.

Da diese Technik mit nicht indizierter Geometrie funktioniert, gibt es keinen Index Puffer. Wie das Diagramm zeigt, enthält der Vertex-Puffer, der die Geometrie enthält, n Kopien der Geometriedaten. Für jede Instanz, die gezeichnet wird, werden die Geometriedaten aus dem ersten Vertex-Puffer gelesen, und die Instanzdaten werden aus dem zweiten Vertex-Puffer gelesen.

Im folgenden sind die entsprechenden Vertex-Puffer Deklarationen aufgeführt:


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



Diese Deklarationen sind identisch mit den Deklarationen, die im Beispiel für indizierte Geometrie vorgenommen werden. Die erste Deklaration (für Stream 0) definiert die Geometry-Daten, und die zweite Deklaration (für Stream 1) definiert die Instanzdaten pro Objekt. Wenn Sie den ersten Vertex-Puffer erstellen, achten Sie darauf, dass Sie ihn mit der Anzahl von Instanzen der Geometry-Daten laden, die Sie zeichnen werden.

Vor dem Rendering müssen Sie den unter Teiler einrichten, der der Laufzeit mitteilt, wie der erste Vertex-Puffer in n Instanzen aufgeteilt werden soll. Legen Sie dann den unter Teiler mithilfe von [**setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) wie folgt fest:


```
// Set the divider
pd3dDevice->SetStreamSourceFreq(0, 1);
// Bind the stream to the vertex buffer
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
        D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance);
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
        D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



Der erste Aufrufen von [**setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) besagt, dass Stream 0 n Instanzen von m Scheitel Punkten enthält. [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) bindet dann Stream 0 an den Geometrie Scheitelpunkt Puffer.

Im zweiten-Befehl identifiziert [**setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) Stream 1 als Quelle der Instanzdaten. Der zweite Parameter ist die Anzahl der Vertices in jedem Objekt (m). Beachten Sie, dass der instanzdatenstream immer als zweiter Stream deklariert werden muss. [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) bindet dann Stream 1 an den Vertex-Puffer, der die Instanzdaten enthält.

Wenn Sie mit dem Rendern der Instanzdaten fertig sind, stellen Sie sicher, dass die vertexstreamfrequenz auf ihren Standardzustand zurückgesetzt wird. Da in diesem Beispiel zwei Streams verwendet werden, legen Sie beide Streams wie unten dargestellt fest:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a>Vergleich der nicht indizierten Geometrie Leistung

Der Hauptvorteil dieses instanziierungsstils besteht darin, dass er für nicht indizierte Geometrie verwendet werden kann. Es ist zwar nicht möglich, eine einzelne Schlussfolgerung zu treffen, wie viel diese Technik die Renderingzeit in jeder Anwendung reduzieren könnte, aber berücksichtigen Sie den Unterschied in der Menge der Daten, die in die Laufzeit gestreamt werden, sowie die Anzahl der Zustandsänderungen, die für die folgende rendersequenz reduziert werden:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set the divider
    pd3dDevice->SetStreamSourceFreq(0, 1);
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



Beachten Sie, dass die Renderschleife einmal aufgerufen wird. Die Geometry-Daten werden einmal gestreamt, obwohl n Instanzen der Geometrie vorhanden sind, die gestreamt werden. Die Daten aus dem Vertex-instanzpuffer werden einmal gestreamt. Diese nächste Rendering-Sequenz ist identisch mit der Funktionalität, aber Sie nutzt nicht die Instanziierung:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }
    
    pd3dDevice->EndScene();
}
```



Ohne Instanziierung muss die Renderschleife durch eine zweite Schleife umschließt werden, um jedes Objekt zu zeichnen. Durch das Eliminieren der zweiten Renderschleife sollten Sie eine bessere Leistung erwarten, da weniger renderstatusänderungen innerhalb der Schleife aufgerufen werden.

Insgesamt empfiehlt es sich zu erwarten, dass die indizierte Technik ([Zeichnen der indizierten Geometrie](#drawing-indexed-geometry)) eine bessere Leistung als die nicht indizierte Technik ([Zeichnen nicht indizierter Geometrie](#drawing-non-indexed-geometry)) erwartet, da die indizierte Technik nur eine Kopie der Geometriedaten streamt. Beachten Sie, dass die Parameter für [**drawindexedprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) für eine der Rendering-Sequenzen nicht geändert wurden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Themen](advanced-topics.md)
</dt> <dt>

[Instanziierungsbeispiel](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)
</dt> </dl>

 

 
