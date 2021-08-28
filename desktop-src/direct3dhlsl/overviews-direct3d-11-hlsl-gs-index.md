---
title: Indizierung mehrerer Ausgabe Streams
description: In Shadermodell 5 kann ein Geometrie-Shader bis zu vier separate Streams unterstützen. Dies bedeutet, dass ein einzelner Shader abhängig von der Anzahl der deklarierten Streams zwischen einem und vier Ausgabestreams ausgeben kann.
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37aefd8b7cdcab05515bda6f81fa6c679751dc95
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473396"
---
# <a name="how-to-index-multiple-output-streams"></a>Vorgehensweise: Indizierung mehrerer Ausgabe Streams

In Shadermodell 5 kann ein Geometrie-Shader bis zu vier separate Streams unterstützen. Dies bedeutet, dass ein einzelner Shader abhängig von der Anzahl der deklarierten Streams zwischen einem und vier Ausgabestreams ausgeben kann.

So indizen Sie mehrere Ausgabestreams

1.  Definieren Sie einen Datenstrom mithilfe eines Streamvorlagentyps.

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  Definieren Sie einen zweiten Datenstrom mithilfe eines Streamvorlagentyps.

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  Ausgeben von Daten in (oder beide) Streams mithilfe der systeminternen Funktionen des Streamausgabeobjekts (z. B. Append oder RestartStrip).

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

    

Wenn Sie einen einzelnen Ausgabestream verwenden, können Sie Dreiecksstreifen, Linienstrips oder Punktlisten ausgeben. Wenn Sie Dreiecks- und Linienstreifen im Stream-Out-Puffer speichern, werden sie auf Dreiecks- bzw. Linienlisten erweitert. Sie können auch einen Datenstrom rastern und nicht an einen Speicherpuffer senden.

Bei Verwendung mehrerer Ausgabestreams müssen alle Datenströme Punkte enthalten, und bis zu einem Ausgabestream kann an den Rasterizer gesendet werden. In der Regel rastert eine Anwendung keinen Stream.

Nachdem Sie Daten in einen Puffer gestreamt haben, können Sie diese Daten verwenden, um jeden primitiven Typ zu rendern, nicht nur den primitiven Typ, den Sie zum Füllen des Puffers verwendet haben.

Die Gesamtausgabe des geometry-Shaders ist auf 1024 Skalar begrenzt. Wenn mehrere Datenströme vorhanden sind, wird die Anzahl der Skalarwerte aus dem größten Streamtyp multipliziert mit der maximalen Scheitelpunktanzahl berechnet.




| | | Unterschiede zwischen Shadermodell 4 und Shadermodell 5:<br /> Shadermodell 4:<br /><ul><li>Die maximale Anzahl von Skalaren für die Streamausgabe beträgt 64.</li><li>Die Pro-Komponenten-Registermaske muss im gesamten Indexbereich übereinstimmen.</li></ul>Shadermodell 5:<br /><ul><li>Die maximale Anzahl von Skalaren für die Streamausgabe beträgt 128.</li><li>Die Registermaske pro Komponente muss nicht über den gesamten Indexbereich hinweg übereinstimmen.</li><li>Die dynamische Indizierung von Ausgaben muss für alle Streams zulässig sein.</li><li>Interpolationsmodi müssen für die Streams nicht übereinstimmen.</li></ul> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geometry Shader-Features](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 





