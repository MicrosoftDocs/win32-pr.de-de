---
title: Effekte (Direct3D 11)
description: Erfahren Sie mehr über Direct3D 11-Effekte. Ein Effekt ist der Pipelinezustand, der durch in HLSL geschriebene Ausdrücke und eine syntaxspezifische Syntax für das Effektframework festgelegt wird.
ms.assetid: d52a2cad-eac9-4442-9ee5-114bebe0f245
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fe4cdb204e498a0c6a8f4d5f6e4656446c0f0a3f4d660f2e0e2a33e8515a0e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990100"
---
# <a name="effects-direct3d-11"></a>Effekte (Direct3D 11)

Ein DirectX-Effekt ist eine Auflistung des Pipelinezustands, die von in [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-reference) geschriebenen Ausdrücken und einer syntaxspezifischen Syntax für das Effektframework festgelegt wird.

Verwenden Sie nach dem Kompilieren eines Effekts die Effektframework-APIs zum Rendern. Die Effektfunktionalität kann so einfach sein wie ein Vertex-Shader, der geometrie transformiert, und ein Pixel-Shader, der eine Volltonfarbe ausgibt, bis hin zu einer Renderingtechnik, die mehrere Durchläufe erfordert, jede Phase der Grafikpipeline verwendet und den Shaderzustand sowie den Pipelinezustand bearbeitet, der nicht den programmierbaren Shadern zugeordnet ist.

Der erste Schritt besteht im Organisieren des Zustands, den Sie in einem Effekt steuern möchten. Dazu gehören der Shaderzustand (Scheitelpunkt, Hülle, Domäne, Geometrie, Pixel- und Compute-Shader), der von den Shadern verwendete Textur- und Samplerzustand sowie andere nicht programmierbare Pipelinestatus. Sie können einen Effekt im Arbeitsspeicher als Textzeichenfolge erstellen, aber in der Regel wird die Größe so groß, dass es praktisch ist, den Effektzustand in einer Effektdatei (einer Textdatei, die mit der Erweiterung .fx endet) zu speichern. Um einen Effekt zu verwenden, müssen Sie ihn kompilieren (um die HLSL-Syntax sowie die Effektframeworksyntax zu überprüfen), den Effektzustand über API-Aufrufe initialisieren und die Renderschleife so ändern, dass die Rendering-APIs aufrufen.

Ein Effekt kapselt den render-Zustand, der für einen bestimmten Effekt erforderlich ist, in eine einzelne Renderingfunktion, die als Technik bezeichnet wird. Ein Durchgang ist ein Teilsatz einer Technik, die den Renderzustand enthält. Implementieren Sie einen oder mehrere Durchläufe innerhalb einer Technik, um einen Multiple-Pass-Renderingeffekt zu implementieren. Beispiel: Sie möchten eine Geometrie mit einem Satz von Tiefen-/Schablonenpuffern rendern und dann einige Sprites darauf zeichnen. Sie könnten das Geometrierendering im ersten Durchgang und die Sprite-Zeichnung im zweiten Durchgang implementieren. Um den Effekt zu rendern, rendern Sie einfach beide Durchläufe in der Renderschleife. Sie können eine beliebige Anzahl von Techniken in einem Effekt implementieren. Je größer die Anzahl der Techniken, desto größer ist die Kompilierzeit für den Effekt. Eine Möglichkeit, diese Funktionalität zu nutzen, besteht in der Erstellung von Effekten mit Techniken, die für die Ausführung auf unterschiedlicher Hardware entwickelt wurden. Dadurch kann eine Anwendung die Leistung basierend auf den erkannten Hardwarefunktionen ordnungsgemäß herabstufen.

Eine Reihe von Techniken kann in einer Gruppe (die die Syntax "fxgroup" verwendet) gruppiert werden. Techniken können auf beliebige Weise gruppiert werden. Beispielsweise können mehrere Gruppen erstellt werden, eine pro Material. jedes Material kann eine Technik für jede Hardwareebene haben. Jede Technik würde eine Reihe von Durchläufen haben, die das Material auf der jeweiligen Hardware definieren.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                | Beschreibung                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Organisieren des Zustands in einem Effekt](d3d11-graphics-programming-guide-effects-organize.md)<br/>                    | Bei Direct3D 11 ist der Effektzustand für bestimmte Pipelinestufen nach Strukturen organisiert.<br/>                                                                   |
| [Effect-Systemschnittstellen](d3d11-graphics-programming-guide-effects-interfaces.md)<br/>                       | Das Effektsystem definiert mehrere Schnittstellen zum Verwalten des Effektzustands.<br/>                                                                                  |
| [Spezielle Schnittstellen](d3d11-graphics-reference-effect-specializing.md)<br/>                               | [**ID3DX11EffectVariable**](id3dx11effectvariable.md) verfügt über eine Reihe von Methoden zum Umwandlung der Schnittstelle in den bestimmten Schnittstellentyp, den Sie benötigen.<br/> |
| [Schnittstellen und Klassen in Effekten](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md)<br/>  | Es gibt viele Möglichkeiten, Klassen und Schnittstellen in Effects 11 zu verwenden.<br/>                                                                                         |
| [Rendern eines Effekts](d3d11-graphics-programming-guide-effects-render.md)<br/>                                | Ein Effekt kann verwendet werden, um Informationen zu speichern oder mit einer Gruppe von Status zu rendern.<br/>                                                                         |
| [Klonen eines Effekts](d3d11-graphics-programming-guide-effects-cloning.md)<br/>                                 | Beim Klonen eines Effekts wird eine zweite, fast identische Kopie des Effekts erstellt.<br/>                                                                                 |
| [Stream Out-Syntax](d3d11-graphics-reference-effect-streamout.md)<br/>                                        | Ein Geometrie-Shader mit Stream out wird mit einer bestimmten Syntax deklariert.<br/>                                                                                  |
| [Unterschiede zwischen Effekt 10 und Effekt 11](d3d11-graphics-programming-guide-effects-differences.md)<br/> | In diesem Thema werden die Unterschiede zwischen Effects 10 und Effects 11 veranschaulicht.<br/>                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

