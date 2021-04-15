---
description: Sie können einen Farbverlaufs Pinsel verwenden, um eine Form mit einer allmählich veränderlichen Farbe auszufüllen.
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: Auffüllen von Formen mit einem Farbverlaufs Pinsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6784d0bfd59fd37f217e8d7a1cdd230348807d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994254"
---
# <a name="filling-shapes-with-a-gradient-brush"></a>Auffüllen von Formen mit einem Farbverlaufs Pinsel

Sie können einen Farbverlaufs Pinsel verwenden, um eine Form mit einer allmählich veränderlichen Farbe auszufüllen. Beispielsweise können Sie einen horizontalen Farbverlauf verwenden, um eine Form mit Farben auszufüllen, die sich allmählich ändert, wenn Sie vom linken Rand der Form zum rechten Rand wechseln. Stellen Sie sich ein Rechteck mit einem linken Rand vor, der schwarz ist (dargestellt durch die rote, grüne und blaue Komponente 0, 0, 0) und einen rechten roten Rand (dargestellt durch 255, 0, 0). Wenn das Rechteck 256 Pixel breit ist, ist die rote Komponente eines gegebenen Pixels eine größer als die rote Komponente des Pixels links. Das äußteste linke Pixel in einer Zeile hat Farbkomponenten (0, 0, 0), das zweite Pixel hat (1, 0, 0), das dritte Pixel hat (2, 0, 0) usw., bis Sie zum äußersten äußersten Pixel mit Farbkomponenten (255, 0,0) gelangen. Diese interpoliert Farbwerte bilden den Farbverlauf.

Die Farbe eines linearen Farbverlaufs ändert sich, wenn Sie horizontal, vertikal oder parallel zu einer angegebenen schrägen Linie wechseln. Ein Pfad Farbverlauf ändert die Farbe, wenn Sie zum inneren und zur Grenze eines Pfads wechseln. Sie können Pfad Farbverläufe anpassen, um eine Vielzahl von Effekten zu erzielen.

GDI+ stellt die Klassen [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) und [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) bereit, von denen beide von der [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) -Klasse erben.

In den folgenden Themen werden die Farbverläufe linear und Path ausführlicher behandelt:

-   [Erstellen eines linearen Farbverlaufs](-gdiplus-creating-a-linear-gradient-use.md)
-   [Erstellen eines Pfad Farbverlaufs](-gdiplus-creating-a-path-gradient-use.md)
-   [Anwenden der Gamma Korrektur auf einen Farbverlauf](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 



