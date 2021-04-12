---
description: Jeder Entwickler, der Echtzeitanwendungen erstellt, die 3D-Grafiken verwenden, beschäftigt sich mit der Leistungsoptimierung. Dieser Abschnitt enthält Richtlinien zum erzielen der besten Leistung aus Ihrem Code.
ms.assetid: 074f848e-4a42-48a2-adf7-4026b8967413
title: Leistungsoptimierungen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d42be994522f0d83e36387b1a5866b3eee10df3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480691"
---
# <a name="performance-optimizations-direct3d-9"></a>Leistungsoptimierungen (Direct3D 9)

Jeder Entwickler, der Echtzeitanwendungen erstellt, die 3D-Grafiken verwenden, beschäftigt sich mit der Leistungsoptimierung. Dieser Abschnitt enthält Richtlinien zum erzielen der besten Leistung aus Ihrem Code.

-   [Allgemeine Tipps zur Leistung](#general-performance-tips)
-   [Datenbanken und culult](#databases-and-culling)
-   [Batch Verarbeitung von primitiven](#batching-primitives)
-   [Beleuchtungs Tipps](#lighting-tips)
-   [Textur Größe](#texture-size)
-   [Matrixtransformationen](#matrix-transforms)
-   [Verwenden dynamischer Texturen](#using-dynamic-textures)
-   [Verwenden dynamischer Scheitelpunkt-und Index Puffer](#using-dynamic-vertex-and-index-buffers)
-   [Verwenden von Meshes](#using-meshes)
-   [Z-Puffer Leistung](#z-buffer-performance)

## <a name="general-performance-tips"></a>Allgemeine Tipps zur Leistung

-   Löschen Sie nur, wenn Sie müssen.
-   Minimieren Sie Zustandsänderungen, und gruppieren Sie die verbleibenden Statusänderungen.
-   Verwenden Sie kleinere Texturen, wenn dies möglich ist.
-   Zeichnen Sie Objekte in Ihrer Szene von vorne nach hinten.
-   Verwenden Sie Dreiecks Streifen anstelle von Listen und Lüfter. Um die optimale Leistung des Vertex-Caches zu erzielen, ordnen Sie für die Wiederverwendung von Dreiecks Scheitel Punkten anstelle einer späteren Verwendung von
-   Eine ordnungsgemäße Herabstufung von speziellen Effekten, die eine unverhältnismäßig große Freigabe von Systemressourcen erfordern.
-   Testen Sie ständig die Leistung Ihrer Anwendung.
-   Minimieren Sie Scheitelpunkt-Puffer Switches.
-   Verwenden Sie nach Möglichkeit statische Scheitelpunkt Puffer.
-   Verwenden Sie für statische Objekte anstelle eines Objekts pro Objekt einen großen statischen Vertex-Puffer pro f.
-   Wenn Ihre Anwendung zufälligen Zugriff auf den Vertex-Puffer im AGP-Speicher benötigt, wählen Sie eine Scheitelpunkt Format Größe aus, die ein Vielfaches von 32 Bytes ist. Wählen Sie andernfalls das kleinste geeignete Format aus.
-   Zeichnen Sie mithilfe indizierter primitiver Elemente. Dies ermöglicht eine effizientere Scheitelpunkt Zwischenspeicherung innerhalb von Hardware.
-   Wenn das tiefe Puffer Format einen Schablonen Kanal enthält, löschen Sie immer die Kanäle für Tiefe und Schablone gleichzeitig.
-   Kombinieren Sie nach Möglichkeit die Shader-Anweisung und die Datenausgabe. Beispiel:
    ```
    // Rather than doing a multiply and add, and then output the data with 
    //   two instructions:
    mad r2, r1, v0, c0
    mov oD0, r2

    // Combine both in a single instruction, because this eliminates an  
    //   additional register copy.
    mad oD0, r1, v0, c0 
    ```

    

## <a name="databases-and-culling"></a>Datenbanken und culult

Das Entwickeln einer zuverlässigen Datenbank der Objekte in ihrer Welt ist entscheidend für die ausgezeichnete Leistung in Direct3D. Es ist wichtiger als die Verbesserungen bei der rasterisierung oder Hardware.

Sie sollten die niedrigste Polygon Anzahl verwalten, die Sie möglicherweise verwalten können. Entwurf für eine niedrige Polygon Anzahl durch das Erstellen von Low-Polygon-Modellen von Anfang an. Fügen Sie ggf. Polygone hinzu, ohne die Leistung zu einem späteren Zeitpunkt im Entwicklungsprozess zu beeinträchtigen. Beachten Sie, dass es sich bei den schnellsten Polygonen um diejenigen handelt, die Sie nicht

## <a name="batching-primitives"></a>Batch Verarbeitung von primitiven

Um die beste Renderingleistung während der Ausführung zu erzielen, versuchen Sie, mit primitiven in Batches zu arbeiten und die Anzahl der renderzustandsänderungen so gering wie möglich zu halten. Wenn Sie z. b. über ein Objekt mit zwei Texturen verfügen, Gruppieren Sie die Dreiecke, die die erste Textur verwenden, und folgen Sie den notwendigen Rendering-Zuständen, um die Textur zu ändern. Gruppieren Sie dann alle Dreiecke, die die zweite Textur verwenden. Die einfachste Hardwareunterstützung für Direct3D wird mit Batches von Rendering-Zuständen und-Batches von primitiven über die Hardware Abstraktionsschicht (HAL) aufgerufen. Je effektiver die Anweisungen in einem Batch verarbeitet werden, desto weniger HAL-Aufrufe werden während der Ausführung ausgeführt.

## <a name="lighting-tips"></a>Beleuchtungs Tipps

Da mit Lichtern jedem gerenderten Frame eine pro-Vertex-Gebühr hinzugefügt wird, können Sie die Leistung erheblich verbessern, indem Sie darauf achten, wie Sie Sie in Ihrer Anwendung verwenden. Die meisten der folgenden Tipps werden von der Maxime abgeleitet: "der schnellste Code ist Code, der niemals aufgerufen wird."

-   Verwenden Sie so wenig Lichtquellen wie möglich. Um die allgemeine Beleuchtungs Stufe zu erhöhen, verwenden Sie z. b. das Ambient-Licht, anstatt eine neue Light-Quelle hinzuzufügen.
-   Direktionale Lichter sind effizienter als Punktbeleuchtung oder Scheinwerfer. Bei direktionalen Lichtern ist die Richtung des Lichts korrigiert und muss nicht pro Scheitelpunkt berechnet werden.
-   Scheinwerfer können effizienter als Punkt Leuchten sein, da der Bereich außerhalb des Licht Lichts schnell berechnet wird. Ob die Scheinwerfer effizienter sind oder nicht, hängt davon ab, wie viel Ihrer Szene durch das Spotlight beleuchtet wird.
-   Verwenden Sie den Range-Parameter, um die Lichter auf die Teile der Szene zu beschränken, die Sie beleuchten müssen. Alle hellen Typen werden relativ früh beendet, wenn Sie außerhalb des gültigen Bereichs liegen.
-   Glanzlichter heben fast den doppelten Aufwand für ein Licht. Verwenden Sie Sie nur, wenn Sie müssen. Legen Sie den D3DRS \_ specularenable-Rendering-Zustand auf 0 (Standardwert) fest, wann immer dies möglich ist. Wenn Sie Materialien definieren, müssen Sie den Glanz Wert auf NULL festlegen, um Glanzlichter für dieses Material zu deaktivieren. das Festlegen der Glanz Farbe auf 0, 0, 0 ist nicht ausreichend.

## <a name="texture-size"></a>Textur Größe

Die Leistung der Textur Zuordnung hängt stark von der Geschwindigkeit des Arbeitsspeichers ab. Es gibt eine Reihe von Möglichkeiten, die Cache Leistung der Texturen Ihrer Anwendung zu maximieren.

-   Halten Sie die Texturen klein. Die kleineren Texturen sind, umso besser die Wahrscheinlichkeit, dass Sie im sekundären Cache der Haupt-CPU gewartet werden.
-   Ändern Sie die Texturen nicht pro primitiver Basis. Versuchen Sie, Polygone in der Reihenfolge ihrer verwendeten Texturen gruppiert zu halten.
-   Verwenden Sie nach Möglichkeit quadratische Texturen. Texturen, deren Dimensionen 256 x 256 sind, sind die schnellste. Wenn Ihre Anwendung beispielsweise vier 128 x 128-Texturen verwendet, stellen Sie sicher, dass Sie dieselbe Palette verwenden, und platzieren Sie Sie alle in einer 256x256-Textur. Durch diese Vorgehensweise wird auch die Menge an Textur Austausch reduziert. Natürlich sollten Sie die Texturen von 256x256 nur dann verwenden, wenn Ihre Anwendung eine viel Texturierung erfordert, da Texturen wie bereits erwähnt so klein wie möglich gehalten werden.

## <a name="matrix-transforms"></a>Matrixtransformationen

Direct3D verwendet die Welt-und Ansichts Matrizen, die Sie zum Konfigurieren mehrerer interner Datenstrukturen festgelegt haben. Jedes Mal, wenn Sie eine neue Welt-oder Sicht Matrix festlegen, berechnet das System die zugeordneten internen Strukturen neu. Wenn Sie diese Matrizen häufig festlegen, z. b. Tausende Male pro Frame, ist dies Rechenzeit aufwändig. Sie können die Anzahl der erforderlichen Berechnungen minimieren, indem Sie Ihre Welt und Matrizen in einer World-View-Matrix verketten, die Sie als Weltmatrix festlegen, und dann die Ansichts Matrix auf die Identität festlegen. Behalten Sie zwischengespeicherte Kopien der einzelnen Welt, und zeigen Sie Matrizen an, sodass Sie die World Matrix nach Bedarf ändern, verketten und zurücksetzen können. Aus Gründen der Übersichtlichkeit in dieser Dokumentation verwenden Direct3D Samples diese Optimierung nur selten.

## <a name="using-dynamic-textures"></a>Verwenden dynamischer Texturen

Um herauszufinden, ob der Treiber dynamische Texturen unterstützt, überprüfen Sie das D3DCAPS2 \_ dynamictexturen-Flag der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur.

Beachten Sie beim Arbeiten mit dynamischen Texturen die folgenden Punkte:

-   Sie können nicht verwaltet werden. Beispielsweise kann der Pool nicht mit D3DPOOL \_ verwaltet werden.
-   Dynamische Texturen können auch dann gesperrt werden, wenn Sie in der D3DPOOL- \_ Standardeinstellung erstellt werden.
-   D3DLOCK \_ DISCARD ist ein gültiges sperrflag für dynamische Texturen.

Es empfiehlt sich, nur eine dynamische Textur Pro Format und möglicherweise pro Größe zu erstellen. Dynamische Mipmaps, Cubes und Volumes werden aufgrund des zusätzlichen Aufwands beim Sperren der einzelnen Ebenen nicht empfohlen. Für Mipmaps ist D3DLOCK \_ DISCARD nur auf der obersten Ebene zulässig. Alle Ebenen werden verworfen, indem nur die oberste Ebene gesperrt wird. Dieses Verhalten ist für Volumes und Cubes identisch. Bei Cubes werden die oberste Ebene und die Vorderseite 0 gesperrt.

Der folgende Pseudo Code zeigt ein Beispiel für die Verwendung einer dynamischen Textur.


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



## <a name="using-dynamic-vertex-and-index-buffers"></a>Verwenden dynamischer Scheitelpunkt-und Index Puffer

Wenn Sie einen statischen Vertex-Puffer sperren, während der-Grafikprozessor den Puffer verwendet, kann dies zu einer erheblichen Leistungs Einbuße werden. Der Sperr Aufruf muss warten, bis der Grafikprozessor das Lesen von Vertex-oder Indexdaten aus dem Puffer abgeschlossen hat, bevor er an die aufrufende Anwendung zurückgegeben werden kann, eine beträchtliche Verzögerung. Das Sperren und anschließende Rendering von einem statischen Puffer mehrmals pro Frame verhindert außerdem, dass der Grafikprozessor renderingbefehle puffert, da er vor dem Zurückgeben des Sperr Zeigers Befehle beenden muss. Ohne gepufferte Befehle bleibt der Grafikprozessor im Leerlauf, bis die Anwendung den Vertex-Puffer oder Index Puffer füllt und einen Renderingbefehl ausgibt.

Im Idealfall würden die Scheitelpunkt-oder Indexdaten nie geändert werden, dies ist jedoch nicht immer möglich. Es gibt viele Situationen, in denen die Anwendung Scheitel Punkte oder Indexdaten jedes Frames ändern muss, vielleicht sogar mehrmals pro Frame. In diesen Fällen sollte der Scheitelpunkt oder Index Puffer mit D3DUSAGE Dynamic erstellt werden \_ . Dieses nutzungsflag bewirkt, dass Direct3D bei häufigen Sperr Vorgängen optimiert wird. D3DUSAGE \_ Dynamic ist nur nützlich, wenn der Puffer häufig gesperrt ist. Daten, die konstant bleiben, sollten in einem statischen Scheitelpunkt oder Index Puffer abgelegt werden.

Um eine Leistungsverbesserung bei der Verwendung dynamischer Scheitelpunkt Puffer zu erhalten, muss die Anwendung [**IDirect3DVertexBuffer9:: Lock**](/windows/desktop/api) oder [**IDirect3DIndexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) mit den entsprechenden Flags aufzurufen. D3DLOCK \_ DISCARD gibt an, dass die Anwendung die alten Scheitelpunkt-oder Indexdaten nicht im Puffer aufbewahren muss. Wenn der Grafikprozessor den Puffer weiterhin verwendet, wenn die Sperre mit D3DLOCK DISCARD aufgerufen wird \_ , wird anstelle der alten Puffer Daten ein Zeiger auf einen neuen Speicherbereich zurückgegeben. Dies ermöglicht es dem Grafikprozessor, die alten Daten weiterhin zu verwenden, während die Anwendung Daten im neuen Puffer platziert. In der Anwendung ist keine zusätzliche Speicherverwaltung erforderlich. der alte Puffer wird wieder verwendet oder automatisch zerstört, wenn der Grafikprozessor damit fertig ist. Beachten Sie, dass beim Sperren eines Puffers mit D3DLOCK \_ verwerfen immer der gesamte Puffer verworfen wird, wobei ein Offset ungleich 0 (null) oder ein Feld mit eingeschränkter Größe keine Informationen in entsperrungs Bereichen des Puffers beibehält

Es gibt Fälle, in denen die Menge der Daten, die die Anwendung für die Speicherung pro Sperre benötigt, klein ist, z. b. das Hinzufügen von vier Scheitel Punkten zum Rendering D3DLOCK \_ noüberschreibung gibt an, dass die Anwendung keine Daten überschreibt, die bereits im dynamischen Puffer verwendet werden. Der Lock-Befehl gibt einen Zeiger auf die alten Daten zurück, sodass die Anwendung neue Daten in nicht verwendeten Regionen des Scheitel Punkts oder Index Puffers hinzufügen kann. Die Anwendung sollte Scheitel Punkte oder Indizes, die in einem zeichnen-Vorgang verwendet werden, nicht ändern, da Sie möglicherweise noch von dem Grafikprozessor verwendet werden. Die Anwendung sollte dann D3DLOCK \_ verwerfen verwenden, nachdem der dynamische Puffer voll ist, um einen neuen Speicherbereich zu erhalten, wobei die alten Scheitelpunkt-oder Indexdaten nach Abschluss des Grafikprozessors verworfen werden.

Der asynchrone Abfrage Mechanismus ist hilfreich, um zu bestimmen, ob Scheitel Punkte weiterhin vom Grafikprozessor verwendet werden. Geben Sie \_ nach dem letzten drawprimitiven-Befehl, der die Scheitel Punkte verwendet, eine Abfrage vom Typ D3DQUERYTYPE-Ereignis aus. Die Scheitel Punkte werden nicht mehr verwendet, wenn [**IDirect3DQuery9:: GetData**](/windows/desktop/api) S \_ OK zurückgibt. Wenn Sie einen Puffer mit D3DLOCK \_ verwerfen oder ohne Flags sperren, gewährleisten Sie immer, dass die Scheitel Punkte ordnungsgemäß mit dem Grafikprozessor synchronisiert werden. die Verwendung von Lock ohne Flags führt jedoch zu der zuvor beschriebenen Leistungs Einbuße. Andere API-Aufrufe wie [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api), [**IDirect3DDevice9:: EndScene**](/windows/desktop/api)und [**IDirect3DDevice9::P Resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) garantieren nicht, dass der Grafikprozessor die Verwendung von Vertices abgeschlossen hat.

Im folgenden finden Sie Möglichkeiten, dynamische Puffer und die richtigen Sperrflags zu verwenden.


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



## <a name="using-meshes"></a>Verwenden von Meshes

Sie können die Netzen mithilfe von Direct3D-indizierten Dreiecken anstelle von indizierten Dreiecks Streifen optimieren. Die Hardware erkennt, dass 95 Prozent der aufeinander folgenden Dreiecke tatsächlich zu einem Streifen und entsprechend angepasst werden. Viele Treiber führen dies auch für ältere Hardware aus.

D3DX Mesh-Objekte können jedes Dreieck oder Gesicht aufweisen, das mit einem DWORD-Attribut gekennzeichnet ist, das als Attribut dieses Gesichts bezeichnet wird. Die Semantik des DWORD ist Benutzer definiert. Sie werden von D3DX verwendet, um das Mesh in Teilmengen zu klassifizieren. Die Anwendung legt mit dem [**ID3DXMesh:: LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md) -Befehl spezifische Attribute fest. Die [**ID3DXMesh:: optimiert**](id3dxmesh--optimize.md) -Methode verfügt über eine Option zum Gruppieren der messcheitel Punkte und Gesichter von Attributen mithilfe der D3DXMESHOPT \_ attrsort-Option. Wenn dies geschehen ist, berechnet das Mesh-Objekt eine Attribut Tabelle, die von der Anwendung durch Aufrufen von [**ID3DXBaseMesh:: GetAttributeTable**](id3dxbasemesh--getattributetable.md)abgerufen werden kann. Dieser Befehl gibt 0 (null) zurück, wenn das Mesh nicht nach Attributen sortiert ist. Es gibt keine Möglichkeit für eine Anwendung, eine Attribut Tabelle festzulegen, da Sie von der **ID3DXMesh:: optimiert** -Methode generiert wird. Die Attribut Sortierung ist Daten sensibel. wenn die Anwendung also weiß, dass ein Mesh Attribut sortiert ist, muss dennoch **ID3DXMesh:: optimiert** aufgerufen werden, um die Attribut Tabelle zu generieren.

In den folgenden Themen werden die verschiedenen Attribute eines Mesh beschrieben.

### <a name="attribute-id"></a>Attribut-ID

Eine Attribut-ID ist ein Wert, der eine Gruppe von Gesichtern einer Attribut Gruppe zuordnet. Diese ID beschreibt, welche Teilmenge von Gesichter [**ID3DXBaseMesh::D rawsubset**](id3dxbasemesh--drawsubset.md) zeichnen soll. Attribut-IDs werden für die Gesichter im Attribut Puffer angegeben. Die tatsächlichen Werte der Attribut-IDs können alles sein, was in 32 Bits passt, aber es ist üblich, 0 bis n zu verwenden, wobei n die Anzahl der Attribute ist.

### <a name="attribute-buffer"></a>Attribut Puffer

Der Attribut Puffer ist ein Array von DWords (eins pro Gesicht), das angibt, zu welcher Attribut Gruppe die einzelnen Gesichter gehören. Dieser Puffer wird bei der Erstellung eines Mesh mit 0 (null) initialisiert, wird jedoch entweder von den Lade Routinen ausgefüllt oder muss vom Benutzer ausgefüllt werden, wenn mehr als ein Attribut mit der ID 0 gewünscht wird. Dieser Puffer enthält die Informationen, die zum Sortieren des Netzes auf der Grundlage von Attributen in [**ID3DXMesh:: optimiert**](id3dxmesh--optimize.md)verwendet werden. Wenn keine Attribut Tabelle vorhanden ist, scannt [**ID3DXBaseMesh::D rawsubset**](id3dxbasemesh--drawsubset.md) den Puffer, um die Gesichter des zu zeichnenden Attributs auszuwählen.

### <a name="attribute-table"></a>Attribut Tabelle

Bei der Attribut Tabelle handelt es sich um eine Struktur im Besitz des Netzes. Die einzige Möglichkeit für die Generierung ist das Aufrufen von [**ID3DXMesh::**](id3dxmesh--optimize.md) Optimization mit aktivierter Attribut Sortierung oder stärkerer Optimierung. Die Attribut Tabelle wird verwendet, um schnell einen einzelnen zeichnen-primitiven Aufrufen von [**ID3DXBaseMesh::D rawsubset**](id3dxbasemesh--drawsubset.md)zu initiieren. Der einzige andere Verwendungszweck besteht darin, dass fortlaufende Netze auch diese Struktur beibehalten, sodass Sie sehen können, welche Gesichter und Scheitel Punkte auf der aktuellen Detailebene aktiv sind.

## <a name="z-buffer-performance"></a>Z-Puffer Leistung

Anwendungen können die Leistung bei Verwendung von z-Pufferung und Texturierung steigern, indem Sie sicherstellen, dass Szenen von vorne nach hinten gerendert werden. Strukturierte z-gepufferte primitive werden für den z-Puffer auf der Basis der Scan Linie vorgetestet. Wenn eine Scanzeile von einem zuvor gerenderten Polygon ausgeblendet wird, lehnt das System Sie schnell und effizient ab. Z-Pufferung kann die Leistung verbessern, aber das Verfahren ist besonders nützlich, wenn eine Szene die gleichen Pixel mehrmals zeichnet. Dies ist schwierig zu berechnen, aber Sie können oft eine genaue Näherung treffen. Wenn die gleichen Pixel weniger als zweimal gezeichnet werden, können Sie die beste Leistung erzielen, indem Sie z-bufferoff deaktivieren und die Szene von hinten wieder in den Vordergrund rendern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmiertipps](programming-tips.md)
</dt> </dl>

 

 
