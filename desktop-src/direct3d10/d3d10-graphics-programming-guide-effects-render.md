---
description: Ein Effekt kann zum Speichern von Informationen oder zum Rendering mithilfe einer Zustands Gruppe verwendet werden.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Rendern eines Effekts (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfba9432412846e2dc634d6ab68be999b504e06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214083"
---
# <a name="rendering-an-effect-direct3d-10"></a>Rendern eines Effekts (Direct3D 10)

Ein Effekt kann zum Speichern von Informationen oder zum Rendering mithilfe einer Zustands Gruppe verwendet werden. Jede Technik gibt Scheitelpunkt-Shader, Geometry-Shader, Pixel-Shader, shaderzustand, Sampler und Textur Zustand und anderen Pipeline Zustand an. Nachdem Sie den Status in einem Effekt organisiert haben, können Sie den renderingeffekt Kapseln, der sich aus diesem Zustand ergibt, indem Sie den Effekt erstellen und rendern.

Es gibt einige Schritte zum Vorbereiten eines Effekts für das Rendering. Der erste ist die Kompilierung, die den HLSL-Code auf die HLSL-Sprachsyntax und die Effekt Framework-Regeln überprüft. Sie können einen Effekt von Ihrer Anwendung mithilfe von API-aufrufen kompilieren, oder Sie können einen Effekt offline mit dem Effekt-Compilerdienstprogramm kompilieren. Nachdem ihre Wirkung erfolgreich kompiliert wurde, erstellen Sie Sie durch Aufrufen eines anderen (aber sehr ähnlichen) Satzes von APIs.

Nachdem der Effekt erstellt wurde, gibt es zwei verbleibende Schritte für die Verwendung. Zunächst müssen Sie die Werte des Wirkungs Zustands (die Werte der Effekt Variablen) mit einer Reihe von Methoden zum Festlegen des Zustands initialisieren. Bei einigen Variablen kann dies einmalig erfolgen, wenn ein Effekt erstellt wird. andere müssen jedes Mal aktualisiert werden, wenn die Anwendung die Renderschleife aufruft. Nachdem die Effekt Variablen festgelegt wurden, weisen Sie die Laufzeit an, die Auswirkung durch Anwenden einer Technik zu Rendering. Diese Themen werden im folgenden ausführlicher erläutert.

-   [Kompilieren eines Effekts (Direct3D 10)](d3d10-graphics-programming-guide-effects-compile.md)
-   [Erstellen eines Effekts (Direct3D 10)](d3d10-graphics-programming-guide-effects-create.md)
-   [Status des festgelegten Effekts (Direct3D 10)](d3d10-graphics-programming-guide-effects-set-state.md)
-   [Anwenden einer Technik (Direct3D 10)](d3d10-graphics-programming-guide-effects-apply-technique.md)

Natürlich sind bei der Verwendung von Effekten [Leistungsaspekte zu berücksichtigen](d3d10-graphics-programming-guide-effects-performance.md) . Diese Überlegungen sind größtenteils identisch, wenn Sie keinen Effekt verwenden. Dinge wie das Minimieren der Menge der Zustandsänderungen oder das Organisieren der Variablen, die nach Häufigkeit aktualisiert werden müssen. Diese Taktiken werden verwendet, um die Datenmenge zu minimieren, die von der CPU an die GPU gesendet werden muss, und damit potenzielle Synchronisierungs Probleme zu minimieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



