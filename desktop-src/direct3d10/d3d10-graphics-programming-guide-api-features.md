---
description: Die Direct3D 10-Grafikpipeline stellt eine grundlegende Architekturänderung dar, die von Grund auf in Hardware und Software neu erstellt wurde, um die nächste Generation von Spielen und 3D-Multimediaanwendungen zu fördern.
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: API-Features (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 416018fcddf2643ba9fbc8e633ec2f636b8158ff329780a55205034e5dbbe240
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858660"
---
# <a name="api-features-direct3d-10"></a>API-Features (Direct3D 10)

Die Direct3D 10-Grafikpipeline stellt eine grundlegende Architekturänderung dar, die von Grund auf in Hardware und Software neu erstellt wurde, um die nächste Generation von Spielen und 3D-Multimediaanwendungen zu fördern. Es wird das Windows Display Driver Model (WDDM) verwendet, das Leistungs- und Verhaltensverbesserungen ermöglicht, z. B. virtuellen GPU-Arbeitsspeicher.

Entwickler, die mit Direct3D 9 vertraut sind, werden eine Reihe von Funktionserweiterungen und Leistungsverbesserungen in Direct3D 10 entdecken, einschließlich:

-   Die Fähigkeit, ganze Primitive in der neuen [geometry-shader-Phase](/previous-versions//bb205146(v=vs.85))zu verarbeiten.
-   Die Möglichkeit, pipelinegenerierte Scheitelpunktdaten mithilfe der [Streamausgabephase](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md)in den Arbeitsspeicher auszugeben.
-   Organisation des Pipelinezustands in 5 unveränderliche [Zustandsobjekte,](d3d10-graphics-programming-guide-api-features-state-objects.md)wodurch eine schnelle Konfiguration der Pipeline ermöglicht wird.
-   Organisation von Shaderkonstanten in [konstanten Puffern,](d3d10-graphics-programming-guide-resources-types.md)wodurch der Bandbreitenaufwand für die Bereitstellung von Shaderkonstantendaten minimiert wird.
-   Die Möglichkeit zum Austausch und Einrichten von pro primitivem Material mithilfe eines Geometrie-Shaders.
-   Neue [Ressourcentypen](d3d10-graphics-programming-guide-resources-types.md) (einschließlich Texturarrays, die über Shader indiziert werden können) und Ressourcenformate.
-   Verbesserte Generalisierung des Ressourcenzugriffs mithilfe einer [Ansicht](d3d10-graphics-programming-guide-resources-access-views.md).
-   Legacy-Hardwarefunktionsbits (Caps) wurden zugunsten eines umfangreichen Satzes garantierter Funktionen entfernt, die auf Direct3D 10-Klassenhardware (mindestens) ausgerichtet sind.
-   [Mehrstufige Runtime:](d3d10-graphics-programming-guide-api-features-layers.md) Die Direct3D 10-API wird mit Ebenen erstellt, beginnend mit der grundlegenden Funktionalität im Kern und der Erstellung optionaler und Entwicklerunterstützungsfunktionen (Debuggen usw.) in äußeren Ebenen.
-   Vollständige HLSL-Integration: Alle Direct3D 10-Shader werden in HLSL geschrieben und mit dem [Common-Shader-Kern](../direct3dhlsl/dx-graphics-hlsl-common-core.md)implementiert.
-   Eine erhöhung der Anzahl von Renderzielen, Texturen und Samplern. Es gibt auch keine Längenbeschränkung für Shader.
-   Ganzzahlige und bitweise Shadervorgänge.
-   Rücklesen einer Tiefen-/Schablonenoberfläche oder einer Multisampled-Ressource, sobald sie nicht mehr als Renderziel gebunden ist.
-   Multisampled Alpha-to-Coverage-Unterstützung.

Es gibt weitere Verhaltensunterschiede, die Direct3D 9-Entwickler ebenfalls beachten sollten (siehe [Überlegungen zu Direct3D 9 zu Direct3D 10](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).

Hier finden Sie eine Liste der Direct3D 9-Features, die entweder nicht mehr unterstützt werden oder in Direct3D 10 überarbeitet wurden (siehe [Veraltete Features).](d3d10-graphics-programming-guide-api-features-deprecated.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch für Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
