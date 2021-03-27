---
description: In den folgenden Abschnitten werden einige der neuen Features in Windows GDI+ beschrieben.
ms.assetid: 0257a23c-560e-472e-863a-6ab5881dc156
title: Neue Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca79ddb4cabd14cc2eaa2493033a78cc7377f8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751337"
---
# <a name="new-features"></a>Neue Funktionen

In den folgenden Abschnitten werden einige der neuen Features in Windows GDI+ beschrieben.

-   [Farbverlaufs Pinsel](#gradient-brushes)
-   [Kardinale Splines](#cardinal-splines)
-   [Unabhängige Pfad Objekte](#independent-path-objects)
-   [Transformationen und das Matrix Objekt](#transformations-and-the-matrix-object)
-   [Skalierbare Regionen](#scalable-regions)
-   [Alpha Blending](#alpha-blending)
-   [Unterstützung für mehrere Bildformate](#support-for-multiple-image-formats)

## <a name="gradient-brushes"></a>Farbverlaufs Pinsel

GDI+ wird auf Windows Graphics Device Interface (GDI) erweitert, indem lineare Farbverlaufs-und Pfad Farbverlaufs Pinsel zum Auffüllen von Formen, Pfaden und Bereichen bereitgestellt werden. Farbverlaufs Pinsel können auch zum Zeichnen von Linien, Kurven und Pfaden verwendet werden. Wenn Sie eine Form mit einem linearen Farbverlaufs Pinsel auffüllen, ändert sich die Farbe allmählich, wenn Sie sich über die Form bewegen. Nehmen Sie beispielsweise an, dass Sie einen horizontalen Farbverlaufs Pinsel erstellen, indem Sie am linken Rand einer Form blau und grün am rechten Rand angeben. Wenn Sie diese Form mit dem horizontalen Farbverlaufs Pinsel auffüllen, wechselt sie allmählich von blau in grün, wenn Sie von der linken Kante zum rechten Rand wechseln. Ebenso ändert sich eine mit einem vertikalen Farbverlaufs Pinsel gefüllte Form bei der Umstellung von oben nach unten. Die folgende Abbildung zeigt eine Ellipse mit einem horizontalen Farbverlaufs Pinsel und einem Bereich, der mit einem diagonalen Farbverlaufs Pinsel gefüllt ist.

![Abbildung einer Form, die von einem horizontalen Farbverlauf und einem durch einen diagonalen Farbverlauf aufgefüllt wird](images/aboutgdip01-art01.png)

Wenn Sie eine Form mit einem Pinsel mit dem Pfad Farbverlauf ausfüllen, haben Sie verschiedene Optionen, um anzugeben, wie sich die Farben ändern, wenn Sie von einem Teil der Form in einen anderen wechseln. Eine Möglichkeit besteht darin, eine Mittel Farbe und eine Begrenzungs Farbe zu haben, sodass sich die Pixel allmählich von einer Farbe zum anderen ändern, während Sie von der Mitte der Form zu den äußeren Rändern wechseln. Die folgende Abbildung zeigt einen Pfad (erstellt aus einem Paar von Bézier-Splines), das mit einem Pfad Farbverlaufs Pinsel gefüllt ist.

![Abbildung einer Form, die mit einem unendlichen Vorzeichen vergleichbar ist, von blau](images/aboutgdip01-art02.png)

## <a name="cardinal-splines"></a>Kardinale Splines

GDI+ unterstützt kardinale Splines, die in GDI nicht unterstützt werden. Bei einem kardinalspline handelt es sich um eine Sequenz von einzelnen Kurven, die mit einer größeren Kurve verknüpft sind. Der Spline wird durch ein Array von Punkten angegeben und durchläuft jeden Punkt in diesem Array. Ein kardinaler Spline verläuft nahtlos (keine spitzen Ecken) durch jeden Punkt im Array und ist daher besser verfeinert als ein Pfad, der durch das Verbinden von geraden Linien erstellt wird. In der folgenden Abbildung werden zwei Pfade dargestellt: eine, die durch das Verbinden von geraden Zeilen erstellt wurde, und eine, die als kardinale Spline

![die Abbildung zeigt zweimal die gleichen fünf Punkte: nach der Verbindungs Herstellung durch einen kardinalspline, der andere nach Liniensegmenten](images/aboutgdip01-art03.png)

## <a name="independent-path-objects"></a>Unabhängige Pfad Objekte

In GDI gehört ein Pfad zu einem Gerätekontext, und der Pfad wird zerstört, wenn er gezeichnet wird. Mit GDI+ wird das Zeichnen von einem [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt ausgeführt, und Sie können mehrere [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekte erstellen und verwalten, die vom **Grafik** Objekt getrennt sind. Ein **GraphicsPath** -Objekt wird von der Zeichnungs Aktion nicht zerstört, daher können Sie das gleiche **GraphicsPath** -Objekt verwenden, um einen Pfad mehrmals zu zeichnen.

## <a name="transformations-and-the-matrix-object"></a>Transformationen und das Matrix Objekt

GDI+ stellt das [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Objekt bereit, ein leistungsfähiges Tool, das Transformationen (Drehungen, Übersetzungen usw.) leicht und flexibel macht. Ein Matrix Objekt funktioniert in Verbindung mit den Objekten, die transformiert werden. Ein [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt verfügt beispielsweise über eine [**GraphicsPath:: Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) -Methode, die die Adresse eines **Matrix** Objekts als Argument empfängt. Eine einzelne 3 × 3-Matrix kann eine Transformation oder eine Sequenz von Transformationen speichern. Die folgende Abbildung zeigt einen Pfad vor und nach einer Sequenz von zwei Transformationen (erste Skalierung und Drehung).

![die Abbildung zeigt die Gliederung einer Form, die gleiche Kontur, aber schmaler und rotiert.](images/aboutgdip01-art04.png)

## <a name="scalable-regions"></a>Skalierbare Regionen

GDI+ wird in GDI mit der Unterstützung für Regionen erheblich erweitert. In GDI werden Regionen in Geräte Koordinaten gespeichert, und die einzige Transformation, die auf eine Region angewendet werden kann, ist eine Übersetzung. GDI+ speichert Regionen in globalen Koordinaten und ermöglicht es einer Region, jede Transformation (z. b. eine Skalierung) durchlaufen zu lassen, die in einer Transformationsmatrix gespeichert werden kann. Die folgende Abbildung zeigt einen Bereich vor und nach einer Sequenz von drei Transformationen: Skalieren, drehen und übersetzen.

![Abbildung, die eine Form anzeigt, die auf Koordinatenachsen zentriert ist, dann dieselbe Form, aber größer, gedreht und rechts übersetzt](images/aboutgdip01-art05.png)

## <a name="alpha-blending"></a>Alpha Blending

Beachten Sie, dass in der obigen Abbildung der nicht transformierte Bereich (mit roter Farbe) über den transformierten Bereich (mit einem Schraffurpinsel gefüllt) angezeigt werden kann. Dies wird durch Alpha Blending ermöglicht, das von GDI+ unterstützt wird. Mit Alpha Blending können Sie die Transparenz einer Füllfarbe angeben. Eine transparente Farbe wird mit der Hintergrundfarbe kombiniert – Wenn Sie die Füllfarbe transparenter gestalten, desto mehr wird der Hintergrund angezeigt. Die folgende Abbildung zeigt vier Ellipsen, die mit derselben Farbe (rot) auf unterschiedlichen Transparenz Ebenen gefüllt sind.

![Abbildung, die vier Ellipsen von variierender Transparenz mit einem semitransparenten Rechteck anzeigt](images/aboutgdip01-art06.png)

## <a name="support-for-multiple-image-formats"></a>Unterstützung für mehrere Bildformate

GDI+ stellt die [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)-, [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)-und [**metadateiklassen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) bereit, mit denen Sie Bilder in einer Vielzahl von Formaten laden, speichern und bearbeiten können. Die folgenden Formate werden unterstützt:

-   BMP
-   GIF (Graphics Interchange Format)
-   JPEG
-   EXIF
-   PNG
-   TIFF
-   ICON
-   WMF
-   EMF

 

 



