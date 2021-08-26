---
description: 'Die Dienste der Windows GDI+ in die folgenden drei kategorien unterteilt:'
ms.assetid: d5bef8e4-7a4c-4ac4-938a-7034ad3d743f
title: Die drei Teile GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5547702ca98cce86ace0f672b7aeed2dc8fc0ecee63534aaa15fac05bdcb024b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014650"
---
# <a name="the-three-parts-of-gdi"></a>Die drei Teile GDI+

Die Dienste der Windows GDI+ in die folgenden drei kategorien unterteilt:

-   [2D-Vektorgrafiken](#2-d-vector-graphics)
-   [Bildverarbeitung](#imaging)
-   [Typografie](#typography)

## <a name="2-d-vector-graphics"></a>2D-Vektorgrafiken

Vektorgrafiken umfasst das Zeichnen von Primitiven (z. B. Linien, Kurven und Abbildungen), die durch Sätze von Punkten in einem Koordinatensystem angegeben werden. Beispielsweise kann eine gerade Linie durch ihre beiden Endpunkte angegeben werden, und ein Rechteck kann durch einen Punkt angegeben werden, der die Position der oberen linken Ecke und ein Zahlenpaar angibt, das seine Breite und Höhe angibt. Ein einfacher Pfad kann durch ein Array von Punkten angegeben werden, die durch gerade Linien verbunden werden sollen. Ein Bézier-Spline ist eine anspruchsvolle Kurve, die von vier Kontrollpunkten angegeben wird.

GDI+ stellt Klassen zur Verfügung, die Informationen über die Primitive selbst speichern, Klassen, die Informationen darüber speichern, wie die Primitive gezeichnet werden sollen, und Klassen, die die Zeichnung tatsächlich erstellen. Beispielsweise speichert die **Rect-Klasse** die Position und Größe eines Rechtecks. Die **Pen-Klasse** speichert Informationen zu Linienfarbe, Linienbreite und Linienstil. und die **Graphics-Klasse** verfügt über Methoden zum Zeichnen von Linien, Rechtecke, Pfaden und anderen Abbildungen. Es gibt auch mehrere **Brush-Klassen,** die Informationen darüber speichern, wie geschlossene Abbildungen und Pfade mit Farben oder Mustern gefüllt werden sollen.

## <a name="imaging"></a>Bildverarbeitung

Bestimmte Arten von Bildern können mit den Techniken von Vektorgrafiken nur schwer oder gar nicht angezeigt werden. Beispielsweise wäre es schwierig, die Bilder auf Symbolleistenschaltflächen und die als Symbole angezeigten Bilder als Sammlungen von Linien und Kurven anzugeben. Ein hochauflösendes digitales Foto eines ungnen Baseball-Teams wäre mit Vektortechniken noch schwieriger zu erstellen. Bilder dieses Typs werden als Bitmaps gespeichert, Arrays von Zahlen, die die Farben einzelner Punkte auf dem Bildschirm darstellen. Datenstrukturen, die Informationen zu Bitmaps speichern, sind tendenziell komplexer als diejenigen, die für Vektorgrafiken erforderlich sind. Daher gibt es mehrere Klassen in GDI+ diesem Zweck. Ein Beispiel für eine solche Klasse ist **CachedBitmap,** die zum Speichern einer Bitmap im Arbeitsspeicher für schnellen Zugriff und schnelle Anzeige verwendet wird.

## <a name="typography"></a>Typografie

Bei der Typografie geht es um die Anzeige von Text in einer Vielzahl von Schriftarten, Größen und Stilen. GDI+ bietet eine beeindruckende Unterstützung für diese komplexe Aufgabe. Eines der neuen Features in GDI+ ist das Antialiasing von Subpixeln, das Text, der auf einem BILDSCHIRM des BILDSCHIRMs angezeigt wird, eine reibungslosere Darstellung bietet.

 

 



