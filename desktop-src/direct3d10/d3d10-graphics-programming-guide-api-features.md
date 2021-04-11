---
description: Die Grafik Pipeline Direct3D 10 stellt eine grundlegende Architektur Änderung dar, die von Grund auf für Hardware und Software neu erstellt wird, um die nächste Generation von spielen und 3D-Multimedia-Anwendungen zu unterhalten.
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: API-Features (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab12285509441bb429c78d995e68ed1753ceb5bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214086"
---
# <a name="api-features-direct3d-10"></a>API-Features (Direct3D 10)

Die Grafik Pipeline Direct3D 10 stellt eine grundlegende Architektur Änderung dar, die von Grund auf für Hardware und Software neu erstellt wird, um die nächste Generation von spielen und 3D-Multimedia-Anwendungen zu unterhalten. Es verwendet das Windows-Anzeigetreiber Modell (WDDM), das Leistungs-und Verhaltens Verbesserungen wie den virtuellen GPU-Speicher ermöglicht.

Entwickler, die mit Direct3D 9 vertraut sind, werden eine Reihe von funktionalen Erweiterungen und Leistungsverbesserungen in Direct3D 10 ermitteln, einschließlich:

-   Die Fähigkeit zum Verarbeiten ganzer primitiver Elemente in der neuen [Geometry-Shader-Stufe](/previous-versions//bb205146(v=vs.85)).
-   Die Möglichkeit zum Ausgeben von Pipeline generierten Vertex-Daten in den Arbeitsspeicher mithilfe der [Stream-Output-Phase](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).
-   Organisation des Pipeline Zustands in 5 unveränderliche [Zustands Objekte](d3d10-graphics-programming-guide-api-features-state-objects.md), die eine schnelle Konfiguration der Pipeline ermöglichen.
-   Organisation von shaderkonstanten in [Konstante Puffer](d3d10-graphics-programming-guide-resources-types.md), wodurch der Bandbreiten Aufwand für die Bereitstellung von Shader-Konstanten Daten minimiert wird.
-   Die Möglichkeit, das austauschen und einrichten pro primitiver Materialien mithilfe eines Geometry-Shaders durchzuführen.
-   Neue [Ressourcentypen](d3d10-graphics-programming-guide-resources-types.md) (einschließlich Textur Arrays, die von Shader indiziert werden können) und Ressourcen Formate.
-   Erhöhung der Generalisierung des Ressourcen Zugriffs mithilfe einer [Ansicht](d3d10-graphics-programming-guide-resources-access-views.md).
-   Ältere hardwarefunktionsbits (Caps) wurden zugunsten eines umfangreichen Satzes von garantierten Funktionen entfernt, die auf Direct3D 10-Class Hardware (minimal) ausgerichtet sind.
-   [Geschichtete Laufzeit](d3d10-graphics-programming-guide-api-features-layers.md) : die Direct3D 10-API wird mit Ebenen erstellt, beginnend mit den grundlegenden Funktionen im Kern und der Erstellung Optionaler und Entwickler-Assist-Funktionen (Debug usw.) in äußeren Ebenen.
-   Vollständige HLSL-Integration-alle Direct3D 10-Shader werden in HLSL geschrieben und mit dem [Common-Shader-Kern](../direct3dhlsl/dx-graphics-hlsl-common-core.md)implementiert.
-   Eine Erhöhung der Anzahl von renderzielen, Texturen und Samplern. Es gibt auch keine Längen Beschränkung für Shader.
-   Ganzzahlige und bitweise shadervorgänge.
-   Ein Rückschlag einer tiefen-/Schablone-Oberfläche oder einer Multisampling-Ressource, sobald Sie nicht mehr als Renderziel gebunden ist.
-   Multisampling-Unterstützung für Alpha-zu-Abdeckung.

Es gibt zusätzliche Verhaltensunterschiede, die Direct3D 9-Entwicklern auch bekannt sein sollten (siehe [Direct3D 9 bis Direct3D 10 Überlegungen](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).

Im folgenden finden Sie eine Liste der Direct3D 9-Features, die entweder nicht mehr unterstützt werden oder in Direct3D 10 geändert wurden (siehe [Veraltete Features](d3d10-graphics-programming-guide-api-features-deprecated.md)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmier Handbuch für Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
