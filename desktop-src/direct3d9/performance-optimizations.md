---
description: Jeder Entwickler, der Echtzeitanwendungen erstellt, die 3D-Grafiken verwenden, macht sich Gedanken über die Leistungsoptimierung. Dieser Abschnitt enthält Richtlinien zum Erzielen der besten Leistung aus Ihrem Code.
ms.assetid: 074f848e-4a42-48a2-adf7-4026b8967413
title: Leistungsoptimierungen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e22ff22e3cde3673a1fc5ccd1da1bdccd95c6a094d670f59742178b28954773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520427"
---
# <a name="performance-optimizations-direct3d-9"></a>Leistungsoptimierungen (Direct3D 9)

Jeder Entwickler, der Echtzeitanwendungen erstellt, die 3D-Grafiken verwenden, macht sich Gedanken über die Leistungsoptimierung. Dieser Abschnitt enthält Richtlinien zum Erzielen der besten Leistung aus Ihrem Code.

-   [Allgemeine leistungs Tipps](#general-performance-tips)
-   [Datenbanken und Culling](#databases-and-culling)
-   [Batchverarbeitung von Primitiven](#batching-primitives)
-   [Beleuchtung Tipps](#lighting-tips)
-   [Texturgröße](#texture-size)
-   [Matrixtransformationen](#matrix-transforms)
-   [Verwenden dynamischer Texturen](#using-dynamic-textures)
-   [Verwenden von dynamischen Scheitelpunkt- und Indexpuffern](#using-dynamic-vertex-and-index-buffers)
-   [Verwenden von Gitternetzen](#using-meshes)
-   [Z-Buffer-Leistung](#z-buffer-performance)

## <a name="general-performance-tips"></a>Allgemeine leistungs Tipps

-   Löschen Sie nur, wenn dies unbedingt der Muss ist.
-   Minimieren Sie Zustandsänderungen, und gruppieren Sie die verbleibenden Zustandsänderungen.
-   Verwenden Sie kleinere Texturen, wenn Sie dies tun können.
-   Zeichnen Sie Objekte in Ihrer Szene von vorn nach zurück.
-   Verwenden Sie Dreiecksstreifen anstelle von Listen und Lüftern. Um eine optimale Leistung des Scheitelpunktcaches zu erzielen, ordnen Sie Strips so an, dass Dreiecksvertices früher und nicht später wiederverwendet werden.
-   Beeinträchtigung von Sondereffekten, die einen unverhältnismäßig großen Anteil an Systemressourcen erfordern.
-   Testen Sie ständig die Leistung Ihrer Anwendung.
-   Minimieren von Vertexpufferschaltern.
-   Verwenden Sie nach Möglichkeit statische Scheitelpunktpuffer.
-   Verwenden Sie einen großen statischen Scheitelpunktpuffer pro FVF für statische Objekte und nicht einen pro Objekt.
-   Wenn Ihre Anwendung zufälligen Zugriff auf den Scheitelpunktpuffer im AGP-Speicher benötigt, wählen Sie eine Scheitelpunktformatgröße aus, die ein Vielfaches von 32 Bytes ist. Wählen Sie andernfalls das kleinste geeignete Format aus.
-   Zeichnen mit indizierten Primitiven. Dies kann eine effizientere Vertexzwischenspeicherung innerhalb der Hardware ermöglichen.
-   Wenn das Tiefenpufferformat einen Schablonenkanal enthält, löschen Sie immer die Tiefen- und Schablonenkanäle gleichzeitig.
-   Kombinieren Sie nach Möglichkeit die Shaderanweisung und die Datenausgabe. Beispiel:
    ```
    // Rather than doing a multiply and add, and then output the data with 
    //   two instructions:
    mad r2, r1, v0, c0
    mov oD0, r2

    // Combine both in a single instruction, because this eliminates an  
    //   additional register copy.
    mad oD0, r1, v0, c0 
    ```

    

## <a name="databases-and-culling"></a>Datenbanken und Culling

Das Erstellen einer zuverlässigen Datenbank der Objekte in Ihrer Welt ist der Schlüssel zu einer hervorragenden Leistung in Direct3D. Dies ist wichtiger als Verbesserungen bei der Rasterung oder Hardware.

Sie sollten die niedrigste Polygonanzahl beibehalten, die Sie möglicherweise verwalten können. Entwerfen Sie eine niedrige Polygonanzahl, indem Sie von Anfang an Modelle mit niedrigen Polygonen erstellen. Fügen Sie Polygone hinzu, wenn Sie dies tun können, ohne die Leistung später im Entwicklungsprozess zu beeinträchtigen. Denken Sie daran, dass die schnellsten Polygone diejenigen sind, die Sie nicht zeichnen.

## <a name="batching-primitives"></a>Batchverarbeitung von Primitiven

Um die beste Renderingleistung während der Ausführung zu erzielen, versuchen Sie, mit Primitiven in Batches zu arbeiten und die Anzahl der Renderzustandsänderungen so gering wie möglich zu halten. Wenn Sie beispielsweise über ein Objekt mit zwei Texturen verfügen, gruppieren Sie die Dreiecke, die die erste Textur verwenden, und folgen Sie ihnen mit dem erforderlichen Renderzustand, um die Textur zu ändern. Gruppieren Sie dann alle Dreiecke, die die zweite Textur verwenden. Die einfachste Hardwareunterstützung für Direct3D wird mit Batches von Renderzuständen und Batches von Primitiven über die Hardwareabstraktionsschicht (HARDWARE Abstraction Layer, NAS) aufgerufen. Je effektiver die Anweisungen in Batches ausgeführt werden, desto weniger AUFRUFE werden während der Ausführung ausgeführt.

## <a name="lighting-tips"></a>Beleuchtung Tipps

Da die Beleuchtung jedem gerenderten Frame Kosten pro Scheitelpunkt hinzufüge, können Sie die Leistung erheblich verbessern, indem Sie darauf achten, wie Sie sie in Ihrer Anwendung verwenden. Die meisten der folgenden Tipps leiten sich von der Maxime ab: "Der schnellste Code ist Code, der nie aufgerufen wird".

-   Verwenden Sie so wenige Lichtquellen wie möglich. Um die Gesamtbeleuchtung zu erhöhen, verwenden Sie beispielsweise das Umgebungslicht, anstatt eine neue Lichtquelle hinzuzufügen.
-   Richtungslichter sind effizienter als Punktlichter oder -spotlights. Bei direktionalen Beleuchtungen ist die Richtung zum Licht festgelegt und muss nicht pro Scheitelpunkt berechnet werden.
-   Spotlights können effizienter als Punktlichter sein, da der Bereich außerhalb des Lichtkegels schnell berechnet wird. Ob Spotlights effizienter sind oder nicht, hängt davon ab, wie viel ihrer Szene durch den Blickpunkt entfacht wird.
-   Verwenden Sie den Bereichsparameter, um Ihre Beleuchtung auf die Teile der Szene zu beschränken, die Sie beleuchten müssen. Alle Lichttypen werden relativ früh beendet, wenn sie außerhalb des Bereichs liegen.
-   Glanzlichter hebt fast das Doppelte der Kosten eines Lichts hervor. Verwenden Sie sie nur, wenn Sie dies benötigen. Legen Sie den \_ D3DRS SPECULARENABLE-Renderzustand nach Möglichkeit auf 0 (Standardwert) fest. Beim Definieren von Materialien müssen Sie den Glanzleistungswert auf 0 (null) festlegen, um Glanzlichter für dieses Material zu deaktivieren. Das Festlegen der Glanzfarbe auf 0,0,0 reicht nicht aus.

## <a name="texture-size"></a>Texturgröße

Die Leistung der Texturzuordnung hängt stark von der Geschwindigkeit des Arbeitsspeichers ab. Es gibt eine Reihe von Möglichkeiten, die Cacheleistung der Texturen Ihrer Anwendung zu maximieren.

-   Halten Sie die Texturen klein. Je kleiner die Texturen sind, desto höher ist die Wahrscheinlichkeit, dass sie im sekundären Cache der Haupt-CPU verwaltet werden.
-   Ändern Sie die Texturen nicht pro Primitivem. Versuchen Sie, Polygone in der Reihenfolge der verwendeten Texturen gruppiert zu halten.
-   Verwenden Sie nach Möglichkeit quadratische Texturen. Texturen mit einer Größe von 256 x 256 sind die schnellsten. Wenn Ihre Anwendung beispielsweise vier 128x128-Texturen verwendet, versuchen Sie sicherzustellen, dass sie dieselbe Palette verwenden, und platzieren Sie sie alle in einer 256x256-Textur. Diese Technik reduziert auch den Texturaustausch. Natürlich sollten Sie keine 256x256-Texturen verwenden, es sei denn, Ihre Anwendung erfordert so viel Texturierung, da Texturen, wie bereits erwähnt, so klein wie möglich gehalten werden sollten.

## <a name="matrix-transforms"></a>Matrixtransformationen

Direct3D verwendet die Welt- und Ansichtsmatrizen, die Sie zum Konfigurieren mehrerer interner Datenstrukturen festgelegt haben. Jedes Mal, wenn Sie eine neue Welt oder Ansichtsmatrix festlegen, berechnet das System die zugeordneten internen Strukturen neu. Das häufige Festlegen dieser Matrizen , z. B. Tausende Male pro Frame, ist rechenintensiv. Sie können die Anzahl der erforderlichen Berechnungen minimieren, indem Sie Ihre Welt verketten und Matrizen in einer Weltansichtsmatrix anzeigen, die Sie als Weltmatrix festlegen, und dann die Ansichtsmatrix auf die Identität festlegen. Behalten Sie zwischengespeicherte Kopien einzelner Welten bei, und zeigen Sie Matrizen an, damit Sie die Weltmatrix nach Bedarf ändern, verketten und zurücksetzen können. Aus Gründen der Übersichtlichkeit in dieser Dokumentation verwenden Direct3D-Beispiele diese Optimierung selten.

## <a name="using-dynamic-textures"></a>Verwenden dynamischer Texturen

Um herauszufinden, ob der Treiber dynamische Texturen unterstützt, überprüfen Sie das D3DCAPS2 \_ DYNAMICTEXTURES-Flag der [**D3DCAPS9-Struktur.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

Beachten Sie bei der Arbeit mit dynamischen Texturen Folgendes:

-   Sie können nicht verwaltet werden. Beispielsweise kann ihr Pool nicht D3DPOOL \_ MANAGED sein.
-   Dynamische Texturen können gesperrt werden, auch wenn sie in D3DPOOL DEFAULT erstellt \_ werden.
-   D3DLOCK \_ DISCARD ist ein gültiges Sperrflag für dynamische Texturen.

Es ist eine gute Idee, nur eine dynamische Textur pro Format und möglicherweise pro Größe zu erstellen. Dynamische Mipmaps, Cubes und Volumes werden aufgrund des zusätzlichen Mehraufwands beim Sperren jeder Ebene nicht empfohlen. Für Mipmaps ist D3DLOCK \_ DISCARD nur auf der obersten Ebene zulässig. Alle Ebenen werden verworfen, indem nur die oberste Ebene gesperrt wird. Dieses Verhalten ist für Volumes und Cubes identisch. Bei Cubes sind die oberste Ebene und das Gesicht 0 gesperrt.

Der folgende Pseudocode zeigt ein Beispiel für die Verwendung einer dynamischen Textur.


```
DrawProceduralTexture(pTex)
{
    // pTex should not be very small because overhead of 
    //   calling driver every D3DLOCK_DISCARD will not 
    //   justify the performance gain. Experimentation is encouraged.
    pTex->Lock(D3DLOCK_DISCARD);
    <Overwrite *entire* texture>
    pTex->Unlock();
    pDev->SetTexture();
    pDev->DrawPrimitive();
}
```



## <a name="using-dynamic-vertex-and-index-buffers"></a>Verwenden von dynamischen Scheitelpunkt- und Indexpuffern

Das Sperren eines statischen Scheitelpunktpuffers, während der Grafikprozessor den Puffer verwendet, kann erhebliche Leistungseinbußen zur Folge haben. Der Sperraufruf muss warten, bis der Grafikprozessor das Lesen von Scheitelpunkten oder Indexdaten aus dem Puffer abgeschlossen hat, bevor er zur aufrufenden Anwendung zurückkehren kann . Dies ist eine erhebliche Verzögerung. Das Sperren und anschließende Rendern aus einem statischen Puffer mehrmals pro Frame verhindert auch, dass der Grafikprozessor Renderingbefehle puffert, da befehle abgeschlossen werden müssen, bevor der Sperrzeiger zurückgegeben wird. Ohne gepufferte Befehle bleibt der Grafikprozessor im Leerlauf, bis die Anwendung den Scheitelpunktpuffer oder Indexpuffer auffüllt und einen Renderingbefehl aus gibt.

Im Idealfall würden sich die Scheitelpunkt- oder Indexdaten nie ändern, dies ist jedoch nicht immer möglich. Es gibt viele Situationen, in denen die Anwendung Scheitelpunkt- oder Indexdaten in jedem Frame ändern muss, möglicherweise sogar mehrmals pro Frame. In diesen Situationen sollte der Scheitelpunkt oder Indexpuffer mit D3DUSAGE DYNAMIC erstellt \_ werden. Dieses Verwendungsflag bewirkt, dass Direct3D für häufige Sperrvorgänge optimiert wird. D3DUSAGE DYNAMIC ist nur nützlich, wenn der Puffer häufig gesperrt wird. Daten, die konstant bleiben, sollten in einem statischen Scheitelpunkt oder \_ Indexpuffer platziert werden.

Um eine Leistungsverbesserung zu erzielen, wenn dynamische Scheitelpunktpuffer verwendet werden, muss die Anwendung [**IDirect3DVertexBuffer9::Lock**](/windows/desktop/api) oder [**IDirect3DIndexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) mit den entsprechenden Flags aufrufen. D3DLOCK DISCARD gibt an, dass die Anwendung die alten Scheitelpunkt- oder Indexdaten nicht \_ im Puffer behalten muss. Wenn der Grafikprozessor weiterhin den Puffer verwendet, wenn die Sperre mit D3DLOCK DISCARD aufgerufen wird, wird anstelle der alten Pufferdaten ein Zeiger auf einen neuen \_ Speicherbereich zurückgegeben. Dadurch kann der Grafikprozessor weiterhin die alten Daten verwenden, während die Anwendung Daten in den neuen Puffer platziert. In der Anwendung ist keine zusätzliche Speicherverwaltung erforderlich. Der alte Puffer wird automatisch wiederverwendet oder zerstört, wenn der Grafikprozessor damit fertig ist. Beachten Sie, dass beim Sperren eines Puffers mit D3DLOCK DISCARD immer der gesamte Puffer verworfen wird. Wenn Sie einen Offset ungleich 0 (null) oder ein Feld mit begrenzter Größe angeben, werden informationen in entsperrten Bereichen des Puffers nicht \_ beibehalten.

Es gibt Fälle, in denen die Datenmenge, die die Anwendung pro Sperre speichern muss, klein ist, z. B. das Hinzufügen von vier Scheitelsteinen zum Rendern eines Sprite. D3DLOCK NOOVERWRITE gibt an, dass die Anwendung daten, die bereits im dynamischen Puffer verwendet werden, \_ nicht überschreibt. Der Sperraufruf gibt einen Zeiger auf die alten Daten zurück, sodass die Anwendung neue Daten in nicht verwendeten Regionen des Scheitelpunkts oder Indexpuffers hinzufügen kann. Die Anwendung sollte keine Scheitelungen oder Indizes ändern, die in einem Zeichnen-Vorgang verwendet werden, da sie möglicherweise noch vom Grafikprozessor verwendet werden. Die Anwendung sollte dann D3DLOCK DISCARD verwenden, nachdem der dynamische Puffer voll ist, um einen neuen Speicherbereich zu empfangen, und die alten Scheitelpunkt- oder Indexdaten nach Abschluss des Grafikprozessors \_ verwerfen.

Der asynchrone Abfragemechanismus ist nützlich, um zu bestimmen, ob Scheiteltices noch vom Grafikprozessor verwendet werden. Geben Sie nach dem letzten DrawPrimitive-Aufruf, der die Scheitelungen verwendet, eine Abfrage vom Typ D3DQUERYTYPE \_ EVENT aus. Die Scheitelungen werden nicht mehr verwendet, wenn [**IDirect3DQuery9::GetData**](/windows/desktop/api) S \_ OK zurückgibt. Durch das Sperren eines Puffers mit D3DLOCK DISCARD oder ohne Flags wird immer sichergestellt, dass die Scheitelzeichen ordnungsgemäß mit dem Grafikprozessor synchronisiert werden. Die Verwendung der Sperre ohne Flags würde jedoch die zuvor beschriebenen Leistungsbehindungen mit sich \_ kommen. Andere API-Aufrufe wie [**IDirect3DDevice9::BeginScene,**](/windows/desktop/api) [**IDirect3DDevice9::EndScene**](/windows/desktop/api)und [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) garantieren nicht, dass der Grafikprozessor mit Scheitelgraden fertig ist.

Im Folgenden finden Sie Möglichkeiten, dynamische Puffer und die richtigen Sperrflags zu verwenden.


```
    // USAGE STYLE 1
    // Discard the entire vertex buffer and refill with thousands of vertices.
    // Might contain multiple objects and/or require multiple DrawPrimitive 
    //   calls separated by state changes, etc.
 
    // Determine the size of data to be moved into the vertex buffer.
    UINT nSizeOfData = nNumberOfVertices * m_nVertexStride;
 
    // Discard and refill the used portion of the vertex buffer.
    CONST DWORD dwLockFlags = D3DLOCK_DISCARD;
    
    // Lock the vertex buffer.
    BYTE* pBytes;
    if( FAILED( m_pVertexBuffer->Lock( 0, 0, &pBytes, dwLockFlags ) ) )
        return false;
    
    // Copy the vertices into the vertex buffer.
    memcpy( pBytes, pVertices, nSizeOfData );
    m_pVertexBuffer->Unlock();
 
    // Render the primitives.
    m_pDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, nNumberOfVertices/3)
```




```
    // USAGE STYLE 2
    // Reusing one vertex buffer for multiple objects
 
    // Determine the size of data to be moved into the vertex buffer.
    UINT nSizeOfData = nNumberOfVertices * m_nVertexStride;
 
    // No overwrite will be used if the vertices can fit into 
    //   the space remaining in the vertex buffer.
    DWORD dwLockFlags = D3DLOCK_NOOVERWRITE;
    
    // Check to see if the entire vertex buffer has been used up yet.
    if( m_nNextVertexData > m_nSizeOfVB - nSizeOfData )
    {
        // No space remains. Start over from the beginning 
        //   of the vertex buffer.
        dwLockFlags = D3DLOCK_DISCARD;
        m_nNextVertexData = 0;
    }
    
    // Lock the vertex buffer.
    BYTE* pBytes;
    if( FAILED( m_pVertexBuffer->Lock( (UINT)m_nNextVertexData, nSizeOfData, 
               &pBytes, dwLockFlags ) ) )
        return false;
    
    // Copy the vertices into the vertex buffer.
    memcpy( pBytes, pVertices, nSizeOfData );
    m_pVertexBuffer->Unlock();
 
    // Render the primitives.
    m_pDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 
               m_nNextVertexData/m_nVertexStride, nNumberOfVertices/3)
 
    // Advance to the next position in the vertex buffer.
    m_nNextVertexData += nSizeOfData;
```



## <a name="using-meshes"></a>Verwenden von Gitternetzen

Sie können Gitternetze optimieren, indem Sie indizierte Direct3D-Dreiecke anstelle indizierter Dreiecksstreifen verwenden. Die Hardware stellt fest, dass 95 Prozent der aufeinander folgenden Dreiecke tatsächlich Strips bilden und entsprechend anpassen. Viele Treiber tun dies auch für ältere Hardware.

D3DX-Gitternetzobjekte können jedes Dreieck oder Gesicht haben, das mit einem DWORD gekennzeichnet ist, das als Attribut dieses Gesichts bezeichnet wird. Die Semantik des DWORD ist benutzerdefiniert. Sie werden von D3DX verwendet, um das Gitternetz in Teilmengen zu klassifizieren. Die Anwendung legt mithilfe des [**ID3DXMesh::LockAttributeBuffer-Aufrufs Gesichtsattribute**](id3dxmesh--lockattributebuffer.md) fest. Die [**ID3DXMesh::Optimize-Methode**](id3dxmesh--optimize.md) verfügt über eine Option, um die Gitternetzvertices und -gesichter mithilfe der Option D3DXMESHOPT ATTRSORT nach Attributen \_ zu gruppen. In diesem Fall berechnet das Mesh-Objekt eine Attributtabelle, die von der Anwendung durch Aufrufen von [**ID3DXBaseMesh::GetAttributeTable abgerufen werden kann.**](id3dxbasemesh--getattributetable.md) Dieser Aufruf gibt 0 zurück, wenn das Gitternetz nicht nach Attributen sortiert ist. Eine Anwendung kann keine Attributtabelle festlegen, da sie von der **ID3DXMesh::Optimize-Methode generiert** wird. Die Attributsortierung ist datensensible. Wenn die Anwendung also weiß, dass ein Gitternetz sortiert ist, muss sie weiterhin **ID3DXMesh::Optimize** aufrufen, um die Attributtabelle zu generieren.

In den folgenden Themen werden die verschiedenen Attribute eines Gitters beschrieben.

### <a name="attribute-id"></a>Attribut-ID

Eine Attribut-ID ist ein Wert, der einer Attributgruppe eine Gruppe von Gesichtern zu ordnet. Diese ID beschreibt, welche Teilmenge der Gesichter [**ID3DXBaseMesh::D rawSubset**](id3dxbasemesh--drawsubset.md) zeichnen soll. Attribut-IDs werden für die Gesichter im Attributpuffer angegeben. Die tatsächlichen Werte der Attribut-IDs können alle Werte sein, die in 32 Bits passen. Es ist jedoch üblich, 0 bis n zu verwenden, wobei n die Anzahl von Attributen ist.

### <a name="attribute-buffer"></a>Attributpuffer

Der Attributpuffer ist ein Array von DWORDs (eins pro Gesicht), das angibt, zu welcher Attributgruppe jedes Gesicht gehört. Dieser Puffer wird bei der Erstellung eines Gitters mit 0 (null) initialisiert, wird jedoch entweder von den Auslastungsroutinen gefüllt oder muss vom Benutzer aufgefüllt werden, wenn mehr als ein Attribut mit der ID 0 gewünscht ist. Dieser Puffer enthält die Informationen, mit denen das Gitternetz basierend auf Attributen in [**ID3DXMesh::Optimize sortiert wird.**](id3dxmesh--optimize.md) Wenn keine Attributtabelle vorhanden ist, scannt [**ID3DXBaseMesh::D rawSubset**](id3dxbasemesh--drawsubset.md) diesen Puffer, um die Gesichter des angegebenen Attributs auszuwählen, das gezeichnet werden soll.

### <a name="attribute-table"></a>Attributtabelle

Die Attributtabelle ist eine Struktur, die sich im Besitz des Gitters befindet und von diesem verwaltet wird. Die einzige Möglichkeit, eine zu erstellen, besteht im Aufrufen von [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) mit aktivierter Attributsortierung oder stärkerer Optimierung. Die Attributtabelle wird verwendet, um schnell einen einzelnen primitiven Zeichnen-Aufruf von [**ID3DXBaseMesh::D rawSubset zu initiieren.**](id3dxbasemesh--drawsubset.md) Die einzige andere Verwendung besteht in der Beibehaltung dieser Struktur durch progressing meshes, sodass sie erkennen kann, welche Gesichter und Scheitelungen auf der aktuellen Detailebene aktiv sind.

## <a name="z-buffer-performance"></a>Z-Buffer-Leistung

Anwendungen können die Leistung erhöhen, wenn Z-Pufferung und Texturierung verwendet werden, indem sichergestellt wird, dass Szenen von vorn nach hinten gerendert werden. Texturierte z-gepufferte Primitive werden anhand des Z-Puffers auf Basis einer Scanzeile vorab getestet. Wenn eine Scanlinie von einem zuvor gerenderten Polygon ausgeblendet wird, lehnt das System sie schnell und effizient ab. Die Z-Pufferung kann die Leistung verbessern, aber die Technik ist am nützlichsten, wenn eine Szene die gleichen Pixel mehr als einmal zeichnet. Dies ist schwierig, genau zu berechnen, aber Sie können häufig eine enge Annäherung treffen. Wenn die gleichen Pixel weniger als zweimal gezeichnet werden, können Sie die beste Leistung erzielen, indem Sie die Z-Pufferung deaktivieren und die Szene von zurück nach vorne rendern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieren Tipps](programming-tips.md)
</dt> </dl>

 

 
