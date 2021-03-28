---
title: Optimieren von HLSL-Shadern
description: In diesem Abschnitt werden allgemeine Strategien beschrieben, mit denen Sie Ihre Shader optimieren können. Diese Strategien können auf Shader angewendet werden, die in einer beliebigen Sprache auf einer beliebigen Plattform geschrieben sind.
ms.assetid: 014b9cb3-a489-48d7-8174-b97de168bf3a
keywords:
- High-Level-Shader-Sprache
- HLSL, Leistung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06d3bb806e98e489020aa1755ef2a6c952459d86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037350"
---
# <a name="optimizing-hlsl-shaders"></a>Optimieren von HLSL-Shadern

In diesem Abschnitt werden allgemeine Strategien beschrieben, mit denen Sie Ihre Shader optimieren können. Diese Strategien können auf Shader angewendet werden, die in einer beliebigen Sprache auf einer beliebigen Plattform geschrieben sind.

-   [Informationen zum Ausführen von shaderberechnungen](#know-where-to-perform-shader-calculations)
-   [Unnötige Anweisungen überspringen](#skip-unnecessary-instructions)
-   [Paket Variablen und interpolanten](#pack-variables-and-interpolants)
-   [Reduzieren der Shader-Komplexität](#reduce-shader-complexity)
-   [Verwandte Themen](#related-topics)
-   [Zugehörige Themen](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a>Informationen zum Ausführen von shaderberechnungen

Vertexshader führen Vorgänge aus, die das Abrufen von Scheitel Punkten und das Durchführen einer Matrix Transformation für Scheitelpunkt Daten einschließen. Normalerweise werden Vertex-Shader einmal pro Scheitelpunkt ausgeführt.

Pixel-Shader führen Vorgänge aus, die das Abrufen von Textur Daten und das Durchführen von Beleuchtungsberechnungen einschließen. In der Regel werden Pixel-Shader für einen bestimmten Teil der Geometrie einmal pro Pixel ausgeführt.

In der Regel werden Pixel-Ausrichtungs Scheitel Punkte in einer Szene angezeigt, sodass Pixel-Shader häufiger als Vertex-Shader ausgeführt werden.

Beachten Sie beim Entwerfen von shaderalgorithmen Folgendes:

-   Ausführen von Berechnungen für den Vertex-Shader, wenn möglich. Eine Berechnung, die für einen PixelShader ausgeführt wird, ist wesentlich teurer als eine Berechnung, die für einen Scheitelpunkt-Shader ausgeführt wird.
-   Verwenden Sie ggf. nach Scheitelpunkt Berechnungen, um die Leistung in Situationen wie dichten Netzen zu verbessern. Bei dichten Netzen können pro-Vertex-Berechnungen Ergebnisse erzeugen, die sich visuell nicht von den Ergebnissen unterscheiden, die mit pro Pixel-Berechnungen erzeugt wurden.

## <a name="skip-unnecessary-instructions"></a>Unnötige Anweisungen überspringen

In HLSL bietet dynamische Verzweigung die Möglichkeit, die Anzahl der ausgeführten Anweisungen einzuschränken. Daher kann die dynamische Verzweigung helfen, die shaderausführungszeit zu beschleunigen. Wenn Geometrie oder Pixel nicht angezeigt werden, verwenden Sie dynamische Verzweigungen, um den Shader zu beenden oder um Anweisungen einzuschränken. Wenn z. b. ein Pixel nicht beleuchtet wird, gibt es keinen Punkt, an dem der Beleuchtungs Algorithmus ausgeführt wird.

In der folgenden Tabelle sind einige Fälle aufgeführt, in denen Sie Bedingungen im Shader testen und dynamische Verzweigungen verwenden können, um unnötige Anweisungen zu überspringen. Die Tabelle ist nicht vollständig. Vielmehr soll Sie Ihnen Ideen zur Optimierung Ihres Codes vermitteln.



| Zu überprüfen Bedingung                                    | Antwort im Shader       |
|-------------------------------------------------------|------------------------------|
| Bei der Alpha Überprüfung wird festgelegt, dass ein Pixel nicht angezeigt wird. | Überspringen Sie den Rest des Shader. |
| Das Pixel oder die Geometrie ist vollständig verstopft.                | Überspringen Sie den Rest des Shader. |
| Die Skin-Gewichtungen sind NULL.                                | Überspringen von Knochen.                  |
| Die leichte Dämpfung ist 0 (null).                            | Beleuchtung überspringen.               |
| Nicht positiver lambertian-Begriff.                         | Beleuchtung überspringen.               |



 

## <a name="pack-variables-and-interpolants"></a>Paket Variablen und interpolanten

Berücksichtigen Sie den für Shader-Daten erforderlichen Speicherplatz. Verpacken Sie so viele Informationen wie möglich in eine Variable oder interpolant. Manchmal können die Informationen aus zwei Variablen in den Speicherbereich einer einzelnen Variablen gepackt werden.

## <a name="reduce-shader-complexity"></a>Reduzieren der Shader-Komplexität

Halten Sie Ihre Shader klein und einfach. Im Allgemeinen werden Shader mit weniger Anweisungen schneller ausgeführt als Shader mit weiteren Anweisungen. Es ist auch einfacher, kleinere, weniger komplexe Shader zu Debuggen und zu optimieren.

## <a name="related-topics"></a>Verwandte Themen

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




