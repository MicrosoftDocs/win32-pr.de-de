---
description: Die Bump-Zuordnung ist eine besondere Form der spezifikations- oder diffusen Umgebungszuordnung, die die Reflektionen von objekten mit feinen Mosaiken simuliert, ohne dass eine extrem hohe Polygonanzahl erforderlich ist.
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: Bump-Zuordnung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb10a3a01ff3b7989cd7c44f95d6980cb08a86c00b3e9a0fc02173e349d4968
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805829"
---
# <a name="bump-mapping-direct3d-9"></a>Bump-Zuordnung (Direct3D 9)

Die Bump-Zuordnung ist eine besondere Form der spezifikations- oder diffusen Umgebungszuordnung, die die Reflektionen von objekten mit feinen Mosaiken simuliert, ohne dass eine extrem hohe Polygonanzahl erforderlich ist. Die von Direct3D implementierte Bumpzuordnung kann genau als Texturkoordinatenverfall pro Pixel von specularen oder diffusen Umgebungszuordnungen beschrieben werden, da Sie Informationen über die Kontur der Bumpmap in Bezug auf Deltawerte bereitstellen, die das System auf die Texturkoordinaten Von Ihnen und v einer Umgebungskarte in der nächsten Texturphase angewendet wird. Die Deltawerte werden im Pixelformat der Bumpmapoberfläche codiert (siehe [Bump Map Pixel Formats](bump-map-pixel-formats.md)).

Die Bumpzuordnung basiert auf der Mischung mehrerer Texturen. Dies bedeutet, dass das Gerät mindestens zwei Mischungsphasen unterstützen muss. eine für die Bumpmap und eine andere für eine Umgebungskarte. Es sind mindestens drei Texturmischungsphasen erforderlich, um eine zusätzliche Basistexturzuordnung anzuwenden. Dies ist der häufigste Fall. Das folgende Diagramm zeigt die Beziehungen zwischen der Basistextur, der Bumpmap und der Umgebungszuordnung in der Texturmischungskaskade.

![Diagramm der Kaskadierung der Texturmischung](images/bumpmap-tcascade.png)

Sie müssen die Texturstufen entsprechend vorbereiten, um die Bumpzuordnung zu aktivieren. In den folgenden Themen wird die Bumpzuordnung und details zur Verwendung in Ihren Anwendungen behandelt:

-   [Pixelformate für "Bump Map"](bump-map-pixel-formats.md)
-   [Formeln für die Bumpzuordnung](bump-mapping-formulas.md)
-   [Verwenden der Bumpzuordnung](using-bump-mapping.md)

Direct3D unterstützt keine nativ unterstützten Höhenzuordnungen. sie sind lediglich ein praktisches Format zum Speichern und Visualisieren von Konturdaten. Ihre Anwendung kann Konturinformationen in einem beliebigen Format speichern oder sogar eine prozedurale Bumpmap generieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelpipeline](pixel-pipeline.md)
</dt> </dl>

 

 



