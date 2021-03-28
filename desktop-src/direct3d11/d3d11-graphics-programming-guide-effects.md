---
title: Effekte (Direct3D 11)
description: Ein DirectX-Effekt ist eine Auflistung von Pipeline Zuständen, die durch in HLSL geschriebene Ausdrücke und eine bestimmte, für das Effect-Framework spezifische Syntax festgelegt ist.
ms.assetid: d52a2cad-eac9-4442-9ee5-114bebe0f245
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8952a35e1212f7d50956cc54e7a046db9f87b3b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728400"
---
# <a name="effects-direct3d-11"></a>Effekte (Direct3D 11)

Ein DirectX-Effekt ist eine Auflistung von Pipeline Zuständen, die durch in [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-reference) geschriebene Ausdrücke und eine bestimmte, für das Effect-Framework spezifische Syntax festgelegt ist.

Verwenden Sie nach dem Kompilieren eines Effekts die Effekt-Framework-APIs zum Rendering. Die Auswirkung der Funktionalität kann von etwas einfacher sein wie ein Vertexshader, der Geometrie transformiert, und ein Pixelshader, der eine voll Tonfarbe ausgibt, an eine renderingtechnik, die mehrere Durchgänge erfordert, jede Phase der Grafik Pipeline verwendet und den shaderzustand und den Pipeline Zustand, der den programmierbaren Shadern nicht zugeordnet ist, ändert.

Der erste Schritt besteht darin, den Zustand zu organisieren, den Sie steuern möchten. Dies schließt den shaderzustand (Scheitelpunkt, Hülle, Domäne, Geometrie, Pixel und Compute-Shader), den Textur-und samplerzustand, der von den Shadern verwendet wird, und den anderen nicht programmierbaren Pipeline Zustand ein. Sie können einen Effekt im Arbeitsspeicher als Text Zeichenfolge erstellen, aber in der Regel ist die Größe so groß, dass es praktisch ist, den Effekt Zustand in einer Effekt Datei zu speichern (eine Textdatei, die auf eine FX-Erweiterung endet). Um einen Effekt zu erzielen, müssen Sie ihn kompilieren (um die HLSL-Syntax und die Effekt-Framework-Syntax zu überprüfen), den Effekt Zustand über API-Aufrufe initialisieren und die Renderingschleife ändern, um die Rendering-APIs aufzurufen.

Ein Effekt kapselt den gesamten renderzustand, der für einen bestimmten Effekt erforderlich ist, in eine einzelne Renderingfunktion, die als Technik bezeichnet wird. Ein Durchlauf ist eine Teilmenge einer Technik, die den renderzustand enthält. Implementieren Sie einen oder mehrere Durchgänge innerhalb eines Verfahrens, um einen Multipass-renderingeffekt zu implementieren. Angenommen, Sie möchten eine Geometrie mit einem Satz von tiefen-/Schablone-Puffern rendern und dann einige Sprites darauf zeichnen. Sie könnten das Geometrie Rendering im ersten Durchlauf und die Sprite-Zeichnung im zweiten Durchlauf implementieren. Um den Effekt zu rendereinigen, werden Sie einfach beide Pass-in der Renderschleife Render. Sie können eine beliebige Anzahl von Techniken in Kraft setzen. Natürlich ist die Anzahl der Techniken umso größer als die Kompilierzeit für den Effekt. Eine Möglichkeit, diese Funktionalität auszunutzen, ist das Erstellen von Effekten mit Techniken, die auf unterschiedlichen Hardware ausgeführt werden sollen. Dies ermöglicht es einer Anwendung, die Leistung basierend auf den erkannten Hardwarefunktionen ordnungsgemäß herabzusetzen.

Eine Reihe von Techniken kann in einer Gruppe gruppiert werden (die die Syntax "fxgroup" verwendet). Techniken können in beliebiger Weise gruppiert werden. Beispielsweise können mehrere Gruppen erstellt werden, eine pro Material. jedes Material kann über eine Technik für jede Hardwareebene verfügen. jede Technik hätte eine Reihe von Durchläufen, die das Material auf der jeweiligen Hardware definieren.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                | BESCHREIBUNG                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Anordnen des Zustands eines Effekts](d3d11-graphics-programming-guide-effects-organize.md)<br/>                    | Mit Direct3D 11 wird der Effekt Zustand für bestimmte Pipeline Stufen nach Strukturen organisiert.<br/>                                                                   |
| [System Schnittstellen des Effekts](d3d11-graphics-programming-guide-effects-interfaces.md)<br/>                       | Das Effect-System definiert mehrere Schnittstellen zur Verwaltung des Wirkungs Zustands.<br/>                                                                                  |
| [Spezialisierte Schnittstellen](d3d11-graphics-reference-effect-specializing.md)<br/>                               | [**ID3DX11EffectVariable**](id3dx11effectvariable.md) verfügt über eine Reihe von Methoden, mit denen die Schnittstelle in den speziellen Typ der benötigten Schnittstelle umgewandelt wird.<br/> |
| [Schnittstellen und Klassen in Effekten](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md)<br/>  | Es gibt viele Möglichkeiten, Klassen und Schnittstellen in den Effekten 11 zu verwenden.<br/>                                                                                         |
| [Rendern eines Effekts](d3d11-graphics-programming-guide-effects-render.md)<br/>                                | Ein Effekt kann zum Speichern von Informationen oder zum Rendering mithilfe einer Zustands Gruppe verwendet werden.<br/>                                                                         |
| [Klonen eines Effekts](d3d11-graphics-programming-guide-effects-cloning.md)<br/>                                 | Das Klonen eines Effekts erzeugt eine zweite, fast identische Kopie des Effekts.<br/>                                                                                 |
| [Stream out-Syntax](d3d11-graphics-reference-effect-streamout.md)<br/>                                        | Ein Geometry-Shader mit Stream out wird mit einer bestimmten Syntax deklariert.<br/>                                                                                  |
| [Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md)<br/> | In diesem Thema werden die Unterschiede zwischen den Effekten 10 und den Effekten 11 veranschaulicht.<br/>                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

