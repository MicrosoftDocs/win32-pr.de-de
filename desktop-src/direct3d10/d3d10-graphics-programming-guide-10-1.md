---
description: Direct3D 10,1-Features
ms.assetid: e60c6116-e2f9-46b7-aed8-13e3e5ae2b90
title: Direct3D 10,1-Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99935941f60a984407c688e4ae67f0a125b0130d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338905"
---
# <a name="direct3d-101-features"></a>Direct3D 10,1-Features

Direct3D 10,1 erweitert den Featuresatz von Direct3D 10,0 durch die folgenden neuen Features:

-   Mode unabhängige Blend-Modi pro Renderziel mithilfe der neuen Blend-State-Schnittstelle (siehe [**ID3D10BlendState1-Schnittstelle**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)). Dual-Source-Mischungs Vorgänge sind auf den renderzielslot 0 beschränkt; Sie dürfen nicht in andere Ausgaben schreiben oder Renderziele an andere Slots als Slot 0 gebunden haben.
-   Kulierungsverhalten: 0 (null) Flächen werden automatisch gefiltert. Dies wirkt sich nur auf das Draht Modell-Rendering aus.
-   Gleit Komma Regeln: verwendet die gleichen IEEE-754-Regeln für Gleit Komma Zahlen, außer wenn 32-Bit-Gleit Komma Vorgänge gestrafft wurden, um ein Ergebnis innerhalb von 0,5 Unit-Last-Place (0,5 ULP) des unendlich präzisen Ergebnisses zu liefern. Dies gilt für Addition, Subtraktion und Multiplikation. (Genauigkeit bei 0,5 ULP für Multiplikation, 1,0 ULP für die gegenseitige Angabe).
-   Formate: die Genauigkeit der float16-Mischung wurde auf 0,5 ULP angehoben. Blending ist auch für UNORM16/SNORM16/SNORM8-Formate erforderlich.
-   Multisample Anti-Aliasing: multisamplinggrad wurde verbessert, um die Abdeckungs basierte Transparenz zu generalisieren und multisamplinggrad mit Multipass-Rendering effektiver zu gestalten. Um dies zu erreichen, werden alle Multisampling-Semantik so definiert, als ob der Pixelshader immer einmal pro Stichprobe (Stichproben Häufigkeit) ausgeführt wird, wobei eine separate Farbe pro Beispiel berechnet wird. Wenn ein Pixelshader keine pro-Sample-Attribute verwendet, wird derselbe Wert für jedes abgedeckte Beispiel in einem Pixel berechnet. In diesem Fall entspricht Sie der Hardware, die den Shader einmal pro Pixel (Pixelfrequenz) ausführt, und replizieren das Ergebnis an alle behandelten Stichproben. Natürlich führt die Ausführung bei Pixel Häufigkeit immer zu denselben Ergebnissen wie das Ausführen desselben Shaders bei der Stichproben Häufigkeit, wenn die Attribute mit einer Pixelfrequenz abgetastet werden. Die psinvocations-Pipeline Statistik erhöht sich bei der Stichproben Häufigkeit, es sei denn, der Shader wird mit Pixelfrequenz ausgeführt.
-   Bandbreite der Pipeline Stufe: erhöhen Sie die Datenmenge, die zwischen den shaderphasen übermittelt werden kann: 

    | Resource                        | Grenzwerte                    |
    |---------------------------------|---------------------------|
    | Register zwischen shaderphasen | 32 (32 Bit x 4-Komponente) |
    | Vertex-Shader-Eingabe Register   | 32                        |
    | Eingabe Slots für Eingabe Assembler     | 32                        |

    

     

-   Rasterisierungsregeln: die Regeln für die rasterisierung wurden für Zeilen geändert, zusätzlich wurden neue Funktionen hinzugefügt.
    -   Multisample enable wirkt sich nur auf die zeilenrasterisierung aus (Punkte und Dreiecke sind nicht betroffen) und wird zur Auswahl eines Linien Zeichnungs Algorithmus verwendet. Dies bedeutet, dass einige Multisampling-Rasterung aus Direct3D 10 nicht mehr unterstützt werden.
    -   Neue Pixel-Shader-Ausführung in der Stichproben Häufigkeit mit primitiver rasterisierung.
-   Resources: copyresource ist in zwei neuen Szenarien aktiviert:
    -   Sowohl Farb-als auch tiefe/Schablone-MSAA-Oberflächen können nun mit copyresource als Quelle oder Ziel verwendet werden.
    -   Format Konvertierung beim Kopieren zwischen bestimmten 32/64/128-Bit-vorstrukturierten, typisierten Ressourcen und komprimierten Darstellungen derselben Bitbreite.
