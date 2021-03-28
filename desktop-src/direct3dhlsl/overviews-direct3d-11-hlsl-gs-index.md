---
title: Indizieren mehrerer Ausgabedaten Ströme
description: In Shader Model 5 kann ein Geometry-Shader bis zu 4 separate Streams unterstützen. Dies bedeutet, dass ein einzelner Shader abhängig von der Anzahl der deklarierten Streams zwischen einem und vier Ausgabestreams ausgeben kann.
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8564917be9565e862043e370840f8ac7280f174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036435"
---
# <a name="how-to-index-multiple-output-streams"></a>Vorgehensweise: Indizieren mehrerer Ausgabedaten Ströme

In Shader Model 5 kann ein Geometry-Shader bis zu 4 separate Streams unterstützen. Dies bedeutet, dass ein einzelner Shader abhängig von der Anzahl der deklarierten Streams zwischen einem und vier Ausgabestreams ausgeben kann.

So indizieren Sie mehrere Ausgabedaten Ströme

1.  Definieren Sie einen Datenstrom mithilfe eines Datenstrom-Vorlagen Typs.

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  Definieren Sie einen zweiten Datenstrom mithilfe eines Stream-Vorlagen Typs.

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  Ausgabedaten an Datenströme (oder beides) mithilfe der systeminternen Funktionen des Stream-Ausgabe Objekts (z. b. Append oder restartstrip).

    ```
    void MyGS( 
        InVertex verts[2], 
        inout PointStream<OutVertex1> myStream1, 
        inout PointStream<OutVertex2> myStream2 )
    {
        OutVertex1 myVert1 = TransformVertex1( verts[0] );
        OutVertex2 myVert2 = TransformVertex2( verts[1] );
        myStream1.Append( myVert1 );
        myStream2.Append( myVert2 );
    }
    ```

    

Wenn Sie einen einzelnen Ausgabestream verwenden, können Sie Dreiecks Streifen, Zeilen Streifen oder Punkt Listen ausgeben. Wenn Sie Dreieck-und Zeilen Streifen im Stream-out-Puffer speichern, werden Sie auf Dreieck-bzw. Zeilen Listen erweitert. Sie können auch einen Datenstrom Rasterisieren und ihn nicht an einen Arbeitsspeicher Puffer senden.

Bei der Verwendung mehrerer Ausgabedaten Ströme müssen alle Streams Punkte enthalten, und es kann bis zu einem Ausgabedatenstrom an den Rasterizer gesendet werden. Üblicherweise wird ein beliebiger Stream von einer Anwendung nicht rasterisiert.

Nachdem Sie Daten in einen Puffer gestreamt haben, können Sie diese Daten verwenden, um jeden primitiven Typ zu erzeugen, nicht nur den primitiven Typ, den Sie zum Ausfüllen des Puffers verwendet haben.

Die Gesamtausgabe des Geometry-Shaders ist auf 1024 skalare beschränkt. Wenn mehrere Streams vorhanden sind, wird die Anzahl der skalare aus dem größten Streamtyp multipliziert mit der maximalen Vertex-Anzahl berechnet.



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Shader-Modell 4 und Shader-Modell 5:<br/> Shadermodell 4:<br/>
<ul>
<li>Die maximale Anzahl von skalaren für die Streamausgabe beträgt 64.</li>
<li>Die Registrierungs Maske pro Komponente muss über den Index Bereich abgestimmt werden.</li>
</ul>
Shader-Modell 5:<br/>
<ul>
<li>Die maximale Anzahl von skalaren für die Streamausgabe beträgt 128.</li>
<li>Die Registrierungs Maske pro Komponente muss nicht über den Index Bereich abgestimmt werden.</li>
<li>Die dynamische Indizierung von Ausgaben muss für alle Streams rechtmäßig sein.</li>
<li>Der Interpolations Modus muss für die Streams nicht abgeglichen werden.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geometry-Shaderfunktionen](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 





