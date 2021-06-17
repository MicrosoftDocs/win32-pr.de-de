---
description: Erfahren Sie mehr über das Rendern eines Effekts für Direct3D 10. Ein Effekt kann verwendet werden, um Informationen zu speichern oder mit einer Gruppe von Status zu rendern.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Rendern eines Effekts (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79db595585c6587648fba12afa5fbb22ff33e845
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262572"
---
# <a name="rendering-an-effect-direct3d-10"></a>Rendern eines Effekts (Direct3D 10)

Ein Effekt kann verwendet werden, um Informationen zu speichern oder mit einer Gruppe von Status zu rendern. Jede Technik gibt Vertex-Shader, Geometrie-Shader, Pixel-Shader, Shaderzustand, Sampler- und Texturzustand und anderen Pipelinezustand an. Nachdem Sie den Zustand in einem Effekt organisiert haben, können Sie den Renderingeffekt, der sich aus diesem Zustand ergibt, kapseln, indem Sie den Effekt erstellen und rendern.

Es gibt einige Schritte zum Vorbereiten eines Effekts für das Rendering. Die erste ist die Kompilierung, bei der HLSL wie Code mit der HLSL-Sprachsyntax und den Auswirkungsframeworkregeln überprüft wird. Sie können einen Effekt aus Ihrer Anwendung mithilfe von API-Aufrufen kompilieren, oder Sie können einen Effekt offline mithilfe des Effektcompiler-Hilfsprogramms kompilieren. Nachdem Der Effekt erfolgreich kompiliert wurde, erstellen Sie ihn, indem Sie einen anderen (aber sehr ähnlichen) Satz von APIs aufrufen.

Nachdem der Effekt erstellt wurde, gibt es zwei verbleibende Schritte für die Verwendung. Zunächst müssen Sie die Effektzustandswerte (die Werte der Effektvariablen) mithilfe einer Reihe von Methoden zum Festlegen des Zustands initialisieren. Bei einigen Variablen kann dies einmal erfolgen, wenn ein Effekt erstellt wird. andere müssen jedes Mal aktualisiert werden, wenn ihre Anwendung die Renderschleife aufruft. Nachdem die Effektvariablen festgelegt wurden, teilen Sie der Laufzeit mit, die Auswirkung durch Anwenden einer Technik zu rendern. Diese Themen werden weiter unten ausführlicher erläutert.

-   [Kompilieren eines Effekts (Direct3D 10)](d3d10-graphics-programming-guide-effects-compile.md)
-   [Erstellen eines Effekts (Direct3D 10)](d3d10-graphics-programming-guide-effects-create.md)
-   [Festlegen des Effektzustands (Direct3D 10)](d3d10-graphics-programming-guide-effects-set-state.md)
-   [Anwenden einer Technik (Direct3D 10)](d3d10-graphics-programming-guide-effects-apply-technique.md)

Natürlich gibt es [Überlegungen zur Leistung bei](d3d10-graphics-programming-guide-effects-performance.md) der Verwendung von Effekten. Diese Überlegungen sind größtenteils identisch, wenn Sie keinen Effekt verwenden. Dies kann beispielsweise das Minimieren der Menge an Zustandsänderungen oder das Organisieren der Variablen sein, die nach Häufigkeit aktualisiert werden müssen. Diese Taktiken werden verwendet, um die Menge der Daten zu minimieren, die von der CPU an die GPU gesendet werden müssen, und daher potenzielle Synchronisierungsprobleme zu minimieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



