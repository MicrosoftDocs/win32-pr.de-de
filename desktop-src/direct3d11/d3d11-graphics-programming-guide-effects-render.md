---
title: Rendern eines Effekts (Direct3D 11)
description: Erfahren Sie mehr über das Rendern eines Effekts für Direct3D 11. Ein Effekt kann verwendet werden, um Informationen zu speichern oder mit einer Gruppe von Status zu rendern.
ms.assetid: 7af239de-812d-4295-b599-b9deb371b01b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3ba8ebbc1ac8989ac10568a00f26b26370c4bb8e7710098733dad74618e53af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913600"
---
# <a name="rendering-an-effect-direct3d-11"></a>Rendern eines Effekts (Direct3D 11)

Ein Effekt kann verwendet werden, um Informationen zu speichern oder mit einer Gruppe von Status zu rendern. Jede Technik gibt eine Reihe von Vertex-Shadern, Hüllen-Shadern, Domänen-Shadern, Geometrie-Shadern, Pixel-Shadern, Compute-Shadern, Shaderzustand, Sampler- und Texturzustand, ungeordneten Zugriffsansichtszustand und anderen Pipelinestatus an. Sobald Sie also den Zustand in einem Effekt organisiert haben, können Sie den Renderingeffekt, der sich aus diesem Zustand ergibt, kapseln, indem Sie den Effekt erstellen und rendern.

Es gibt einige Schritte zum Vorbereiten eines Effekts für das Rendering. Die erste ist die Kompilierung, bei der HLSL wie Code mit der HLSL-Sprachsyntax und den Auswirkungsframeworkregeln überprüft wird. Sie können einen Effekt aus Ihrer Anwendung mithilfe von API-Aufrufen kompilieren, oder Sie können einen Effekt offline kompilieren, indem Sie das Effektcompiler-Hilfsprogramm [fxc.exe. ](/windows/desktop/direct3dtools/fxc) Nachdem der Effekt erfolgreich kompiliert wurde, erstellen Sie ihn, indem Sie einen anderen (aber sehr ähnlichen) Satz von APIs aufrufen.

Nachdem der Effekt erstellt wurde, gibt es zwei verbleibende Schritte für die Verwendung. Zunächst müssen Sie die Effektzustandswerte (die Werte der Effektvariablen) mithilfe einer Reihe von Methoden zum Festlegen des Zustands initialisieren, wenn sie nicht in HLSL initialisiert werden. Bei einigen Variablen kann dies einmal erfolgen, wenn ein Effekt erstellt wird. andere müssen jedes Mal aktualisiert werden, wenn ihre Anwendung die Renderschleife aufruft. Nachdem die Effektvariablen festgelegt wurden, teilen Sie der Laufzeit mit, den Effekt durch Anwenden einer Technik zu rendern. Diese Themen werden weiter unten ausführlicher erläutert.

Natürlich gibt es Überlegungen zur Leistung bei der Verwendung von Effekten. Diese Überlegungen sind größtenteils identisch, wenn Sie keinen Effekt verwenden. Dies kann z. B. das Minimieren der Menge an Zustandsänderungen und das Organisieren der Variablen nach Aktualisierungshäufigkeit sein. Diese Taktiken werden verwendet, um die Menge der Daten zu minimieren, die von der CPU an die GPU gesendet werden müssen, und daher potenzielle Synchronisierungsprobleme zu minimieren.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                        | Beschreibung                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Kompilieren eines Effekts](d3d11-graphics-programming-guide-effects-compile.md)<br/>         | Nachdem ein Effekt erstellt wurde, besteht der nächste Schritt im Kompilieren des Codes, um nach Syntaxproblemen zu suchen.<br/>                                                                                                                                                                                                          |
| [Erstellen eines Effekts](d3d11-graphics-programming-guide-effects-create.md)<br/>           | Ein Effekt wird durch Laden des kompilierten Effekt-Bytecodes in das Effektframework erstellt. Im Gegensatz zu Effekten 10 muss der Effekt kompiliert werden, bevor der Effekt erstellt wird. In den Arbeitsspeicher geladene Effekte können durch Aufrufen von [**D3DX11CreateEffectFromMemory erstellt werden.**](d3dx11createeffectfrommemory.md)<br/>                 |
| [Festlegen des Effektzustands](d3d11-graphics-programming-guide-effects-set-state.md)<br/>        | Einige Effektkonst constants müssen nur initialisiert werden. Nach der Initialisierung wird der Effektzustand für die gesamte Renderschleife auf das Gerät festgelegt. Andere Variablen müssen jedes Mal aktualisiert werden, wenn die Renderschleife aufgerufen wird. Der grundlegende Code zum Festlegen von Effektvariablen wird unten für jeden Variablentypen gezeigt.<br/> |
| [Anwenden einer Technik](d3d11-graphics-programming-guide-effects-apply-technique.md)<br/> | Wenn die Konstanten, Texturen und der Shaderzustand deklariert und initialisiert sind, müssen Sie nur noch den Effektzustand auf dem Gerät festlegen.<br/>                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

