---
title: Kacheln des Bereichs einer gekachelten Ressource
description: Wenn Sie eine gekachelte Ressource erstellen, bestimmen die Dimensionen, die Formatelementgröße und die Anzahl der Mipmaps und/oder Arrayslices (falls zutreffend) die Anzahl der Kacheln, die zum Sichern der gesamten Oberfläche erforderlich sind.
ms.assetid: 834E317F-CFFD-460C-9F89-793081BA1853
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75feaa7852a7bc2567d7b4983ff4d59d12b516f5feb4be2886f93294f77bd6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633220"
---
# <a name="how-a-tiled-resources-area-is-tiled"></a>Kacheln des Bereichs einer gekachelten Ressource

Wenn Sie eine gekachelte Ressource erstellen, bestimmen die Dimensionen, die Formatelementgröße und die Anzahl der Mipmaps und/oder Arrayslices (falls zutreffend) die Anzahl der Kacheln, die zum Sichern der gesamten Oberfläche erforderlich sind. Das Pixel-/Bytelayout innerhalb von Kacheln wird durch die -Implementierung bestimmt. Die Anzahl der Pixel, die in eine Kachel passen, ist abhängig von der Formatelementgröße fest und identisch, unabhängig davon, ob Sie ein Standard-Swizzle verwenden oder nicht.

Die Anzahl der Kacheln, die von einer bestimmten Oberflächengröße und Formatelementbreite verwendet werden, ist basierend auf den Tabellen in den folgenden Abschnitten klar definiert und vorhersagbar. Für Ressourcen, die Mipmaps oder Fälle enthalten, in denen Oberflächendimensionen keine Kachel füllen, sind einige Einschränkungen vorhanden und werden unter [Mipmap-Packen erläutert.](mipmap-packing.md)

Unterschiedliche gekachelte Ressourcen können auf identischen Arbeitsspeicher mit unterschiedlichen Formaten verweisen, solange Anwendungen nicht auf die Ergebnisse des Schreibens in den Arbeitsspeicher mit einem Format und lesen mit einem anderen angewiesen sind. Unter eingeschränkten Umständen können Sich Anwendungen jedoch auf die Ergebnisse des Schreibens in den Arbeitsspeicher mit einem Format und lesen mit einem anderen verlassen, wenn sich die Formate in derselben Formatfamilie befinden (d. h. sie haben das gleiche typlose übergeordnete Format). DxGI FORMAT \_ \_ R8G8B8A8 UNORM und DXGI FORMAT R8G8B8A8 UINT sind beispielsweise miteinander kompatibel, aber nicht \_ \_ mit \_ \_ DXGI FORMAT \_ \_ R16G16 \_ UNORM. Eine Anwendung muss alle Ressourceneigenschaften konservativ ab suchen, um Daten zwischen zwei Texturen neu zu interpretierten, da Kachelmuster sehr konservativ undefiniert sind. Natürlich ist das Format jedoch laxer. Die Formate müssen nur wie oben dargestellt kompatibel sein. Eine Ausnahme ist, dass die Daten von einem Formataliasing zu einem anderen klar definiert sind: Wenn eine Kachel für alle Bits vollständig 0 enthält, kann diese Kachel mit jedem Format verwendet werden, das diese Speicherinhalte als 0 interpretiert (unabhängig vom Speicherlayout). Daher könnte eine Kachel in 0x00 im Format DXGI FORMAT R8 UNORM löschen und dann mit einem Format wie DXGI FORMAT R32G32 FLOAT verwendet werden, und es scheint, dass der Inhalt noch \_ \_ \_ \_ \_ \_ (0,0f, 0,0f) ist.

Das Layout der Daten innerhalb einer Kachel kann von Ressourceneigenschaften, der Unterressource, in der sie sich befinden, und der Kachelposition innerhalb der Unterressource abhängen. Die wichtigsten Ausnahmen sind oben dargestellt: Kompatible Formate mit anderen Ressourceneigenschaften sind gleich, und wenn alle Texel das gleiche Muster aufweisen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                             | Beschreibung                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unterteilung von Texture2D- und Texture2DArray-Unterressourcen](texture2d-and-texture2darray-subresource-tiling.md)<br/> | Diese Tabellen zeigen, [**wie Texture2D-**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) [**und Texture2DArray-Unterressourcen**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) nebeneinander angeordnet werden. <br/>                                                                                                          |
| [Unterteilung von Texture3D-Unterressourcen](texture3d-subresource-tiling.md)<br/>                                       | Diese Tabelle zeigt, [**wie Texture3D-Unterressourcen**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) gekachelt werden. <br/>                                                                                                                                                                            |
| [Pufferanordnung](buffer-tiling.md)<br/>                                                                     | Eine [Pufferressource](overviews-direct3d-11-resources-buffers.md) ist in Kacheln mit 64 KB unterteilt, mit einem leeren Platz auf der letzten Kachel, wenn die Größe nicht ein Vielfaches von 64 KB ist.<br/>                                                                                                  |
| [MipMap-Verpackung](mipmap-packing.md)<br/>                                                                   | Abhängig von [](tiled-resources-features-tiers.md) der Ebene der Unterstützung für gekachelte Ressourcen folgen Mipmaps mit bestimmten Dimensionen nicht den standardmäßigen Kachelformen und werden als alle in einer Weise miteinander gepackt, die für die Anwendung nicht transparent ist. <br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von gekachelten Ressourcen](creating-tiled-resources.md)
</dt> </dl>

 

