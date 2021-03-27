---
title: Pipeline Zugriff auf gekachelte Ressourcen
description: Gekachelte Ressourcen können in Shader-Ressourcen Ansichten (SRV), renderzielsichten (RTV), Datenquellen Sichten (Datenquellen Sicht) und unsortierter Zugriffs Ansichten (UAV) sowie einigen Bindungs Punkten verwendet werden, bei denen Sichten nicht verwendet werden, wie z. b. Vertex-Puffer Bindungen.
ms.assetid: D0BC0B6C-2325-4EAF-9E80-E748F58045B1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4a183fcaee90d84985a09c83826a4ad0b6d646
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729256"
---
# <a name="pipeline-access-to-tiled-resources"></a>Pipeline Zugriff auf gekachelte Ressourcen

Gekachelte Ressourcen können in Shader-Ressourcen Ansichten (SRV), renderzielsichten (RTV), Datenquellen Sichten (Datenquellen Sicht) und unsortierter Zugriffs Ansichten (UAV) sowie einigen Bindungs Punkten verwendet werden, bei denen Sichten nicht verwendet werden, wie z. b. Vertex-Puffer Bindungen. Eine Liste der unterstützten Bindungen finden Sie unter Parameter für die [Kachel Ressourcen Erstellung](tiled-resource-creation-parameters.md). Kopier \* Vorgänge funktionieren auch für gekachelte Ressourcen.

Wenn mehrere Kachel Koordinaten in einer oder mehreren Ansichten an denselben Speicherort gebunden sind, werden Lese-und Schreibvorgänge aus unterschiedlichen Pfaden desselben Speichers in einer nicht deterministischen und nicht wiederholbaren Reihenfolge von Speicherzugriffen ausgeführt.

Wenn alle Kacheln hinter einer Speicherzugriffs Beanspruchung von einem Shader eindeutigen Kacheln zugeordnet sind, ist das Verhalten auf allen Implementierungen mit der Oberfläche identisch, die den gleichen Speicherinhalt auf nicht gekachelte Weise aufweisen.

In diesem Abschnitt finden Sie weitere Informationen über den Pipeline Zugriff auf gekachelte Ressourcen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                              | BESCHREIBUNG                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SRV-verhalten bei nicht zugeordneten Kacheln](srv-behavior-with-non-mapped-tiles.md)<br/>                            | Das Verhalten von Lesevorgängen in der Shader-Ressourcen Ansicht (SRV), die nicht zugeordnete Kacheln einschließen, hängt von der Hardwareunterstützung ab. <br/>                                          |
| [UAV-verhalten bei nicht zugeordneten Kacheln](uav-behavior-with-non-mapped-tiles.md)<br/>                            | Das Verhalten von Lese-und Schreibvorgängen für die ungeordnete Zugriffs Ansicht (UAV) hängt von der Hardwareunterstützung ab. <br/>                                                            |
| [Rasterizerverhalten bei nicht zugeordneten Kacheln](rasterizer-behavior-with-non-mapped-tiles.md)<br/>              | In diesem Abschnitt wird das Verhalten des Rasterizers mit nicht zugeordneten Kacheln beschrieben.<br/>                                                                                              |
| [Kachelzugriffseinschränkungen bei doppelten Zuordnungen](tile-access-limitations-with-duplicate-mappings-.md)<br/> | In diesem Abschnitt werden Kachel Zugriffs Einschränkungen mit doppelten Zuordnungen beschrieben.<br/>                                                                                        |
| [Funktionen für Textur Stichproben der Kachel Ressourcen](tiled-resources-texture-sampling-features.md)<br/>              | In diesem Abschnitt werden die Funktionen für Textur Stichproben von Kacheln beschrieben<br/>                                                                                              |
| [Verfügbar machen von HLSL-Kacheln](hlsl-tiled-resources-exposure.md)<br/>                                      | Die neue Syntax von Microsoft High Level Shader Language (HLSL) ist erforderlich, um gekachelte Ressourcen in [Shader-Modell 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)zu unterstützen. <br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gekachelte Ressourcen](tiled-resources.md)
</dt> </dl>

 

