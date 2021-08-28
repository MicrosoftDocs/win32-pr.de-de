---
description: In einer Szene, die viele Objekte enthält, die die gleiche Geometrie verwenden, können Sie viele Instanzen dieser Geometrie in unterschiedlichen Ausrichtungen, Größen, Farben und so weiter zeichnen, mit erheblich besserer Leistung, indem Sie die Menge an Daten reduzieren, die Sie für den Renderer liefern müssen.
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: Effizientes Zeichnen mehrerer Geometry-Instanzen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70586142b58076e5010083f61aeff360aa245a298e5d010fb487aed8b5843ec8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122368"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a>Effizientes Zeichnen mehrerer Geometry-Instanzen (Direct3D 9)

In einer Szene, die viele Objekte enthält, die die gleiche Geometrie verwenden, können Sie viele Instanzen dieser Geometrie in unterschiedlichen Ausrichtungen, Größen, Farben und so weiter zeichnen, mit erheblich besserer Leistung, indem Sie die Menge an Daten reduzieren, die Sie für den Renderer liefern müssen.

Dies kann mithilfe von zwei Techniken erreicht werden: die erste zum Zeichnen indizierter Geometrie und die zweite für nicht indizierte Geometrie. Beide Techniken verwenden zwei Scheitelpunktpuffer: einen zum Liefern von Geometriedaten und einen zum Liefern von Objektinstanzdaten. Die Instanzdaten können eine Vielzahl von Informationen sein, z. B. eine Transformation, Farbdaten oder Beleuchtungsdaten – im Grunde alles, was Sie in einer Scheitelpunktdeklaration beschreiben können. Das Zeichnen vieler Instanzen der Geometrie mit diesen Techniken kann die Menge der an den Renderer gesendeten Daten erheblich reduzieren.

