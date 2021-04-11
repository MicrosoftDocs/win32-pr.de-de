---
description: Die Bump-Zuordnung ist eine spezielle Form der Glanz-oder diffusen Umgebungs Zuordnung, die die Reflektionen von fein Mosaik Objekten simuliert, ohne dass extrem hohe Polygon Zahlen erforderlich sind.
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: Bump-Zuordnung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dba4621568f595eae965941168ad6930e183f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127389"
---
# <a name="bump-mapping-direct3d-9"></a>Bump-Zuordnung (Direct3D 9)

Die Bump-Zuordnung ist eine spezielle Form der Glanz-oder diffusen Umgebungs Zuordnung, die die Reflektionen von fein Mosaik Objekten simuliert, ohne dass extrem hohe Polygon Zahlen erforderlich sind. Die von Direct3D implementierte Bump-Zuordnung kann genau als Pixel übergreifende Textur Koordinate für Glanz-oder diffuse Umgebungs Zuordnungen beschrieben werden, da Sie Informationen über die Kontur der Bump Map in Bezug auf Delta Werte bereitstellen, die das System für die Texturkoordinaten eines Umgebungs Diagramms in der nächsten Textur Phase anwendet. Die Delta Werte werden im Pixel Format der Bump Map-Oberfläche codiert (Weitere Informationen finden Sie unter [Bump Map Pixel Formats](bump-map-pixel-formats.md)).

Die Bump-Zuordnung basiert auf der Mischung mehrerer Texturen. Dies bedeutet, dass das Gerät mindestens zwei Mischungs Phasen unterstützen muss. eine für die Bump Map und eine für eine Umgebungs Zuordnung. Mindestens drei Textur Mischungs Phasen sind erforderlich, um eine zusätzliche Basis Textur Zuordnung anzuwenden. Dies ist der häufigste Fall. Im folgenden Diagramm werden die Beziehungen zwischen der Basis Textur, der Bump Map und der Umgebungs Zuordnung in der Textur Mischungs kaskadieren angezeigt.

![Diagramm der Textur Mischungs kaskadieren](images/bumpmap-tcascade.png)

Sie müssen die Textur Stufen entsprechend vorbereiten, um die Bump-Zuordnung zu aktivieren. In den folgenden Themen wird die Bump-Zuordnung eingeführt, und es wird erläutert, wie Sie Sie in Ihren Anwendungen verwenden können:

-   [Peermap-Pixel Formate](bump-map-pixel-formats.md)
-   [Bump-Mapping-Formeln](bump-mapping-formulas.md)
-   [Verwenden der Bump-Zuordnung](using-bump-mapping.md)

Direct3D bietet keine Unterstützung für Höhen Zuordnungen. Sie sind lediglich ein nützliches Format, in dem Sie die Konturdaten speichern und visualisieren können. In Ihrer Anwendung können Sie die Informationen in einem beliebigen Format speichern oder sogar eine prozedurale Bump Map generieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel Pipeline](pixel-pipeline.md)
</dt> </dl>

 

 



