---
title: Rendern eines Effekts (Direct3D 11)
description: Erfahren Sie mehr über das Rendern eines Effekts für Direct3D 11. Ein Effekt kann zum Speichern von Informationen oder zum Rendern mit einer Statusgruppe verwendet werden.
ms.assetid: 7af239de-812d-4295-b599-b9deb371b01b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7def8f7bbfb9f2c7a5102eb8e02fc848155e4bde
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112261832"
---
# <a name="rendering-an-effect-direct3d-11"></a>Rendern eines Effekts (Direct3D 11)

Ein Effekt kann zum Speichern von Informationen oder zum Rendern mit einer Statusgruppe verwendet werden. Jede Technik gibt einige Vertex-Shader, Hüllen-Shader, Domänen-Shader, Geometrie-Shader, Pixel-Shader, Compute-Shader, Shaderzustand, Sampler- und Texturzustand, ungeordneten Zugriffsansichtszustand und anderen Pipelinezustand an. Sobald Sie also den Zustand in einem Effekt organisiert haben, können Sie den Renderingeffekt, der sich aus diesem Zustand ergibt, kapseln, indem Sie den Effekt erstellen und rendern.

Es gibt einige Schritte zum Vorbereiten eines Effekts für das Rendering. Die erste ist die Kompilierung, die den HLSL-ähnlichen Code anhand der HLSL-Sprachsyntax und der Auswirkungsframeworkregeln überprüft. Sie können einen Effekt aus Ihrer Anwendung mithilfe von API-Aufrufen kompilieren, oder Sie können einen Effekt offline kompilieren, indem Sie das Effektcompilerhilfsprogramm [fxc.exe](/windows/desktop/direct3dtools/fxc)verwenden. Nachdem Ihre Auswirkung erfolgreich kompiliert wurde, erstellen Sie sie, indem Sie einen anderen (aber sehr ähnlichen) Satz von APIs aufrufen.

Nachdem der Effekt erstellt wurde, gibt es zwei verbleibende Schritte für die Verwendung. Zunächst müssen Sie die Werte des Effektzustands (die Werte der Effektvariablen) mithilfe einer Reihe von Methoden zum Festlegen des Zustands initialisieren, wenn sie nicht in HLSL initialisiert werden. Bei einigen Variablen kann dies einmal erfolgen, wenn ein Effekt erstellt wird. andere müssen jedes Mal aktualisiert werden, wenn Ihre Anwendung die Renderschleife aufruft. Nachdem die Effektvariablen festgelegt wurden, weisen Sie die Laufzeit an, den Effekt durch Anwenden einer Technik zu rendern. Diese Themen werden im Folgenden ausführlicher erläutert.

Natürlich gibt es Überlegungen zur Leistung bei der Verwendung von Effekten. Diese Überlegungen sind größtenteils identisch, wenn Sie keinen Effekt verwenden. Beispiele: Minimieren der Menge von Zustandsänderungen und Organisieren der Variablen nach Aktualisierungshäufigkeit. Diese Taktiken werden verwendet, um die Datenmenge zu minimieren, die von der CPU an die GPU gesendet werden muss, und somit potenzielle Synchronisierungsprobleme zu minimieren.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                        | Beschreibung                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Kompilieren eines Effekts](d3d11-graphics-programming-guide-effects-compile.md)<br/>         | Nachdem ein Effekt erstellt wurde, besteht der nächste Schritt darin, den Code zu kompilieren, um nach Syntaxproblemen zu suchen.<br/>                                                                                                                                                                                                          |
| [Erstellen eines Effekts](d3d11-graphics-programming-guide-effects-create.md)<br/>           | Ein Effekt wird erstellt, indem der kompilierte Effekt-Bytecode in das Effektframework geladen wird. Im Gegensatz zu Effekten 10 muss der Effekt vor dem Erstellen des Effekts kompiliert werden. In den Arbeitsspeicher geladene Effekte können durch Aufrufen von [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md)erstellt werden.<br/>                 |
| [Festlegen des Auswirkungszustands](d3d11-graphics-programming-guide-effects-set-state.md)<br/>        | Einige Effektkonstanten müssen nur initialisiert werden. Nach der Initialisierung wird der Effektzustand für die gesamte Renderschleife auf das Gerät festgelegt. Andere Variablen müssen jedes Mal aktualisiert werden, wenn die Renderschleife aufgerufen wird. Der grundlegende Code zum Festlegen von Effektvariablen ist unten für jeden Variablentyp dargestellt.<br/> |
| [Anwenden einer Technik](d3d11-graphics-programming-guide-effects-apply-technique.md)<br/> | Mit den deklarierten und initialisierten Konstanten, Texturen und Shaderstatus muss nur noch der Effektzustand auf dem Gerät festgelegt werden.<br/>                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