-   Textur Stichproben-Beispiel- \_ c-und Beispiel- \_ c-LZ- \_ Anweisungen werden für die Zusammenarbeit mit Texture2DArrays und texturecubearrays definiert. verwenden Sie den Location-Member (die Alpha Komponente), um einen Array Index anzugeben.
-   Views-texturecube und das neue texturecubearray (siehe [**d3d10 \_ Texcube- \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)) sind keine tatsächlichen Ressourcen, aber es handelt sich um neue Sichten für eine Texture2DArray-Ressource. Erstellen Sie eine Ressourcen Ansicht aus einer Texture2DArray-Ressource mit einem neuen \_ \_ nutzungsflag (d3d10 Resource misc \_ texturecube), verwenden Sie die neue [**ID3D10ShaderResourceView1 Interface**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) Interface, um eine cubetextur-Ansicht an die Pipeline zu binden.

Die neuen Features erfordern einen 10,1-Gerätetyp (siehe [**ID3D10Device1 Interface**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)), der durch Aufrufen von [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1)erstellt werden kann, oder Sie können das Gerät erstellen und die Kette durch Aufrufen von [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1)gleichzeitig austauschen.

In Windows Vista Service Pack 1 sind die DLLs Direct3D 10,0 und Direct3D 10,1 nebeneinander auf dem System vorhanden. Um auf 10,1-Features zuzugreifen, führen Sie einen der folgenden Schritte aus:

## <a name="accessing-101-features-on-vista-gold-and-vista-service-pack-1"></a>Zugreifen auf 10,1-Features unter Vista Gold und Vista Service Pack 1

Entwickler, die sowohl Vista Gold als auch SP1 unterstützen möchten, müssen das Fehlen der neuen 10,1-API-Erweiterungen auf Vista Gold berücksichtigen. Sowohl dxut als auch d3dx10 bieten Hilfsfunktionen zum Erstellen des entsprechenden Geräts, basierend auf den im System verfügbaren DLLs und der verfügbaren Hardware (10,0 oder 10,1). Das 10,1-Gerät erbt vom 10,0-Gerät und kann mithilfe von QueryInterface () abgerufen werden. Es wird empfohlen, dass jede Anwendung den Gerätetyp nachverfolgt und einen Zeiger auf das 10,1-Gerät (falls verfügbar) beibehält, um häufige QueryInterface-Aufrufe zu vermeiden, wenn 10,1-Funktionen gewünscht werden. Analog dazu wird empfohlen, dass die Anwendung nachverfolgt 10,1, ob das Objekt ein 10,0-oder 10,1-Typ ist, um redundante QueryInterface ()-Aufrufe zu vermeiden. D3dx10 enthält eine Reihe von Hilfsprogrammfunktionen zur Vereinfachung dieses Prozesses (siehe [**D3DX10CreateDevice**](d3dx10createdevice.md) und [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md)).

## <a name="accessing-101-features-on-vista-service-pack-1-exclusively"></a>Ausschließlich Zugriff auf 10,1-Features unter Vista Service Pack 1

Einige Entwickler können sich dafür entscheiden, Vista Service Pack 1 zu benötigen, das umfassend an Endbenutzer verteilt wird und eine Reihe von Verbesserungen außerhalb von Direct3D 10,1 umfasst. Diese Entwickler können die Direct3D 10,1-Header und-Bibliotheken exklusiv verwenden. dabei wird eine Abhängigkeit von den Direct3D 10,1-DLLs hergestellt, die sowohl 10,0-als auch 10,1-Hardware unterstützen (bei einigen aufrufen können jedoch auf 10,0-Geräten Fehler auftreten, wenn die neue Funktionalität nicht unterstützt wird).

Einige zusätzliche Hinweise:

-   Die APIs, die im D3DX10.dll verfügbar gemacht werden, akzeptieren 10,0-und 10,1-Geräte und nutzen die Vorteile von 10,1-Funktionen, wenn Sie verfügbar sind.
-   D3D10SDKLayers.dll unterstützt ein 10,1-Gerät und kann die entsprechende Debug-spew für 10,1-Features ausgeben.
-   D3D10Ref.dll implementiert ein Software Gerät der 10,0-und 10,1-Software.
-   D3dx10 und FXC unterstützen das aktualisierte 10,1-Shader-Modell mit den folgenden Zielen: vs \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 \_ 1 und FX \_ 4 \_ 1, die an ein 10,1-Gerät gebunden werden können. Ein 10,1-Gerät unterstützt Shadermodell 4,0 und 4,1-Shader.
-   Das Direct3D 10,0 Effect-Framework unterstützt 10,0-und 10,1-Geräte. jede Technik, die Shader-Modell-4,1-Shader oder die neuen 10,1-Funktionen enthält, muss jedoch ein 10,1-Gerät verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmier Handbuch für Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



