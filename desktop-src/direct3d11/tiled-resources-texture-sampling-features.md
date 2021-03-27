---
title: Funktionen für Textur Stichproben der Kachel Ressourcen
description: In diesem Abschnitt werden die Funktionen für Textur Stichproben von Kacheln beschrieben
ms.assetid: E56737CE-C468-4D3C-84EE-E8EB2AB6F505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd46c96219e54aea6990e91de8e340fdca5e32b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728728"
---
# <a name="tiled-resources-texture-sampling-features"></a>Funktionen für Textur Stichproben der Kachel Ressourcen

In diesem Abschnitt werden die Funktionen für Textur Stichproben von Kacheln beschrieben

## <a name="requirements-of-tiled-resources-texture-sampling-features"></a>Anforderungen an die Textur-Sampling-Features der Kachel Ressourcen

Die hier beschriebenen Funktionen für die Textur Stichproben erfordern die Unterstützung von untergeordneten Elementen der Ebene [2](tier-2.md) .

## <a name="shader-feedback-about-mapped-areas"></a>Shader-Feedback zu zugeordneten Bereichen

Jede shaderanweisung, die eine gekachelte Ressource liest und/oder schreibt, bewirkt, dass Statusinformationen aufgezeichnet werden. Dieser Status wird als optionaler zusätzlicher Rückgabewert für jede Ressourcen Zugriffs Anweisung verfügbar gemacht, die in ein Temp-32-Bit-Register übergeht. Der Inhalt des Rückgabewerts ist nicht transparent. Das heißt, das direkte Lesen durch das Shader-Programm ist nicht zulässig. Sie können jedoch die [**checkaccessfullymapping**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) -Funktion verwenden, um die Statusinformationen zu extrahieren.

## <a name="fully-mapped-check"></a>Vollständige Zuordnung überprüfen

Die [**checkaccessfullymapping**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) -Funktion interpretiert den von einem Speicherzugriff zurückgegebenen Status und gibt an, ob alle Daten, auf die zugegriffen wird, in der Ressource zugeordnet wurden. **Checkaccessfullymapping** gibt true (0xFFFFFFFF) zurück, wenn Daten zugeordnet wurden, oder false (0x00000000), wenn die Daten nicht zugeordnet wurden.

Bei Filter Vorgängen ist die Gewichtung eines bestimmten Texttyps manchmal 0,0. Ein Beispiel hierfür ist ein lineares Beispiel mit Texturkoordinaten, die sich direkt in einem texturcenter befinden: 3 andere texeln (die von der Hardware abweichen können) tragen zum Filter bei, aber mit 0 Gewichtung. Diese 0-Gewichtungs texeln tragen überhaupt nicht zum Filterergebnis bei. Wenn Sie also auf **null** -Kacheln fallen, werden Sie nicht als nicht zugeordneter Zugriff gezählt. Beachten Sie, dass die gleiche Garantie für Textur Filter gilt, die mehrere MIP-Ebenen einschließen. Wenn die texeln in einer der Mipmaps nicht zugeordnet sind, aber die Gewichtung für diese texeln gleich 0 ist, werden diese texeln nicht als nicht zugeordneter Zugriff gezählt.

Wenn die Stichprobenentnahme von einem Format mit weniger als 4 Komponenten (z. b. DXGI- \_ Format \_ R8 \_ unorm) erfolgt, führen alle texeln, die auf **null** -Kacheln fallen, dazu, dass ein **null** zugeordneter Zugriff gemeldet wird, unabhängig davon, welche Komponenten der Shader tatsächlich im Ergebnis untersucht. Beispielsweise scheint das Lesen aus dem R8 \_ -unorm und das Maskieren des Lese Ergebnisses im Shader mit. GBA/. yzw die Textur überhaupt nicht zu lesen. Wenn die textrece jedoch eine **null** zugeordnete Kachel ist, wird der Vorgang weiterhin als **null** -Zuordnungs Zugriff gezählt.

Der Shader kann den Status überprüfen und jede gewünschte Vorgehensweise bei einem Fehler verfolgen. Eine Vorgehensweise kann z. b. "Fehler" protokollieren (z. b. über den UAV-Schreibvorgang) und/oder einen anderen Lesevorgang an eine gröbere-Lod ausgeben, die bekanntermaßen zugeordnet ist. Eine Anwendung kann auch erfolgreiche Zugriffe nachverfolgen, um einen Eindruck davon zu erhalten, auf welchen Teil des zugeordneten Satzes von Kacheln zugegriffen wurde.

Eine Komplikation für die Protokollierung besteht darin, dass kein Mechanismus vorhanden ist, mit dem der genaue Satz von Kacheln gemeldet werden kann Die Anwendung kann konservative Schätzwerte auf der Grundlage der für den Zugriff verwendeten Koordinaten und mithilfe der Lod-Anweisung (z. b. [**tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)), die die Berechnung der Hardware-Lod zurückgibt, durchführen.

