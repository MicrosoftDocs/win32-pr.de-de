---
title: Effekte (Direct3D 11)
description: Erfahren Sie mehr über Direct3D 11-Effekte. Ein Effekt ist der Pipelinezustand, der durch in HLSL geschriebene Ausdrücke und eine syntaxspezifische Syntax festgelegt wird, die für das Effektframework spezifisch ist.
ms.assetid: d52a2cad-eac9-4442-9ee5-114bebe0f245
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063b554e28786b48a467de12042bf6ada99645a9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010643"
---
# <a name="effects-direct3d-11"></a>Effekte (Direct3D 11)

Ein DirectX-Effekt ist eine Auflistung des Pipelinezustands, die durch in [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-reference) geschriebene Ausdrücke und eine syntaxspezifische Syntax festgelegt wird, die für das Effektframework spezifisch ist.

Verwenden Sie nach dem Kompilieren eines Effekts die Effektframework-APIs zum Rendern. Die Effektfunktionalität kann von einem so einfachen Bereich reichen wie ein Vertex-Shader, der Geometrie und einen Pixel-Shader transformiert, der eine Volltonfarbe ausgibt, bis hin zu einer Renderingtechnik, die mehrere Durchläufe erfordert, jede Phase der Grafikpipeline verwendet und den Shaderzustand sowie den Pipelinezustand bearbeitet, der nicht den programmierbaren Shadern zugeordnet ist.

Der erste Schritt besteht darin, den Zustand zu organisieren, den Sie in einem Effekt steuern möchten. Dies schließt den Shaderzustand (Scheitelpunkt, Hülle, Domäne, Geometrie, Pixel- und Compute-Shader), den von den Shadern verwendeten Textur- und Samplerzustand sowie andere nicht programmierbare Pipelinestatus ein. Sie können einen Effekt im Arbeitsspeicher als Textzeichenfolge erstellen, aber in der Regel wird die Größe so groß, dass es praktisch ist, den Effektzustand in einer Effektdatei zu speichern (eine Textdatei, die mit einer FX-Erweiterung endet). Um einen Effekt zu verwenden, müssen Sie ihn kompilieren (um die HLSL-Syntax sowie die Syntax des Effektframeworks zu überprüfen), den Effektzustand über API-Aufrufe initialisieren und Ihre Renderschleife so ändern, dass die Rendering-APIs aufgerufen werden.

Ein Effekt kapselt den gesamten Renderzustand, der von einem bestimmten Effekt benötigt wird, in eine einzelne Renderingfunktion, die als Technik bezeichnet wird. Ein Durchlauf ist ein Teilsatz einer Technik, die den Renderzustand enthält. Um einen Renderingeffekt mit mehreren Durchläufen zu implementieren, implementieren Sie einen oder mehrere Durchläufe innerhalb einer Technik. Angenommen, Sie möchten einige Geometrien mit einem Satz von Tiefen-/Schablonenpuffern rendern und anschließend einige Sprites darüber zeichnen. Sie können das Geometrierendering im ersten Durchlauf und die Spritezeichnung im zweiten Durchlauf implementieren. Um den Effekt zu rendern, rendern Sie einfach beide Durchläufe in der Renderschleife. Sie können eine beliebige Anzahl von Techniken in einem Effekt implementieren. Je größer die Anzahl der Techniken ist, desto größer ist die Kompilierzeit für den Effekt. Eine Möglichkeit, diese Funktionalität zu nutzen, besteht darin, Effekte mit Techniken zu erzielen, die für die Ausführung auf unterschiedlicher Hardware konzipiert sind. Dadurch kann eine Anwendung die Leistung basierend auf den erkannten Hardwarefunktionen ordnungsgemäß herabstufen.

Eine Reihe von Techniken kann in einer Gruppe gruppiert werden (die die Syntax "fxgroup" verwendet). Techniken können in beliebiger Weise gruppiert werden. Beispielsweise können mehrere Gruppen erstellt werden, eine pro Material. jedes Material kann über eine Technik für jede Hardwareebene verfügen. jede Technik verfügt über eine Reihe von Durchläufen, die das Material auf der jeweiligen Hardware definieren.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                | Beschreibung                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Organisieren des Zustands in einem Effekt](d3d11-graphics-programming-guide-effects-organize.md)<br/>                    | Mit Direct3D 11 wird der Effektzustand für bestimmte Pipelinephasen nach Strukturen organisiert.<br/>                                                                   |
| [Effektsystemschnittstellen](d3d11-graphics-programming-guide-effects-interfaces.md)<br/>                       | Das Effektsystem definiert mehrere Schnittstellen zum Verwalten des Effektzustands.<br/>                                                                                  |
| [Spezielle Schnittstellen](d3d11-graphics-reference-effect-specializing.md)<br/>                               | [**ID3DX11EffectVariable**](id3dx11effectvariable.md) verfügt über eine Reihe von Methoden zum Umwandeln der Schnittstelle in den gewünschten Schnittstellentyp.<br/> |
| [Schnittstellen und Klassen in Effekten](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md)<br/>  | Es gibt viele Möglichkeiten, Klassen und Schnittstellen in Effects 11 zu verwenden.<br/>                                                                                         |
| [Rendern eines Effekts](d3d11-graphics-programming-guide-effects-render.md)<br/>                                | Ein Effekt kann zum Speichern von Informationen oder zum Rendern mit einer Statusgruppe verwendet werden.<br/>                                                                         |
| [Klonen eines Effekts](d3d11-graphics-programming-guide-effects-cloning.md)<br/>                                 | Beim Klonen eines Effekts wird eine zweite, fast identische Kopie des Effekts erstellt.<br/>                                                                                 |
| [Stream Out-Syntax](d3d11-graphics-reference-effect-streamout.md)<br/>                                        | Ein geometriefarbener Shader mit Ausgehender Stream wird mit einer bestimmten Syntax deklariert.<br/>                                                                                  |
| [Unterschiede zwischen Effekten 10 und Effekten 11](d3d11-graphics-programming-guide-effects-differences.md)<br/> | In diesem Thema werden die Unterschiede zwischen Effekten 10 und Effects 11 erläutert.<br/>                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

