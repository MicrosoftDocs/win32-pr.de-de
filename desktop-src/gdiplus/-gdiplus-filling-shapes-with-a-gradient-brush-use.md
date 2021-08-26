---
description: Sie können einen Farbverlaufspinsel verwenden, um eine Form mit einer sich schrittweise ändernden Farbe zu füllen.
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: Auffüllen von Formen mit einem Farbverlaufspinsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d471e9d3e2d7fb6d151d50ab3b5f10212874180b4554769b5c00a552085391
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015050"
---
# <a name="filling-shapes-with-a-gradient-brush"></a>Auffüllen von Formen mit einem Farbverlaufspinsel

Sie können einen Farbverlaufspinsel verwenden, um eine Form mit einer sich schrittweise ändernden Farbe zu füllen. Beispielsweise können Sie einen horizontalen Farbverlauf verwenden, um eine Form mit Farbe zu füllen, die sich allmählich ändert, wenn Sie sich vom linken Rand der Form zum rechten Rand bewegen. Imagine ein Rechteck mit einem schwarzen linken Rand (dargestellt durch die roten, grünen und blauen Komponenten 0, 0, 0) und einem rechten, roten Rand (dargestellt durch 255, 0, 0). Wenn das Rechteck 256 Pixel breit ist, ist die rote Komponente eines bestimmten Pixels um eins größer als die rote Komponente des Pixels links. Das pixel ganz links in einer Zeile enthält Farbkomponenten (0, 0, 0), das zweite Pixel hat (1, 0, 0), das dritte Pixel hat (2, 0, 0) und so weiter, bis Sie zum äußersten rechten Pixel mit Farbkomponenten (255, 0, 0) kommen. Diese interpolierten Farbwerte machen den Farbverlauf aus.

Ein linearer Farbverlauf ändert die Farbe, wenn Sie sich horizontal, vertikal oder parallel zu einer angegebenen gestrichelten Linie bewegen. Ein Pfadfarbverlauf ändert die Farbe, wenn Sie sich um das Innere und die Begrenzung eines Pfads bewegen. Sie können Pfadverläufe anpassen, um eine Vielzahl von Effekten zu erzielen.

GDI+ die Klassen [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) und [**PathGradientBrush,**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) die beide von der [**Brush-Klasse erben.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)

In den folgenden Themen werden lineare und Pfadverläufe ausführlicher behandelt:

-   [Erstellen eines linearen Farbverlaufs](-gdiplus-creating-a-linear-gradient-use.md)
-   [Erstellen eines Pfadverlaufs](-gdiplus-creating-a-path-gradient-use.md)
-   [Anwenden der Gammakorrektur auf einen Farbverlauf](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 



