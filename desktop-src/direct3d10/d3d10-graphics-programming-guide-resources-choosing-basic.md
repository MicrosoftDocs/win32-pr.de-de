---
description: Eine Ressource ist eine Sammlung von Daten, die von der 3D-Pipeline verwendet wird.
ms.assetid: 802400fa-a606-4d3d-a61d-1cdb5a9f0437
title: Auswählen einer Ressource (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be887fb94f04783b01f8873fb61812bca20faa5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748968"
---
# <a name="choosing-a-resource-direct3d-10"></a>Auswählen einer Ressource (Direct3D 10)

Eine Ressource ist eine Sammlung von Daten, die von der 3D-Pipeline verwendet wird. Das Erstellen von Ressourcen und das Definieren Ihres Verhaltens ist der erste Schritt beim Programmieren Ihrer Anwendung. Dieses Handbuch behandelt grundlegende Themen zum Auswählen der Ressourcen, die für Ihre Anwendung erforderlich sind.

-   [Identifizieren von Pipeline Stufen, die Ressourcen benötigen](#identify-pipeline-stages-that-need-resources)
-   [Ermitteln, wie die einzelnen Ressourcen verwendet werden](#identify-how-each-resource-will-be-used)
-   [Binden von Ressourcen an Pipeline Stufen](#binding-resources-to-pipeline-stages)
-   [Zugehörige Themen](#related-topics)

## <a name="identify-pipeline-stages-that-need-resources"></a>Identifizieren von Pipeline Stufen, die Ressourcen benötigen

Der erste Schritt besteht darin, die [Pipeline Phase](d3d10-graphics-programming-guide-pipeline-stages.md) (oder die Stufen) auszuwählen, die eine Ressource verwenden werden. Das heißt, jede Phase, mit der Daten aus einer Ressource gelesen werden, sowie die Phasen, die Daten in eine Ressource schreiben, werden identifiziert. Wenn Sie die Pipeline Stufen kennen, in denen die Ressourcen verwendet werden, bestimmt die APIs, die aufgerufen werden, um die Ressource an die Stufe zu binden.

In dieser Tabelle sind die Ressourcentypen aufgeführt, die an die einzelnen Pipeline Stufen gebunden werden können. Er gibt an, ob die Ressource als Eingabe oder Ausgabe sowie als Bindungs-API gebunden werden kann.



| Pipeline Phase  | Ein/Aus | Resource               | Ressourcentyp                           | Bindungs-API                                                                                                                                                                                                |
|-----------------|--------|------------------------|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eingabe-Assembler | In     | Vertex-Puffer          | Buffer                                  | [**IASetVertexBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers)                                                                                                                                           |
| Eingabe-Assembler | In     | Indexpuffer           | Buffer                                  | [**IASetIndexBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer)                                                                                                                                               |
| Shaderphasen   | In     | Shader-ResourceView    | Buffer, Texture1D, Texture2D, Texture3D | [**Vssetshaderresources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshaderresources), [**gssetshaderresources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshaderresources), [**pssetshaderresources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshaderresources) |
| Shaderphasen   | In     | Shader-Constant Puffer | Buffer                                  | [**Vssetconstantbuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers), [**gssetconstantbuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers), [**pssetconstantbuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers) |
| Streamausgabe   | aus    | Buffer                 | Buffer                                  | [**SOSetTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-sosettargets)                                                                                                                                                       |
| Ausgabezusammenführung   | aus    | Renderzielansicht     | Buffer, Texture1D, Texture2D, Texture3D | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |
| Ausgabezusammenführung   | aus    | Ansicht "Tiefe/Schablone"     | Texture1D, Texture2D                    | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |



 

## <a name="identify-how-each-resource-will-be-used"></a>Ermitteln, wie die einzelnen Ressourcen verwendet werden

Nachdem Sie die Pipeline Stufen ausgewählt haben, die von der Anwendung verwendet werden (und damit die Ressourcen, die in den einzelnen Phasen benötigt werden), besteht der nächste Schritt darin, zu bestimmen, wie die einzelnen Ressourcen verwendet werden sollen, d. h. ob die CPU oder die GPU auf eine Ressource zugreifen kann.

Die Hardware, auf der Ihre Anwendung ausgeführt wird, hat mindestens mindestens eine CPU und eine GPU. Um einen Verwendungs Wert auszuwählen, berücksichtigen Sie den Prozessortyp, der von den folgenden Optionen gelesen oder in die Ressource geschrieben werden muss (siehe [**d3d10 \_ Usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)).



| Resource Usage | Kann aktualisiert werden von                    | Aktualisierungshäufigkeit |
|----------------|--------------------------------------|---------------------|
| Standard        | GPU                                  | selten        |
| Dynamisch        | CPU                                  | wieder          |
| Staging        | GPU                                  | –                 |
| Unveränderlich      | CPU (nur zum Zeitpunkt der Erstellung der Ressource) | –                 |



 

Die Standardverwendung sollte für eine Ressource verwendet werden, bei der erwartet wird, dass Sie von der CPU seltener aktualisiert wird (weniger als einmal pro Frame). Im Idealfall würde die CPU niemals direkt in eine Ressource mit Standardverwendung schreiben, um potenzielle Leistungseinbußen zu vermeiden.

Dynamische Verwendung sollte für eine Ressource verwendet werden, die die CPU relativ häufig (einmal oder mehr pro Frame) aktualisiert. Ein typisches Szenario für eine dynamische Ressource besteht darin, dynamische Vertex-und Index Puffer zu erstellen, die zur Laufzeit mit Daten über die Geometrie aufgefüllt werden, die aus der Sicht des Benutzers für jeden Frame sichtbar sind. Diese Puffer werden verwendet, um nur die Geometrie zu erzeugen, die für den Benutzer für diesen Frame sichtbar ist.

Die Verwendung von Staging sollte zum Kopieren von Daten in und aus anderen Ressourcen verwendet werden. Ein typisches Szenario ist das Kopieren von Daten in eine Ressource mit der Standard Auslastung (auf die die CPU nicht zugreifen kann) auf eine Ressource mit der stagingverwendung (auf die die CPU zugreifen kann).

Unveränderliche Ressourcen sollten verwendet werden, wenn sich die Daten in der Ressource nie ändern.

Eine andere Möglichkeit, dieselbe Idee zu betrachten, besteht darin, zu überprüfen, was eine Anwendung mit einer Ressource bewirkt.



| Verwendung der Ressource durch die Anwendung     | Resource Usage       |
|---------------------------------------|----------------------|
| Einmal laden und nie aktualisieren            | Unveränderlich oder Standard |
| Anwendung füllt Ressourcen wiederholt | Dynamisch              |
| In Textur Rendering                     | Standard              |
| CPU-Zugriff auf GPU-Daten                | Staging              |



 

Wenn Sie nicht sicher sind, welche Verwendung Sie auswählen, sollten Sie mit der standardmäßigen Verwendung beginnen, da es sich um den gängigsten Fall handelt. Ein Shader-Constant Puffer ist der einzige Ressourcentyp, der immer die Standardverwendung aufweisen sollte.

## <a name="binding-resources-to-pipeline-stages"></a>Binden von Ressourcen an Pipeline Stufen

Eine Ressource kann gleichzeitig an mehrere Pipeline Phasen gebunden werden, solange die beim Erstellen der Ressource angegebenen Einschränkungen ([**nutzungsflags**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**Bindungsflags**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag), [**CPU-Zugriffsflags**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)) erfüllt sind. Genauer gesagt kann eine Ressource als Eingabe und als Ausgabe gleichzeitig gebunden werden, solange das Lesen und Schreiben eines Teils einer Ressource nicht gleichzeitig erfolgen kann.

Beim Binden einer Ressource sollten Sie sich Gedanken darüber machen, wie die GPU und die CPU auf die Ressource zugreifen. Ressourcen, die für einen einzigen Zweck entwickelt wurden (verwenden Sie nicht mehrere Nutzungs-, Bindungs-und CPU-Zugriffsflags), führen zu einer besseren Leistung.

Nehmen Sie beispielsweise an, dass die Groß-/Kleinschreibung eines Renderziels mehrmals verwendet wird. Es kann schneller sein, dass zwei Ressourcen vorhanden sind: ein Renderziel und eine Textur, die als Shaderressource verwendet wird. Jede Ressource verwendet nur ein Bindungsflag ([**d3d10 \_ Bind \_ - \_ Renderziel**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) oder **d3d10 \_ Bind- \_ Shader- \_ Ressource**). Die Daten werden mithilfe von [**copyresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) oder [**copysubresourceregion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)aus der renderzieltextur in die Shader-Textur kopiert. Dies kann die Leistung verbessern, indem der Renderziel-Schreibvorgang aus dem Shader-Texture-Lesevorgang isoliert wird. Natürlich ist die einzige Möglichkeit, beide Ansätze zu implementieren und den Leistungsunterschied in ihrer jeweiligen Anwendung zu messen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



