---
title: Kacheln eines gekachelten Ressourcenbereichs
description: Wenn Sie eine Kachel Ressource erstellen, bestimmen Dimensionen, Format Elementgröße und Anzahl von Mipmaps und/oder Array Slices (falls zutreffend) die Anzahl der Kacheln, die für die gesamte Oberfläche benötigt werden.
ms.assetid: 834E317F-CFFD-460C-9F89-793081BA1853
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ae1bf4ad1ca308fb3c93a36c4b3478aabdb0f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993511"
---
# <a name="how-a-tiled-resources-area-is-tiled"></a>Kacheln eines gekachelten Ressourcenbereichs

Wenn Sie eine Kachel Ressource erstellen, bestimmen Dimensionen, Format Elementgröße und Anzahl von Mipmaps und/oder Array Slices (falls zutreffend) die Anzahl der Kacheln, die für die gesamte Oberfläche benötigt werden. Das Pixel-/bytelayout in Kacheln wird von der-Implementierung bestimmt. Die Anzahl der Pixel, die je nach Format Elementgröße in eine Kachel passen, ist fest und identisch, unabhängig davon, ob Sie einen Standardwert verwenden oder nicht.

Die Anzahl der Kacheln, die von einer bestimmten Oberflächen Größe und Format Elementbreite verwendet werden, ist basierend auf den Tabellen in den folgenden Abschnitten gut definiert und vorhersagbar. Für Ressourcen, die Mipmaps oder Fälle enthalten, in denen keine Kachel durch Oberflächen Dimensionen aufgefüllt wird, gibt es einige Einschränkungen, die unter [MipMap-Verpackung](mipmap-packing.md)erläutert werden.

Unterschiedliche gekachelte Ressourcen können auf denselben Arbeitsspeicher mit unterschiedlichen Formaten zeigen, wenn Anwendungen nicht auf die Ergebnisse des Schreibvorgangs in den Arbeitsspeicher mit einem Format und dem Lesen mit einem anderen Format beruhen. In eingeschränkten Fällen können sich Anwendungen jedoch auf die Ergebnisse des Schreibvorgangs in den Arbeitsspeicher mit einem Format und das Lesen mit einem anderen-Format verlassen, wenn sich die Formate in derselben Format Familie befinden (d. h., Sie haben dasselbe typlose übergeordnete Format). Beispielsweise sind DXGI \_ \_ -Format R8G8B8A8 \_ unorm und DXGI- \_ Format \_ R8G8B8A8 \_ uint kompatibel, aber nicht mit dem DXGI- \_ Format \_ R16G16 \_ unorm. Eine Anwendung muss alle Ressourcen Eigenschaften im Einklang mit allen Ressourcen Eigenschaften abgleichen, um Daten zwischen zwei Texturen neu interpretieren zu können, da Kachel Muster sehr konservativ nicht definiert sind. Natürlich ist das Format jedoch weniger Lax. Die Formate müssen nur wie oben dargestellt kompatibel sein. Eine Ausnahme besteht darin, dass das Löschen von Daten von einem Format in ein anderes klar definiert ist: Wenn eine Kachel vollständig 0 für alle Bits enthält, kann diese Kachel in jedem Format verwendet werden, das diese Speicherinhalte als 0 (unabhängig vom Speicher Layout) interpretiert. Daher kann eine Kachel mit dem Format DXGI- \_ Format \_ R8 unorm auf 0x00 \_ und dann mit einem Format wie DXGI- \_ Format R32G32 float gelöscht werden, und es wird angezeigt, dass \_ \_ der Inhalt weiterhin (0,0 f, 0,0 f) ist.

Das Layout der Daten in einer Kachel hängt möglicherweise von den Ressourcen Eigenschaften, der untergeordneten Quelle, in der es sich befindet, und der Kachel Position innerhalb der untergeordneten Quelle ab. Die wichtigsten Ausnahmen sind oben dargestellt: kompatible Formate mit anderen Ressourcen Eigenschaften, die gleich sind, und wenn alle texeln dasselbe Muster aufweisen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unterteilung von Texture2D- und Texture2DArray-Unterressourcen](texture2d-and-texture2darray-subresource-tiling.md)<br/> | Diese Tabellen zeigen, wie [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) und [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) -unter Ressourcen nebeneinander angeordnet werden. <br/>                                                                                                          |
| [Unterteilung von Texture3D-Unterressourcen](texture3d-subresource-tiling.md)<br/>                                       | Diese Tabelle zeigt, wie [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) -unter Ressourcen nebeneinander angeordnet werden. <br/>                                                                                                                                                                            |
| [Pufferanordnung](buffer-tiling.md)<br/>                                                                     | Eine [Puffer](overviews-direct3d-11-resources-buffers.md) Ressource ist in Kacheln mit 64 KB unterteilt, wobei ein Leerzeichen in der letzten Kachel leer ist, wenn die Größe kein Vielfaches von 64 KB ist.<br/>                                                                                                  |
| [MipMap-Verpackung](mipmap-packing.md)<br/>                                                                   | Abhängig von der [Ebene](tiled-resources-features-tiers.md) der Unterstützung für gekachelte Ressourcen folgen Mipmaps mit bestimmten Dimensionen nicht den standardmäßigen Kachel Formen und werden als alle in einer Weise, die für die Anwendung nicht transparent ist, in eine Weise verpackt. <br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Kachel Ressourcen](creating-tiled-resources.md)
</dt> </dl>

 

