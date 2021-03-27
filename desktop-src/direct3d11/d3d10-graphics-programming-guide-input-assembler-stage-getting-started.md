---
title: Ersten Einstieg in die Input-Assembler Phase
description: Zum Initialisieren der Eingabe-Assembler-Phase (IA) müssen einige Schritte ausgeführt werden.
ms.assetid: 84c0ca29-2356-4b7f-98ee-ff1758edc540
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901b3facfef781e3f44acf75bee737f280dece55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390559"
---
# <a name="getting-started-with-the-input-assembler-stage"></a>Ersten Einstieg in die Input-Assembler Phase

Zum Initialisieren der Eingabe-Assembler-Phase (IA) müssen einige Schritte ausgeführt werden. Beispielsweise müssen Sie Puffer Ressourcen mit den Vertex-Daten erstellen, die von der Pipeline benötigt werden, und Sie können die IA-Phase, in der die Puffer sind, und die Art der Daten angeben, die aus den Daten zusammengestellt werden sollen.

In diesem Thema werden die grundlegenden Schritte zum Einrichten der IA-Phase beschrieben, die in der folgenden Tabelle aufgeführt sind.



| Schritt                                                                                    | BESCHREIBUNG                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Eingabepuffer erstellen](#create-input-buffers)                                           | Erstellen und initialisieren Sie Eingabepuffer mit eingegebenen Scheitelpunkt Daten.                                           |
| [Erstellen des Input-Layout Objekts](#create-the-input-layout-object)                       | Legen Sie fest, wie die Vertex-Puffer Daten mithilfe eines Input-Layout-Objekts in die IA-Phase gestreamt werden. |
| [Binden von Objekten an die Input-Assembler-Phase](#bind-objects-to-the-input-assembler-stage) | Binden Sie die erstellten Objekte (Eingabepuffer und das Eingabe Layout-Objekt) an die IA-Stufe.                 |
| [Geben Sie den primitiven Typ an.](#specify-the-primitive-type)                               | Bestimmen Sie, wie die Scheitel Punkte in primitive assembliert werden.                                          |
| [Draw-Methoden aufrufen](#call-draw-methods)                                                 | Senden Sie die Daten, die an die IA-Phase gebunden sind, über die Pipeline.                                             |



 

Nachdem Sie diese Schritte verstanden haben, fahren Sie [mit der Verwendung System-Generated Werte](d3d10-graphics-programming-guide-input-assembler-stage-using.md)fort.

## <a name="create-input-buffers"></a>Eingabepuffer erstellen

Es gibt zwei Typen von Eingabe Puffern: [Vertex-Puffer](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) und Index Puffer. Vertex-Puffer stellen Scheitelpunkt Daten für die IA-Phase bereit. Index Puffer sind optional. Sie stellen Indizes für Vertices aus dem Scheitelpunkt Puffer bereit. Sie können einen oder mehrere Vertex-Puffer und optional einen Index Puffer erstellen.

Nachdem Sie die Puffer Ressourcen erstellt haben, müssen Sie ein Eingabe Layoutobjekt erstellen, um das Datenlayout der IA-Phase zu beschreiben. Anschließend müssen Sie die Puffer Ressourcen an die IA-Phase binden. Das Erstellen und Binden von Puffern ist nicht erforderlich, wenn die Shader keine Puffer verwenden. Ein Beispiel für einen einfachen Vertex und einen PixelShader, der ein einzelnes Dreieck zeichnet, finden [Sie unter Verwenden der Input-Assembler Phase ohne Puffer](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).

Hilfe zum Erstellen eines Scheitelpunkt Puffers finden Sie unter [Erstellen eines Scheitelpunkt Puffers](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating). Hilfe zum Erstellen eines Index Puffers finden Sie unter Erstellen eines Index Puffers.

## <a name="create-the-input-layout-object"></a>Erstellen des Input-Layout Objekts

Das Input-Layout-Objekt kapselt den Eingabe Zustand der IA-Stufe. Dies schließt eine Beschreibung der Eingabedaten ein, die an die IA-Phase gebunden ist. Die Daten werden aus dem Arbeitsspeicher von einem oder mehreren Scheitel Punkten aus dem Arbeitsspeicher in die IA-Phase gestreamt. Die Beschreibung identifiziert die Eingabedaten, die von einem oder mehreren Scheitelpunkt Puffern gebunden werden, und gibt der Laufzeit die Möglichkeit, die Eingabe Datentypen mit den Eingabeparameter Typen von Shader zu überprüfen. Bei dieser Typüberprüfung wird nicht nur überprüft, ob die Typen kompatibel sind, sondern auch, dass jedes der Elemente, die der Shader benötigt, in den Puffer Ressourcen verfügbar ist.

Ein eingabelayoutobjekt wird aus einem Array von Eingabe Element Beschreibungen und einem Zeiger auf den kompilierten Shader erstellt (siehe [**ID3D11Device:: ":: samateinputlayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)"). Das Array enthält mindestens ein Eingabe Element. jedes input-Element beschreibt ein einzelnes Vertex-Data-Element aus einem einzelnen Scheitelpunkt Puffer. Der vollständige Satz der Eingabeelementbeschreibungen dient der Beschreibung aller Vertex-Datenelemente von sämtlichen Vertex-Puffern, die an die IA-Phase gebunden werden.

Die folgende layoutbeschreibung beschreibt einen einzelnen Vertex-Puffer, der drei Scheitelpunkt-Datenelemente enthält:


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



In einer Eingabe Element Beschreibung werden die einzelnen Elemente eines Scheitel Punkts in einem Vertex-Puffer, einschließlich Größe, Typ, Speicherort und Zweck, beschrieben. Jede Zeile identifiziert den Datentyp mithilfe der Semantik, des semantischen Indexes und des Datenformats. Eine [Semantik](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) ist eine Text Zeichenfolge, die angibt, wie die Daten verwendet werden. In diesem Beispiel identifiziert die erste Zeile 3-Komponenten Positionsdaten (z. b.*XYZ*). die zweite Zeile identifiziert Textur Daten mit 2 Komponenten (z. b.*UV*). und die dritte Zeile identifiziert normale Daten.

In diesem Beispiel für eine Eingabe Element Beschreibung ist der semantische Index (der zweite Parameter) für alle drei Zeilen auf 0 (null) festgelegt. Der semantische Index hilft dabei, zwischen zwei Zeilen zu unterscheiden, die dieselbe Semantik verwenden. Da in diesem Beispiel keine ähnliche Semantik vorhanden ist, kann der semantische Index auf den Standardwert 0 (null) festgelegt werden.

Der dritte Parameter ist das *Format*. Das Format (siehe [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) gibt die Anzahl der Komponenten pro Element und den-Datentyp an, der die Größe der Daten für jedes Element definiert. Das Format kann zum Zeitpunkt der Ressourcen Erstellung vollständig eingegeben werden, oder Sie können eine Ressource mit einem **DXGI- \_ Format** erstellen, das die Anzahl der Komponenten in einem Element identifiziert, der Datentyp jedoch nicht definiert ist.

### <a name="input-slots"></a>Eingabe Slots

Daten werden in der IA-Phase durch Eingaben aufgerufen, die als *Eingabe Slots* bezeichnet werden, wie in der folgenden Abbildung dargestellt. Die IA-Phase verfügt über *n* Eingabe Slots, die so konzipiert sind, dass Sie bis zu *n* Vertex-Puffer aufnehmen können, die Eingabedaten bereitstellen. Jeder Vertex-Puffer muss einem anderen Slot zugewiesen werden. Diese Informationen werden in der Eingabe Layout-Deklaration gespeichert, wenn das Eingabe Layout-Objekt erstellt wird. Sie können auch einen Offset vom Anfang jedes Puffers bis zum ersten zu lesenden Element im Puffer angeben.

![Abbildung der Eingabe Slots für die IA-Phase](images/d3d10-ia-slots.png)

Die nächsten zwei Parameter sind der *Eingabe Slot* und der *Eingabe Offset*. Wenn Sie mehrere Puffer verwenden, können Sie diese an einen oder mehrere Eingabe Slots binden. Der Eingabe Offset ist die Anzahl von Bytes zwischen dem Anfang des Puffers und dem Anfang der Daten.

### <a name="reusing-input-layout-objects"></a>Wieder verwenden von Input-Layout Objekten

Jedes Eingabe Layout-Objekt wird basierend auf einer shadersignatur erstellt. Dadurch kann die API die Input-Layout-Object-Elemente anhand der Shader-Input-Signatur überprüfen, um sicherzustellen, dass eine genaue Entsprechung von Typen und Semantik vorliegt. Sie können ein einzelnes Eingabe Layout-Objekt für viele Shader erstellen, sofern alle Shader-Eingabe Signaturen genau übereinstimmen.

## <a name="bind-objects-to-the-input-assembler-stage"></a>Binden von Objekten an die Input-Assembler-Phase

Nachdem Sie Vertex-Puffer Ressourcen und ein Eingabe Layoutobjekt erstellt haben, können Sie Sie durch Aufrufen von [**Verknüpfung id3d11devicecontext aus:: iasetvertexbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) und [**Verknüpfung id3d11devicecontext aus:: iasetinputlayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout)an die IA-Phase binden. Das folgende Beispiel zeigt die Bindung eines einzelnen Scheitelpunkt Puffers und ein Eingabe Layout-Objekt an die IA-Phase:


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



Die Bindung des Eingabe-Layoutobjekte erfordert nur einen Zeiger auf das-Objekt.

Im vorherigen Beispiel ist ein einzelner Scheitelpunkt Puffer gebunden. mehrere Vertex-Puffer können jedoch durch einen einzelnen-Befehl an [**Verknüpfung id3d11devicecontext aus:: iasetvertexbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers)gebunden werden, und der folgende Code zeigt einen solchen Aufrufs, um drei Scheitelpunkt Puffer zu binden:


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



Ein Index Puffer wird durch Aufrufen von [**Verknüpfung id3d11devicecontext aus:: iasetindexbuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer)an die IA-Phase gebunden.

## <a name="specify-the-primitive-type"></a>Geben Sie den primitiven Typ an.

Nachdem die Eingabepuffer gebunden wurden, muss der IA-Phase mitgeteilt werden, wie die Scheitel Punkte in primitive assembliert werden. Dies erfolgt durch das Angeben des [primitiven Typs](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) durch Aufrufen von [**Verknüpfung id3d11devicecontext aus:: iasetprimitivetopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); der folgende Code ruft diese Funktion auf, um die Daten als Dreiecks Liste ohne Informationen zu definieren:


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



Der Rest der primitiven Typen wird in [**D3D \_ primitive \_ Topologie**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology)aufgeführt.

## <a name="call-draw-methods"></a>Draw-Methoden aufrufen

Nachdem Eingabe Ressourcen an die Pipeline gebunden wurden, ruft eine Anwendung eine Draw-Methode auf, um primitive zu erzeugen. Es gibt mehrere Draw-Methoden, die in der folgenden Tabelle aufgeführt sind: Einige verwenden Index Puffer, einige Instanzdaten und einige Verwendungs Daten aus der Streaming-Output-Phase als Eingabe für die Eingabe-Assembler-Phase.



| Draw-Methoden                                                                                  | BESCHREIBUNG                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**Verknüpfung id3d11devicecontext aus::D RAW**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | Zeichnen Sie nicht indizierte, nicht instanzierte primitive.                                                            |
| [**Verknüpfung id3d11devicecontext aus::D rawinstanzierte**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | Zeichnen Sie nicht indizierte, instanzierte primitive.                                                                |
| [**Verknüpfung id3d11devicecontext aus::D rawindebug**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | Zeichnen Sie indizierte, nicht instanzierte primitive.                                                                |
| [**Verknüpfung id3d11devicecontext aus::D rawindexedinstangeleitet**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | Zeichnen Sie indizierte, instanzierte primitive.                                                                    |
| [**Verknüpfung id3d11devicecontext aus::D rawauto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | Zeichnen Sie nicht indizierte, nicht instanzierte primitive aus den Eingabedaten, die aus der Streaming-Output-Phase stammen. |



 

Jede Draw-Methode rendert einen einzelnen Topologietyp. Während des Renderings werden unvollständige primitive (solche ohne ausreichenden Scheitel Punkte, fehlende Indizes, partielle primitive usw.) automatisch verworfen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eingabe-Assembler-Phase](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 