---
title: Optimieren von HLSL-Shadern
description: In diesem Abschnitt werden allgemeine Strategien beschrieben, mit denen Sie Ihre Shader optimieren können. Sie können diese Strategien auf Shader anwenden, die in einer beliebigen Sprache und auf jeder Plattform geschrieben sind.
ms.assetid: 014b9cb3-a489-48d7-8174-b97de168bf3a
keywords:
- High-Level-Shadersprache
- HLSL, Leistung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9bc707f88fcc731146fcd3a5bbca641e6f0515a728b07af0863894d249c16a98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726140"
---
# <a name="optimizing-hlsl-shaders"></a>Optimieren von HLSL-Shadern

In diesem Abschnitt werden allgemeine Strategien beschrieben, mit denen Sie Ihre Shader optimieren können. Sie können diese Strategien auf Shader anwenden, die in einer beliebigen Sprache und auf jeder Plattform geschrieben sind.

-   [Wissen, wo Shaderberechnungen ausgeführt werden sollen](#know-where-to-perform-shader-calculations)
-   [Überspringen unnötiger Anweisungen](#skip-unnecessary-instructions)
-   [Packvariablen und Interpolanten](#pack-variables-and-interpolants)
-   [Reduzieren der Shaderkomplexität](#reduce-shader-complexity)
-   [Verwandte Themen](#related-topics)
-   [Zugehörige Themen](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a>Wissen, wo Shaderberechnungen ausgeführt werden sollen

Vertex-Shader führen Vorgänge aus, die das Abrufen von Scheitelpunkten und die Matrixtransformation von Scheitelpunktdaten umfassen. In der Regel werden Vertex-Shader einmal pro Scheitelpunkt ausgeführt.

Pixel-Shader führen Vorgänge durch, die das Abrufen von Texturdaten und das Durchführen von Beleuchtungsberechnungen umfassen. In der Regel werden Pixel-Shader einmal pro Pixel für ein bestimmtes Geometrieelement ausgeführt.

In der Regel übersteigt pixel die Anzahl der Scheitelpunkte in einer Szene, sodass Pixel-Shader häufiger ausgeführt werden als Scheitelpunkt-Shader.

Beachten Sie beim Entwerfen von Shaderalgorithmen Folgendes:

-   Führen Sie nach Möglichkeit Berechnungen für den Scheitelpunkt-Shader durch. Eine Berechnung, die für einen Pixel-Shader ausgeführt wird, ist viel teurer als eine Berechnung, die für einen Scheitelpunkt-Shader ausgeführt wird.
-   Erwägen Sie die Verwendung von Berechnungen pro Scheitelpunkt, um die Leistung in Situationen wie dichten Gitternetzen zu verbessern. Bei dichten Gitternetzen können Scheitelpunktberechnungen Ergebnisse erzeugen, die visuell nicht von Ergebnissen unterschieden werden können, die mit Pixelberechnungen erzeugt werden.

## <a name="skip-unnecessary-instructions"></a>Überspringen unnötiger Anweisungen

In HLSL bietet dynamische Verzweigung die Möglichkeit, die Anzahl der ausgeführten Anweisungen zu begrenzen. Daher kann dynamische Verzweigung dazu beitragen, die Ausführungszeit des Shaders zu beschleunigen. Wenn Geometrie oder Pixel nicht angezeigt werden, verwenden Sie dynamische Verzweigung, um den Shader zu beenden oder Anweisungen einzuschränken. Wenn z. B. ein Pixel nicht leuchtet, hat die Ausführung des Beleuchtungsalgorithmus keinen Sinn.

In der folgenden Tabelle sind einige Fälle aufgeführt, in denen Sie Bedingungen in Ihrem Shader testen und dynamische Verzweigungen verwenden können, um unnötige Anweisungen zu überspringen. Die Tabelle ist nicht vollständig. Stattdessen sollen Sie Ideen für die Optimierung Ihres Codes erhalten.



| Zu überprüfende Bedingung                                    | Antwort im Shader       |
|-------------------------------------------------------|------------------------------|
| Bei der Alphaüberprüfung wird festgestellt, dass ein Pixel nicht sichtbar ist. | Überspringen Sie den Rest des Shaders. |
| Das Pixel oder die Geometrie ist vollständig ausgereift.                | Überspringen Sie den Rest des Shaders. |
| Skingewichtungen sind 0 (null).                                | Überspringen Sie die Warteschlange.                  |
| Die lichte Dämpfung ist 0 (null).                            | Überspringt die Beleuchtung.               |
| Nicht positiver Lambertian-Begriff.                         | Überspringt die Beleuchtung.               |



 

## <a name="pack-variables-and-interpolants"></a>Packvariablen und Interpolanten

Achten Sie auf den Speicherplatz, der für Shaderdaten erforderlich ist. Packen Sie so viele Informationen wie möglich in eine Variable oder ein Interpolant. Manchmal können die Informationen aus zwei Variablen in den Arbeitsspeicher einer einzelnen Variablen gepackt werden.

## <a name="reduce-shader-complexity"></a>Reduzieren der Shaderkomplexität

Halten Sie Ihre Shader klein und einfach. Im Allgemeinen werden Shader mit weniger Anweisungen schneller ausgeführt als Shader mit mehr Anweisungen. Es ist auch einfacher, kleinere, weniger komplexe Shader zu debuggen und zu optimieren.

## <a name="related-topics"></a>Verwandte Themen

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




