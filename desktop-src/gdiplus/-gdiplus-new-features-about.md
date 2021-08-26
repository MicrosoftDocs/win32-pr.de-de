---
description: In den folgenden Abschnitten werden einige der neuen Features in Windows GDI+.
ms.assetid: 0257a23c-560e-472e-863a-6ab5881dc156
title: Neue Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab303cd00f494e06d7567d93c9698878e02d178a7b4f31d230a4b47cafe279b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014860"
---
# <a name="new-features"></a>Neue Funktionen

In den folgenden Abschnitten werden einige der neuen Features in Windows GDI+.

-   [Farbverlaufspinsel](#gradient-brushes)
-   [Kardinale Splines](#cardinal-splines)
-   [Unabhängige Pfadobjekte](#independent-path-objects)
-   [Transformationen und das Matrixobjekt](#transformations-and-the-matrix-object)
-   [Skalierbare Regionen](#scalable-regions)
-   [Alphablending](#alpha-blending)
-   [Unterstützung für mehrere Bildformate](#support-for-multiple-image-formats)

## <a name="gradient-brushes"></a>Farbverlaufspinsel

GDI+ erweitert Windows Graphics Device Interface (GDI) durch die Bereitstellung linearer Farbverlaufs- und Pfadverlaufspinsel zum Auffüllen von Formen, Pfaden und Regionen. Farbverlaufspinsel können auch verwendet werden, um Linien, Kurven und Pfade zu zeichnen. Wenn Sie eine Form mit einem Pinsel mit linearem Farbverlauf füllen, ändert sich die Farbe allmählich, wenn Sie sich über die Form bewegen. Angenommen, Sie erstellen einen Pinsel mit horizontalem Farbverlauf, indem Sie blau am linken Rand einer Form und grün am rechten Rand angeben. Wenn Sie diese Form mit dem Pinsel für den horizontalen Farbverlauf füllen, ändert sie sich allmählich von blau in grün, wenn Sie sich vom linken Rand zum rechten Rand bewegen. Auf ähnliche Weise ändert eine Form, die mit einem Pinsel mit vertikalem Farbverlauf gefüllt ist, die Farbe, wenn Sie von oben nach unten wechseln. Die folgende Abbildung zeigt eine Ellipse, die mit einem horizontalen Farbverlaufspinsel gefüllt ist, und einen Bereich, der mit einem diagonalen Farbverlaufspinsel gefüllt ist.

![Abbildung einer Form, die durch einen horizontalen Farbverlauf gefüllt ist und eine Form mit einem diagonalen Farbverlauf](images/aboutgdip01-art01.png)

Wenn Sie eine Form mit einem Pfadverlaufspinsel füllen, haben Sie eine Vielzahl von Optionen, um anzugeben, wie sich die Farben ändern, wenn Sie von einem Teil der Form zu einem anderen wechseln. Eine Möglichkeit besteht in einer Mittelpunktfarbe und einer Begrenzungsfarbe, sodass sich die Pixel schrittweise von einer Farbe zur anderen ändern, wenn Sie sich von der Mitte der Form zu den äußeren Rändern bewegen. Die folgende Abbildung zeigt einen Pfad (erstellt aus einem Paar von Bézier-Splines), der mit einem Pfadverlaufspinsel gefüllt ist.

![Abbildung einer Form, die einem Unendlichkeitszeichen ähnelt, das von Blau gefüllt ist, wo sich die Hälften an den Rändern zum Wasser treffen](images/aboutgdip01-art02.png)

## <a name="cardinal-splines"></a>Kardinale Splines

GDI+ unterstützt Kardinalsplines, die in GDI nicht unterstützt werden. Eine Kardinalspline ist eine Sequenz einzelner Kurven, die zu einer größeren Kurve verbunden sind. Die Spline wird durch ein Array von Punkten angegeben und durchläuft jeden Punkt in diesem Array. Eine Kardinal-Spline durchläuft jeden Punkt im Array reibungslos (keine spitzen Ecken) und ist daher genauer als ein Pfad, der durch verbindende gerade Linien erstellt wird. Die folgende Abbildung zeigt zwei Pfade: einen, der durch Verbinden von geraden Linien und einer als Kardinal-Spline erstellt wurde.

![Abbildung, die die gleichen fünf Punkte zweimal zeigt: einmal durch einen Kardinal-Spline verbunden, der andere durch Liniensegmente](images/aboutgdip01-art03.png)

## <a name="independent-path-objects"></a>Unabhängige Pfadobjekte

In GDI gehört ein Pfad zu einem Gerätekontext, und der Pfad wird zerstört, wenn er gezeichnet wird. Mit GDI+ wird das Zeichnen von einem [**Graphics-Objekt**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ausgeführt, und Sie können mehrere [**GraphicsPath-Objekte**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) erstellen und verwalten, die vom **Graphics-Objekt getrennt** sind. Ein **GraphicsPath-Objekt** wird durch die Zeichnungsaktion nicht zerstört, sodass Sie dasselbe **GraphicsPath-Objekt** verwenden können, um einen Pfad mehrmals zu zeichnen.

## <a name="transformations-and-the-matrix-object"></a>Transformationen und das Matrixobjekt

GDI+ stellt das [**Matrix-Objekt**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) zur Verfügung, ein leistungsstarkes Tool, das Transformationen (Drehungen, Übersetzungen und so weiter) einfach und flexibel macht. Ein Matrixobjekt funktioniert in Verbindung mit den objekten, die transformiert werden. Ein [**GraphicsPath-Objekt**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) verfügt beispielsweise über eine [**GraphicsPath::Transform-Methode,**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) die die Adresse eines **Matrix-Objekts** als Argument empfängt. Eine einzelne 3×3-Matrix kann eine Transformation oder eine Sequenz von Transformationen speichern. Die folgende Abbildung zeigt einen Pfad vor und nach einer Sequenz von zwei Transformationen (zuerst skalieren, dann drehen).

![Abbildung, die die Kontur einer Form zeigt, dann die gleiche Kontur, aber schmaler und gedreht](images/aboutgdip01-art04.png)

## <a name="scalable-regions"></a>Skalierbare Regionen

GDI+ GDI wird durch die Unterstützung von Regionen stark erweitert. In GDI werden Regionen in Gerätekoordinaten gespeichert, und die einzige Transformation, die auf eine Region angewendet werden kann, ist eine Übersetzung. GDI+ speichert Regionen in Weltkoordinaten und ermöglicht es einer Region, jede Transformation (z. B. Skalierung) zu durchlaufen, die in einer Transformationsmatrix gespeichert werden kann. Die folgende Abbildung zeigt einen Bereich vor und nach einer Sequenz von drei Transformationen: Skalieren, Drehen und Übersetzen.

![Abbildung, die eine Form zeigt, die auf Koordinatenachsen zentriert ist, dann die gleiche Form, aber größer, gedreht und nach rechts übersetzt](images/aboutgdip01-art05.png)

## <a name="alpha-blending"></a>Alphablending

Beachten Sie, dass Sie in der vorherigen Abbildung den nicht transformierten Bereich (mit Rot gefüllt) durch den transformierten Bereich (gefüllt mit einem Schraffraffenpinsel) sehen können. Dies wird durch Alphablending ermöglicht, das von der GDI+. Mit alpha blending können Sie die Transparenz einer Füllfarbe angeben. Eine transparente Farbe wird mit der Hintergrundfarbe kombiniert– desto transparenter machen Sie eine Füllfarbe, desto mehr wird der Hintergrund durch angezeigt. Die folgende Abbildung zeigt vier Ellipsen, die mit der gleichen Farbe (rot) auf verschiedenen Transparenzebenen gefüllt sind.

![Abbildung, die vier Ellipsen unterschiedlicher Transparenz zeigt, die ein halbtransparentes Rechteck überlappen](images/aboutgdip01-art06.png)

## <a name="support-for-multiple-image-formats"></a>Unterstützung für mehrere Bildformate

GDI+ stellt die [**Klassen Image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)und [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) zur Verfügung, mit denen Sie Bilder in einer Vielzahl von Formaten laden, speichern und bearbeiten können. Die folgenden Formate werden unterstützt:

-   BMP
-   GIF (Graphics Interchange Format)
-   JPEG
-   EXIF
-   PNG
-   TIFF
-   ICON
-   WMF
-   EMF

 

 



