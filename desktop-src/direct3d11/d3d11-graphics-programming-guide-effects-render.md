---
title: Rendern eines Effekts (Direct3D 11)
description: Ein Effekt kann zum Speichern von Informationen oder zum Rendering mithilfe einer Zustands Gruppe verwendet werden.
ms.assetid: 7af239de-812d-4295-b599-b9deb371b01b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c99aef9f83cdf286e86ca843e57315d9ab88619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390558"
---
# <a name="rendering-an-effect-direct3d-11"></a>Rendern eines Effekts (Direct3D 11)

Ein Effekt kann zum Speichern von Informationen oder zum Rendering mithilfe einer Zustands Gruppe verwendet werden. Jede Technik gibt eine Reihe von Vertex-Shadern, Hull-Shadern, Domänen-Shadern, Geometry-Shadern, Pixel-Shader, COMPUTE-Shader, shaderzustand, Sampler und Textur Zustand, ungeordneten Zugriffs Ansichts Zustand und anderen Pipeline Status an. Nachdem Sie den Status in einem Effekt organisiert haben, können Sie den renderingeffekt Kapseln, der sich aus diesem Zustand ergibt, indem Sie den Effekt erstellen und rendern.

Es gibt einige Schritte zum Vorbereiten eines Effekts für das Rendering. Der erste ist die Kompilierung, die den HLSL-Code auf die HLSL-Sprachsyntax und die Effekt Framework-Regeln überprüft. Sie können einen Effekt von Ihrer Anwendung mithilfe von API-aufrufen kompilieren, oder Sie können einen Effekt Offline kompilieren, indem Sie das compilerdiensthilfsprogramm [fxc.exe](/windows/desktop/direct3dtools/fxc). Nachdem ihre Wirkung erfolgreich kompiliert wurde, erstellen Sie Sie durch Aufrufen eines anderen (aber sehr ähnlichen) Satzes von APIs.

Nachdem der Effekt erstellt wurde, gibt es zwei verbleibende Schritte für die Verwendung. Zunächst müssen Sie die Werte des Wirkungs Zustands (die Werte der Effekt Variablen) mit einer Reihe von Methoden zum Festlegen des Zustands initialisieren, wenn Sie nicht in HLSL initialisiert werden. Bei einigen Variablen kann dies einmalig erfolgen, wenn ein Effekt erstellt wird. andere müssen jedes Mal aktualisiert werden, wenn die Anwendung die Renderschleife aufruft. Nachdem die Effekt Variablen festgelegt wurden, weisen Sie die Laufzeit an, die Auswirkung durch Anwenden einer Technik zu Rendering. Diese Themen werden im folgenden ausführlicher erläutert.

Natürlich sind bei der Verwendung von Effekten Leistungsaspekte zu berücksichtigen. Diese Überlegungen sind größtenteils identisch, wenn Sie keinen Effekt verwenden. Dinge wie das Minimieren der Menge an Zustandsänderungen und das Organisieren der Variablen nach Aktualisierungshäufigkeit. Diese Taktiken werden verwendet, um die Datenmenge zu minimieren, die von der CPU an die GPU gesendet werden muss, und damit potenzielle Synchronisierungs Probleme zu minimieren.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Kompilieren eines Effekts](d3d11-graphics-programming-guide-effects-compile.md)<br/>         | Nachdem ein Effekt erstellt wurde, besteht der nächste Schritt darin, den Code zu kompilieren, um auf Syntax Probleme zu überprüfen.<br/>                                                                                                                                                                                                          |
| [Erstellen eines Effekts](d3d11-graphics-programming-guide-effects-create.md)<br/>           | Ein Effekt wird erstellt, indem der kompilierte Effekt Bytecode in das Effects-Framework geladen wird. Anders als bei Effekten 10 muss der Effekt vor dem Erstellen des Effekts kompiliert werden. In den Arbeitsspeicher geladene Effekte können durch Aufrufen von [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md)erstellt werden.<br/>                 |
| [Status des festgelegten Effekts](d3d11-graphics-programming-guide-effects-set-state.md)<br/>        | Einige Effekt Konstanten müssen nur initialisiert werden. Nach der Initialisierung wird der Effekt Zustand auf das Gerät für die gesamte Renderschleife festgelegt. Andere Variablen müssen jedes Mal aktualisiert werden, wenn die Renderschleife aufgerufen wird. Der grundlegende Code für das Festlegen von Effekt Variablen wird unten für jeden der Variablen Typen angezeigt.<br/> |
| [Anwenden einer Technik](d3d11-graphics-programming-guide-effects-apply-technique.md)<br/> | Wenn die Konstanten, Texturen und der Shader-Zustand deklariert und initialisiert sind, besteht die einzige Aufgabe darin, den Effekt Zustand im Gerät festzulegen.<br/>                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