-   [Zeichnen der indizierten Geometrie](#drawing-indexed-geometry)
    -   [Leistungsvergleich der indizierten Geometrie](#indexed-geometry-performance-comparison)
-   [Zeichnen von nicht indizierter Geometrie](#drawing-non-indexed-geometry)
    -   [Nicht indizierter Geometrieleistungsvergleich](#non-indexed-geometry-performance-comparison)
-   [Zugehörige Themen](#related-topics)

## <a name="drawing-indexed-geometry"></a>Zeichnen der indizierten Geometrie

Der Scheitelpunktpuffer enthält Pro-Scheitelpunkt-Daten, die durch eine Scheitelpunktdeklaration definiert werden. Angenommen, ein Teil jedes Scheitelpunkts enthält Geometriedaten, und ein Teil jedes Scheitelpunkts enthält Instanzdaten pro Objekt, wie im folgenden Diagramm dargestellt.

![Diagramm eines Scheitelpunktpuffers für indizierte Geometrie](images/drawingmultipleinstances.png)

Diese Technik erfordert ein Gerät, das das \_ Vertex-Shadermodell 3 0 unterstützt. Diese Technik funktioniert mit jedem programmierbaren Shader, aber nicht mit der festen Funktionspipeline.

Für die oben gezeigten Scheitelpunktpuffer finden Sie hier die entsprechenden Vertexpufferdeklarationen:


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



Diese Deklarationen definieren zwei Scheitelpunktpuffer. Die erste Deklaration (für Stream 0, angegeben durch die Nullen in Spalte 1) definiert die Geometriedaten, die aus folgenden Koordinatendaten bestehen: Position, Normal, Tangens, Binormal und Texturkoordinatendaten.

Die zweite Deklaration (für Stream 1, angegeben durch die in Spalte 1) definiert die Daten pro Objektinstanz. Jede Instanz wird durch vier Gleitkommazahlen mit vier Komponenten und eine Farbe mit vier Komponenten definiert. Die ersten vier Werte können verwendet werden, um eine 4x4-Matrix zu initialisieren. Dies bedeutet, dass diese Daten jede Instanz der Geometrie eindeutig formatieren, positionieren und drehen. Die ersten vier Komponenten verwenden eine Texturkoordinatensemantik, die in diesem Fall bedeutet: "Dies ist eine allgemeine Vier-Komponenten-Zahl". Wenn Sie beliebige Daten in einer Scheitelpunktdeklaration verwenden, verwenden Sie eine Texturkoordinatensemantik, um sie zu markieren. Das letzte Element im Stream wird für Farbdaten verwendet. Dies kann im Vertex-Shader angewendet werden, um jeder Instanz eine eindeutige Farbe zu geben.

Vor dem Rendering müssen Sie [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) aufrufen, um die Scheitelpunktpufferstreams an das Gerät zu binden. Hier ist ein Beispiel, in dem beide Scheitelpunktpuffer gebunden werden:


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



[**SetStreamSourceFreq verwendet**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) [D3DSTREAMSOURCE \_ INDEXEDDATA,](other-direct3d-constants.md) um die indizierten Geometriedaten zu identifizieren. In diesem Fall enthält Stream 0 die indizierten Daten, die die Objektgeometrie beschreiben. Dieser Wert wird logisch mit der Anzahl der Instanzen der zu zeichnenden Geometrie kombiniert.

Beachten Sie, dass D3DSTREAMSOURCE INDEXEDDATA und die Anzahl der zu zeichnenden Instanzen immer im Stream 0 \_ (null) festgelegt werden müssen.

Im zweiten Aufruf verwendet [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) [D3DSTREAMSOURCE \_ INSTANCEDATA,](other-direct3d-constants.md) um den Stream zu identifizieren, der die Instanzdaten enthält. Dieser Wert wird logisch mit 1 kombiniert, da jeder Scheitelpunkt einen Satz von Instanzdaten enthält.

Die letzten beiden Aufrufe von [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) binden die Scheitelpunktpufferzeer an das Gerät.

Wenn Sie mit dem Rendern der Instanzdaten fertig sind, stellen Sie sicher, dass Sie die Vertexstreamhäufigkeit auf den Standardzustand zurücksetzen (der keine Instanzinstancierung verwendet). Da in diesem Beispiel zwei Streams verwendet wurden, legen Sie beide Streams wie unten dargestellt fest:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a>Leistungsvergleich der indizierten Geometrie

Es ist zwar nicht möglich, eine einzige Schlussfolgerung darüber zu ziehen, wie viel diese Technik die Renderzeit in jeder Anwendung reduzieren könnte, aber berücksichtigen Sie den Unterschied in der Menge der daten, die in die Laufzeit gestreamt werden, und die Anzahl der Zustandsänderungen, die reduziert werden, wenn Sie die Instancing-Technik verwenden. Diese Rendersequenz nutzt das Zeichnen mehrerer Instanzen derselben Geometrie:


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



Beachten Sie, dass die Renderschleife einmal aufgerufen wird, die Geometriedaten einmal gestreamt werden und n -Instanzen einmal gestreamt werden. Diese nächste Rendersequenz ist in der Funktionalität identisch, nutzt jedoch nicht die Vorteile der -Instancing:


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



Beachten Sie, dass die gesamte Renderschleife von einer zweiten Schleife umschlossen wird, um jedes Objekt zu zeichnen. Jetzt werden die Geometriedaten n-mal (statt einmal) in den Renderer gestreamt, und alle Pipelinezustände können auch redundant für jedes gezeichnete Objekt festgelegt werden. Diese Rendersequenz ist sehr wahrscheinlich deutlich langsamer. Beachten Sie auch, dass sich die Parameter für [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) zwischen den beiden Renderschleifen nicht geändert haben.

## <a name="drawing-non-indexed-geometry"></a>Zeichnen von nicht indizierter Geometrie

In [Drawing Indexed Geometry](#drawing-indexed-geometry)wurden Scheitelpunktpuffer so konfiguriert, dass mehrere Instanzen der indizierten Geometrie mit höherer Effizienz gezeichnunget werden. Sie können auch [**SetStreamSourceFreq verwenden,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) um nicht indizierte Geometrie zu zeichnen. Dies erfordert ein anderes Scheitelpunktpufferlayout und hat unterschiedliche Einschränkungen. Bereiten Sie die Scheitelpunktpuffer wie im folgenden Diagramm vor, um eine nicht indizierte Geometrie zu zeichnen.

![Diagramm eines Scheitelpunktpuffers für nicht indizierte Geometrie](images/olderstyleinstancing.png)

Diese Technik wird von der Hardwarebeschleunigung auf keinen Geräten unterstützt. Er wird nur von der Softwarevertexverarbeitung unterstützt und funktioniert nur mit [ \_ 3 \_ 0-Shadern.](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md)

Da diese Technik mit nicht indizierter Geometrie funktioniert, gibt es keinen Indexpuffer. Wie das Diagramm zeigt, enthält der Scheitelpunktpuffer, der geometrie enthält, n Kopien der Geometriedaten. Für jede gezeichnete Instanz werden die Geometriedaten aus dem ersten Scheitelpunktpuffer und die Instanzdaten aus dem zweiten Scheitelpunktpuffer gelesen.

Dies sind die entsprechenden Vertexpufferdeklarationen:


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



Diese Deklarationen sind identisch mit den Deklarationen im Beispiel für indizierte Geometrie. Auch hier definiert die erste Deklaration (für Stream 0) die Geometriedaten, und die zweite Deklaration (für Stream 1) definiert die Daten pro Objektinstanz. Wenn Sie den ersten Scheitelpunktpuffer erstellen, laden Sie ihn mit der Anzahl der Instanzen der geometriedaten, die Sie zeichnen möchten.

Vor dem Rendern müssen Sie den Unterteiler einrichten, der die Laufzeit darüber informiert, wie der erste Scheitelpunktpuffer in n Instanzen unterteilt werden soll. Legen Sie dann den Unterteiler [**mitHilfe von SetStreamSourceFreq wie**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) hier festgelegt fest:


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



Der erste Aufruf von [**SetStreamSourceFreq besagt,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) dass Stream 0 n Instanzen von m Vertices enthält. [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) bindet dann Stream 0 an den Geometrie-Scheitelpunktpuffer.

Im zweiten Aufruf identifiziert [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) Stream 1 als Quelle der Instanzdaten. Der zweite Parameter ist die Anzahl der Scheitelzeichen in jedem Objekt (m). Denken Sie daran, dass der Instanzdatenstrom immer als zweiter Stream deklariert werden muss. [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) bindet dann Stream 1 an den Scheitelpunktpuffer, der die Instanzdaten enthält.

Wenn Sie mit dem Rendern der Instanzdaten fertig sind, stellen Sie sicher, dass Sie die Vertexstreamhäufigkeit auf den Standardzustand zurücksetzen. Da in diesem Beispiel zwei Streams verwendet wurden, legen Sie beide Streams wie unten dargestellt fest:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a>Nicht indizierter Geometrieleistungsvergleich

Der Hauptvorteil dieses Instancingstils ist, dass er für nicht indizierte Geometrie verwendet werden kann. Es ist zwar nicht möglich, eine einzige Schlussfolgerung zu ziehen, um wie viel diese Technik die Renderzeit in jeder Anwendung reduzieren könnte, aber berücksichtigen Sie den Unterschied in der Menge der daten, die in die Laufzeit gestreamt werden, und die Anzahl der Zustandsänderungen, die für die folgende Rendersequenz reduziert werden:


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



Beachten Sie, dass die Renderschleife einmal aufgerufen wird. Die Geometriedaten werden einmal gestreamt, obwohl n Instanzen der Geometrie gestreamt werden. Die Daten aus dem Instanz-Scheitelpunktpuffer werden einmal gestreamt. Diese nächste Rendersequenz ist in der Funktionalität identisch, nutzt jedoch nicht die Vorteile der -Instancing:


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



Ohne Instancing muss die Renderschleife von einer zweiten Schleife umschlossen werden, um jedes Objekt zu zeichnen. Wenn Sie die zweite Renderschleife entfernen, sollten Sie eine bessere Leistung aufgrund weniger Änderungen des Renderzustands erwarten, die innerhalb der Schleife aufgerufen werden.

Insgesamt ist es sinnvoll zu erwarten, dass die indizierte Technik[(](#drawing-indexed-geometry)Zeichnen der indizierten Geometrie ) eine bessere Leistung als die nicht indizierte Technik[(Zeichnen](#drawing-non-indexed-geometry)von nicht indizierter Geometrie) auf sich hat, da die indizierte Technik nur eine Kopie der Geometriedaten streamt. Beachten Sie, dass sich die [**Parameter für DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) für keine der Rendersequenzen geändert haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Weiterführende Themen](advanced-topics.md)
</dt> <dt>

[Beispiel für die Instancing](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)
</dt> </dl>

 

 