Eine weitere Komplikation ist, dass viele Zugriffe auf die gleichen Kacheln erfolgen, sodass eine Menge redundanter Protokollierung und möglicherweise Konflikte im Speicher stattfindet. Es kann praktisch sein, wenn der Hardware die Möglichkeit eingeräumt wird, sich nicht auf den Zugriff auf Berichts Kacheln zu kümmern, wenn Sie an anderer Stelle als gemeldet wurden. Möglicherweise könnte der Status einer solchen Nachverfolgung von der API zurückgesetzt werden (wahrscheinlich an Frame Grenzen).

## <a name="per-sample-minlod-clamp"></a>Minlod-Klammer pro Stichprobe

Um Shader bei der Vermeidung von Bereichen in falsch zugeordneten Kacheln zu unterstützen, die bekanntermaßen nicht zugeordnet sind, haben die meisten shaderanweisungen mit einem Sampler (Filterung) einen neuen Modus, der es dem Shader ermöglicht, einen zusätzlichen float32 minlod-Klammer Parameter an das Textur Beispiel zu übergeben. Dieser Wert befindet sich im Gegensatz zur zugrunde liegenden Ressource im MipMap-Nummernbereich der Ansicht.

Die Hardware führt [**Max**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-max)("f", "f", "f") am gleichen Speicherort wie die Lod-Berechnung aus, bei der die ressourcenbasierte minlod-Klammer auftritt. Dies ist auch ein **Maximum**().

Wenn das Ergebnis der Anwendung der Lod-Klammer pro Stichprobe und sämtlicher anderer im Sampler definierter Lod-Klammern eine leere Menge ist, ist das Ergebnis das gleiche out-of-Limit-Zugriffs Ergebnis wie die pro-Ressource-minlod-Klammer: 0 für Komponenten im Oberflächen Format und Standardwerte für fehlende Komponenten.

Die Lod-Anweisung (z. b. [**tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)), in der die hier beschriebene minlod-Klammer für Samplingwerte vorausgeht, gibt sowohl eine angehaltene und ungebundene Lod zurück. Die von dieser Lod-Anweisung zurückgegebene gebundene Lod spiegelt alle Klammern wider, einschließlich der pro-Ressource-Klammer, aber keine pro-Stichproben-Klammer. Die pro-Stichproben-Klammer wird gesteuert und wird vom Shader trotzdem bekannt, sodass der Shader-Autor diese Klammer bei Bedarf manuell auf den Rückgabewert der Lod-Anweisung anwenden kann.

## <a name="minmax-reduction-filtering"></a>Minimale/maximale Reduzierungs Filterung

Anwendungen können Ihre eigenen Datenstrukturen verwalten, die Sie über das Aussehen der Zuordnungen für eine gekachelte Ressource informieren. Ein Beispiel wäre eine Oberfläche, die ein Texel enthält, das Informationen für jede Kachel in einer gekachelten Ressource enthalten soll. Eine kann die erste Lod speichern, die an einem bestimmten Kachel Speicherort zugeordnet ist. Durch die sorgfältige Stichprobenentnahme dieser Datenstruktur auf die gleiche Weise, wie die gekachelte Ressource als Stichprobe verwendet werden soll, kann man ermitteln, was die minimale Lod ist, die für einen vollständigen Textur Filter vollständig zugeordnet ist. Um diesen Prozess zu vereinfachen, bietet Direct3D 11,2 einen neuen allgemeinen Samplingmodus, Min/Max-Filterung.

Das Hilfsprogramm der Min/Max-Filterung für die Lod-Nachverfolgung kann für andere Zwecke nützlich sein, z. b. das Filtern von tiefen Oberflächen.

Die minimale/maximale Reduzierungs Filterung ist ein Modus für Samplern, der denselben textursatz abruft, der von einem normalen Textur Filter abgerufen wird. Anstatt jedoch die Werte zu mischen, um eine Antwort zu erhalten, gibt Sie die minimale () oder die maximale Anzahl () der texeln zurück, die pro Komponente abgerufen werden (z. b. die minimale Anzahl aller R-Werte, getrennt von der Summe aller G-Werte usw.).

Die Min/Max-Vorgänge folgen den Regeln für die arithmetische Genauigkeit Direct3D. Die Reihenfolge der Vergleiche spielt keine Rolle.

Bei Filter Vorgängen, bei denen es sich nicht um min/max handelt, ist die Gewichtung eines bestimmten Texttyps manchmal 0,0. Ein Beispiel hierfür ist ein lineares Beispiel mit Texturkoordinaten, die sich direkt in einem Texel-Center-3 anderen texeln (bei denen Sie je nach Hardware variieren können) zu dem Filter beitragen, aber mit 0 (null). Bei allen diesen texeln, bei denen es sich um 0 (null) bei einem nicht-Min/Max-Filter handeln würde, tragen diese textteln nach wie vor nicht zum Ergebnis bei, und die Gewichtungen wirken sich nicht auf den Min/Max-Filter Vorgang aus.

Die vollständige Liste der Filtermodi wird in der [**D3D11 \_ Filter**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter) -Enumeration mit dem Minimalwert und dem Maximum in den Enumerationswerten angezeigt.

Die Unterstützung für dieses Feature hängt von der Unterstützung der [Ebene 2](tier-2.md) für gekachelte Ressourcen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pipeline Zugriff auf gekachelte Ressourcen](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 