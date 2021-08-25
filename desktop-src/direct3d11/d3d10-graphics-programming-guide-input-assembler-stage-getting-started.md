---
title: Erste Schritte mit der Input-Assembler Stage
description: Es sind einige Schritte erforderlich, um die Phase des Eingabeassemblierers (Input-Assembler, IA) zu initialisieren.
ms.assetid: 84c0ca29-2356-4b7f-98ee-ff1758edc540
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513e7452eebf157a80d4239127bf1d04a014375f7bbaf06e4f5814199d7ba053
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858210"
---
# <a name="getting-started-with-the-input-assembler-stage"></a>Erste Schritte mit der Input-Assembler Stage

Es sind einige Schritte erforderlich, um die Phase des Eingabeassemblierers (Input-Assembler, IA) zu initialisieren. Beispielsweise müssen Sie Pufferressourcen mit den von der Pipeline benötigten Scheitelpunktdaten erstellen, der IA-Phase mitteilen, wo sich die Puffer befinden und welche Art von Daten sie enthalten, und den Typ der Primitive angeben, die aus den Daten zusammengesetzt werden sollen.

Die grundlegenden Schritte zum Einrichten der IA-Phase, die in der folgenden Tabelle gezeigt werden, werden in diesem Thema behandelt.



| Schritt                                                                                    | BESCHREIBUNG                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Erstellen von Eingabepuffern](#create-input-buffers)                                           | Erstellen und Initialisieren von Eingabepuffern mit Eingabevertexdaten.                                           |
| [Erstellen des Input-Layout-Objekts](#create-the-input-layout-object)                       | Definieren Sie mithilfe eines Eingabelayoutobjekts, wie die Scheitelpunktpufferdaten in die IA-Phase gestreamt werden. |
| [Binden von Objekten an die Input-Assembler Phase](#bind-objects-to-the-input-assembler-stage) | Binden Sie die erstellten Objekte (Eingabepuffer und das Eingabelayoutobjekt) an die IA-Phase.                 |
| [Angeben des primitiven Typs](#specify-the-primitive-type)                               | Identifizieren Sie, wie die Scheitelpunkte zu Primitiven zusammengesetzt werden.                                          |
| [Aufrufen von Draw-Methoden](#call-draw-methods)                                                 | Senden Sie die Daten, die über die Pipeline an die IA-Phase gebunden sind.                                             |



 

Nachdem Sie diese Schritte verstanden haben, fahren Sie mit [Using System-Generated Values](d3d10-graphics-programming-guide-input-assembler-stage-using.md)fort.

## <a name="create-input-buffers"></a>Erstellen von Eingabepuffern

Es gibt zwei Arten von Eingabepuffern: [Scheitelpunktpuffer](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) und Indexpuffer. Vertexpuffer stellen Scheitelpunktdaten für die IA-Phase bereit. Indexpuffer sind optional. sie stellen Indizes für Scheitelpunkte aus dem Scheitelpunktpuffer bereit. Sie können einen oder mehrere Scheitelpunktpuffer und optional einen Indexpuffer erstellen.

Nachdem Sie die Pufferressourcen erstellt haben, müssen Sie ein Eingabelayoutobjekt erstellen, um das Datenlayout an die IA-Phase zu beschreiben. Anschließend müssen Sie die Pufferressourcen an die IA-Phase binden. Das Erstellen und Binden von Puffern ist nicht erforderlich, wenn Ihre Shader keine Puffer verwenden. Ein Beispiel für einen einfachen Scheitelpunkt- und Pixel-Shader, der ein einzelnes Dreieck zeichnet, finden Sie unter [Verwenden der Input-Assembler Stage ohne Puffer.](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md)

Hilfe zum Erstellen eines Scheitelpunktpuffers finden Sie unter [Erstellen eines Scheitelpunktpuffers.](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating) Hilfe zum Erstellen eines Indexpuffers finden Sie unter Erstellen eines Indexpuffers.

## <a name="create-the-input-layout-object"></a>Erstellen des Input-Layout-Objekts

Das Eingabelayoutobjekt kapselt den Eingabezustand der IA-Phase. Dies schließt eine Beschreibung der Eingabedaten ein, die an die IA-Phase gebunden sind. Die Daten werden aus dem Arbeitsspeicher, aus einem oder mehreren Scheitelpunktpuffern in die IA-Phase gestreamt. Die Beschreibung identifiziert die Eingabedaten, die von einem oder mehreren Scheitelpunktpuffern gebunden sind, und gibt der Laufzeit die Möglichkeit, die Eingabedatentypen anhand der Eingabeparametertypen des Shaders zu überprüfen. Diese Typüberprüfung überprüft nicht nur, ob die Typen kompatibel sind, sondern auch, dass jedes der Elemente, die der Shader benötigt, in den Pufferressourcen verfügbar ist.

Ein Eingabelayoutobjekt wird aus einem Array von Eingabeelementbeschreibungen und einem Zeiger auf den kompilierten Shader erstellt (siehe [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)). Das Array enthält mindestens ein Eingabeelement. jedes Eingabeelement beschreibt ein einzelnes Vertexdatenelement aus einem einzelnen Scheitelpunktpuffer. Der vollständige Satz der Eingabeelementbeschreibungen dient der Beschreibung aller Vertex-Datenelemente von sämtlichen Vertex-Puffern, die an die IA-Phase gebunden werden.

Die folgende Layoutbeschreibung beschreibt einen einzelnen Scheitelpunktpuffer, der drei Vertexdatenelemente enthält:


```
D3D11_INPUT_ELEMENT_DESC layout[] =
{
    { L"POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT, 0, 12, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
};
```



Eine Eingabeelementbeschreibung beschreibt jedes Element, das in einem einzelnen Scheitelpunkt in einem Scheitelpunktpuffer enthalten ist, einschließlich Größe, Typ, Position und Zweck. Jede Zeile identifiziert den Datentyp mithilfe der Semantik, des semantischen Indexes und des Datenformats. Eine [Semantik](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) ist eine Textzeichenfolge, die angibt, wie die Daten verwendet werden. In diesem Beispiel identifiziert die erste Zeile Positionsdaten mit drei Komponenten ( z. B.*xyz);* Die zweite Zeile identifiziert Texturdaten mit zwei Komponenten (*z. B. UV);* und die dritte Zeile identifiziert normale Daten.

In diesem Beispiel einer Eingabeelementbeschreibung wird der semantische Index (der zweite Parameter) für alle drei Zeilen auf 0 (null) festgelegt. Der semantische Index hilft dabei, zwischen zwei Zeilen zu unterscheiden, die dieselbe Semantik verwenden. Da es in diesem Beispiel keine ähnliche Semantik gibt, kann der semantische Index auf den Standardwert 0 (null) festgelegt werden.

Der dritte Parameter ist das *Format*. Das Format (siehe [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) gibt die Anzahl der Komponenten pro Element und den Datentyp an, der die Größe der Daten für jedes Element definiert. Das Format kann zum Zeitpunkt der Ressourcenerstellung vollständig eingegeben werden, oder Sie können eine Ressource mithilfe eines **DXGI \_ FORMAT** erstellen, das die Anzahl der Komponenten in einem Element identifiziert, aber den Datentyp nicht definiert lässt.

### <a name="input-slots"></a>Eingabeslots

Daten gelangen über Eingaben, die als *Eingabeslots* bezeichnet werden, in die IA-Phase, wie in der folgenden Abbildung dargestellt. Die IA-Phase verfügt über *n* Eingabeslots, die so konzipiert sind, dass sie bis zu *n* Scheitelpunktpuffer aufnehmen können, die Eingabedaten bereitstellen. Jeder Scheitelpunktpuffer muss einem anderen Slot zugewiesen werden. Diese Informationen werden in der Eingabelayoutdeklaration gespeichert, wenn das Eingabelayoutobjekt erstellt wird. Sie können auch einen Offset vom Anfang jedes Puffers bis zum ersten Zu lesenden Element im Puffer angeben.

![Abbildung der Eingabeslots für die ia-Phase](images/d3d10-ia-slots.png)

Die nächsten beiden Parameter sind der *Eingabeslot* und der *Eingabeoffset*. Wenn Sie mehrere Puffer verwenden, können Sie sie an einen oder mehrere Eingabeslots binden. Der Eingabeoffset ist die Anzahl der Bytes zwischen dem Anfang des Puffers und dem Anfang der Daten.

### <a name="reusing-input-layout-objects"></a>Wiederverwenden von Input-Layout-Objekten

Jedes Eingabelayoutobjekt wird basierend auf einer Shadersignatur erstellt. Dadurch kann die API die Input-Layout-Object-Elemente anhand der Shader-Eingabesignatur überprüfen, um sicherzustellen, dass eine genaue Übereinstimmung von Typen und Semantik vorliegt. Sie können ein einzelnes Eingabelayoutobjekt für viele Shader erstellen, solange alle Shader-Eingabesignaturen genau übereinstimmen.

## <a name="bind-objects-to-the-input-assembler-stage"></a>Binden von Objekten an die Input-Assembler Phase

Nachdem Sie Vertexpufferressourcen und ein Eingabelayoutobjekt erstellt haben, können Sie sie an die IA-Phase binden, indem Sie [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) und [**ID3D11DeviceContext::IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout)aufrufen. Das folgende Beispiel zeigt die Bindung eines einzelnen Scheitelpunktpuffers und eines Eingabelayoutobjekts an die IA-Phase:


```
UINT stride = sizeof( SimpleVertex );
UINT offset = 0;
g_pd3dDevice->IASetVertexBuffers( 
    0,                // the first input slot for binding
    1,                // the number of buffers in the array
    &g_pVertexBuffer, // the array of vertex buffers
    &stride,          // array of stride values, one for each buffer
    &offset );        // array of offset values, one for each buffer

// Set the input layout
g_pd3dDevice->IASetInputLayout( g_pVertexLayout );
```



Zum Binden des Eingabelayoutobjekts ist nur ein Zeiger auf das -Objekt erforderlich.

Im vorherigen Beispiel wird ein einzelner Scheitelpunktpuffer gebunden. mehrere Scheitelpunktpuffer können jedoch durch einen einzelnen Aufruf von [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers)gebunden werden, und der folgende Code zeigt einen solchen Aufruf zum Binden von drei Scheitelpunktpuffern:


```
UINT strides[3];
strides[0] = sizeof(SimpleVertex1);
strides[1] = sizeof(SimpleVertex2);
strides[2] = sizeof(SimpleVertex3);
UINT offsets[3] = { 0, 0, 0 };
g_pd3dDevice->IASetVertexBuffers( 
    0,                 //first input slot for binding
    3,                 //number of buffers in the array
    &g_pVertexBuffers, //array of three vertex buffers
    &strides,          //array of stride values, one for each buffer
    &offsets );        //array of offset values, one for each buffer
```



Ein Indexpuffer wird durch Aufrufen von [**ID3D11DeviceContext::IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer)an die IA-Phase gebunden.

## <a name="specify-the-primitive-type"></a>Angeben des primitiven Typs

Nachdem die Eingabepuffer gebunden wurden, muss der IA-Stufe mitgeteilt werden, wie die Scheitelpunkte zu Primitiven zusammengesetzt werden sollen. Dies erfolgt durch Angeben des [primitiven Typs](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) durch Aufrufen von [**ID3D11DeviceContext::IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); Der folgende Code ruft diese Funktion auf, um die Daten als Dreiecksliste ohne Adjazenz zu definieren:


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



Die restlichen primitiven Typen sind unter [**D3D \_ PRIMITIVE \_ TOPOLOGY**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology)aufgeführt.

## <a name="call-draw-methods"></a>Aufrufen von Draw-Methoden

Nachdem Eingaberessourcen an die Pipeline gebunden wurden, ruft eine Anwendung eine Draw-Methode auf, um Primitive zu rendern. Es gibt mehrere Draw-Methoden, die in der folgenden Tabelle dargestellt werden: einige verwenden Indexpuffer, einige verwenden Instanzdaten und einige wiederverwenden Daten aus der Streaming-/Ausgabephase als Eingabe in die Eingabeassemblierungsphase.



| Zeichnen von Methoden                                                                                  | BESCHREIBUNG                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**ID3D11DeviceContext::D raw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | Zeichnen von nicht indizierten, nicht instanziierten Primitiven.                                                            |
| [**ID3D11DeviceContext::D rawInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | Zeichnen sie nicht indizierte, instanziierte Primitive.                                                                |
| [**ID3D11DeviceContext::D rawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | Zeichnen sie indizierte, nicht instanziierte Primitive.                                                                |
| [**ID3D11DeviceContext::D rawIndexedInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | Zeichnen sie indizierte, instanziierte Primitive.                                                                    |
| [**ID3D11DeviceContext::D rawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | Zeichnen Sie nicht indizierte, nicht instanziierte Primitive aus Eingabedaten, die aus der Streaming-/Ausgabephase stammen. |



 

Jede draw-Methode rendert einen einzelnen Topologietyp. Während des Renderings werden unvollständige Primitive (solche ohne ausreichende Scheitelpunkte, fehlende Indizes, partielle Primitive usw.) im Hintergrund verworfen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eingabeassembliererphase](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 