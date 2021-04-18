---
description: Herkömmliche Texturen werden als Single-Element-Texturen betrachtet.
ms.assetid: 8fe8da80-0879-413a-a7db-617d2f558b28
title: Texturen mit mehreren Elementen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a434d1e6c6a892c794551aa0caf34890f3def9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344156"
---
# <a name="multiple-element-textures-direct3d-9"></a>Texturen mit mehreren Elementen (Direct3D 9)

Herkömmliche Texturen werden als Single-Element-Texturen betrachtet. Texturen mit mehreren Elementen ermöglichen es Anwendungen, gleichzeitig auf mehrere Elemente einer Textur aus dem Pixelshader zu schreiben. Das Ergebnis im nächsten Renderingdurchlauf besteht darin, dass eine Anwendung ein oder mehrere Elemente als Einzelelement Textur verwenden kann, d. h. als Eingaben für den Pixelshader. Diese zusätzlichen Elemente können als temporärer Speicher für Zwischenergebnisse betrachtet werden, die in einem späteren Durchlauf von der Anwendung verwendet werden.

Die erste Generation von Hardware, die diese Funktion verfügbar macht, weist die folgenden Einschränkungen auf:

-   Alle Textur Oberflächen mit mehreren Elementen werden automatisch zugeordnet. Diese Einschränkung wird behoben, indem Sie diese als neue Art von Oberflächen Format behandelt, bei der mehrere RGBA-Kanäle verschachtelt sind.
-   Alle Elemente der Textur mit mehreren Elementen können die gleiche Bittiefe aufweisen. Diese Einschränkung wird durch den Namen der neuen Oberflächen Formate ausgedrückt.
-   Eine Textur mit mehreren Elementen kann nicht das primäre/anzeigbare Element sein. Das heißt, es muss nur auf dem Bildschirm angezeigt werden. Diese Einschränkung wird durch die Enumeration des Surface-Formats ausgedrückt.
-   Es sind keine Dithering-, Alpha Test-, fogging-, Mischungs-, Raster-op-oder Maskierungs Aktionen zulässig. Es erfolgt keine Verarbeitung nach dem Pixel-Shader, außer dem z-Test und dem Schablone-Test.
-   Die Textur kann keine MipMap sein. Die Erstellung der MIP-Kette schlägt fehl.
-   Das gleiche Element kann nicht als Textur festgelegt werden, wenn es sich um ein Renderziel handelt. Allerdings können unterschiedliche Elemente derselben Textur Oberfläche mit mehreren Elementen gleichzeitig Texturen und Renderingziele sein.
-   Es wird kein Antialiasing unterstützt.
-   Textur Oberflächen mit mehreren Elementen, wenn Sie als Textur verwendet werden, können nicht gefiltert werden. Diese Einschränkung kann mithilfe von [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)überprüft werden.
-   Textur Oberflächen mit mehreren Elementen können nicht gesperrt werden.
-   Mehrere Textur Oberflächen mit mehreren Elementen können gleichzeitig verwendet werden, indem Sie jeweils verschiedenen Phasen zugewiesen werden, genau wie bei normalen Texturen.
-   Textur Oberflächen mit mehreren Elementen unterstützen die Konvertierung von Gamma von 2,2 in eine 1,0-Konvertierung bei einem Lesevorgang, ebenso wie bei anderen Textur Formaten.
-   Einige Implementierungen wenden nicht die Ausgabe Schreib Maske an (D3DRS \_ colorschreiteenable). Solche, die unabhängige Farb Schreib Masken aufweisen können. Dies wird mithilfe eines neuen Funktionsbits ausgedrückt. Die Anzahl der verfügbaren unabhängigen Farb Schreib Masken ist gleich der maximalen Anzahl von Elementen, für die das Gerät geeignet ist.
-   [**Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) löscht alle Elemente der Textur mit mehreren Elementen, die als Renderziel festgelegt wird.

Die Verwendung von Texturen mit mehreren Elementen folgt den folgenden Schritten:

1.  Anwendungen entdecken die Unterstützung für dieses Feature, indem Sie die Verfügbarkeit von Textur Formaten mit mehreren Elementen überprüfen.
2.  Die Anwendung erstellt diese Oberflächen durch Aufrufen von [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture).
3.  Die Anwendung legt die Oberfläche als Renderziel mithilfe des [**SetRenderTarget**](/windows/desktop/api) -Aufrufes fest. Der Pixelshader stellt mithilfe der [MOV-PS-](../direct3dhlsl/mov---ps.md) Anweisung die Ausgabe für die-Oberflächen bereit.
4.  [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) wird aufgerufen, um eine Textur Oberfläche mit mehreren Elementen auf eine bestimmte Stufe festzulegen. Wie bei anderen Texturen kann dieselbe Oberfläche auf mehrere Stufen gleichzeitig festgelegt werden.
5.  [**Setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) wird aufgerufen, um D3DSAMP \_ Elementindex auf die entsprechende Element Nummer in der Textur mit mehreren Elementen festzulegen, von der die samplerbeispiele abgeleitet werden. Der Standardwert für diesen Status ist 0 (null), d. h., nicht-Multiple-Element-Texturen funktionieren. Das Festlegen dieses Zustands auf eine ungeeignete Zahl führt zu einem nicht definierten Verhalten, wenn die Textur mit mehreren Elementen nur zwei Elemente breit ist, aber der Sampler beispielsweise zum Beispiel aus dem vierten Element aufgefordert wird.

## <a name="api-support"></a>API-Unterstützung

Im folgenden finden Sie eine Zusammenfassung der API-Elemente, die Texturen mit mehreren Elementen unterstützen:

-   Das [D3DFMT \_ MULTI2 \_ ARGB8](d3dformat.md) Surface-Format drückt die überlappende Natur des Formats aus.
-   Der D3DSAMP \_ Elementindex-samplerstatus gibt an, welcher Element Index verwendet werden soll.
-   Die folgenden Rendering-Zustände unterstützen Texturen mit mehreren Elementen:

    -   D3DRS \_ COLORWRITEENABLE1
    -   D3DRS \_ COLORWRITEENABLE2
    -   D3DRS \_ COLORWRITEENABLE3

    D3DRS \_ colorschreiteenable gilt für das Renderziel (oder das-Element) 0 (null).

-   Das Flag [D3DPMISCCAPS \_ independentwrite temasks](d3dpmisccaps.md) gibt an, dass das Gerät unabhängige Schreib Masken für mehrere Element Texturen oder mehrere Renderziele unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel Pipeline](pixel-pipeline.md)
</dt> </dl>

 

 
