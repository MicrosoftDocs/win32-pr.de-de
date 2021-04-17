---
description: 'Die Dienste von Windows GDI+ fallen in die folgenden drei allgemeinen Kategorien:'
ms.assetid: d5bef8e4-7a4c-4ac4-938a-7034ad3d743f
title: Die drei Teile von GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2021260e9fe3b3d927131c2ba1856aeed0ed07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994182"
---
# <a name="the-three-parts-of-gdi"></a>Die drei Teile von GDI+

Die Dienste von Windows GDI+ fallen in die folgenden drei allgemeinen Kategorien:

-   [2D-Vektorgrafiken](#2-d-vector-graphics)
-   [Bildverarbeitung](#imaging)
-   [Typografie](#typography)

## <a name="2-d-vector-graphics"></a>2D-Vektorgrafiken

Vektorgrafiken umfassen das Zeichnen primitiver (z. b. Linien, Kurven und Abbildungen), die durch Sätze von Punkten auf einem Koordinatensystem angegeben werden. Beispielsweise kann eine gerade Linie von den beiden Endpunkten angegeben werden, und ein Rechteck kann durch einen Punkt angegeben werden, der die Position der linken oberen Ecke und ein paar von Zahlen mit Breite und Höhe gibt. Ein einfacher Pfad kann durch ein Array von Punkten angegeben werden, die durch gerade Linien verbunden werden sollen. Eine Bézier-Spline ist eine ausgereifte Kurve, die durch vier Steuerungs Punkte angegeben wird.

GDI+ stellt Klassen bereit, mit denen Informationen zu den primitiven selbst gespeichert werden, Klassen, die Informationen über die Art und Weise speichern, wie die primitiven gezeichnet werden sollen, und Klassen, die die Zeichnung tatsächlich durchführen. Die **Rect** -Klasse speichert z. b. die Position und Größe eines Rechtecks. die **Stift** Klasse speichert Informationen über Linien Farbe, Linienstärke und Linienart. und die **Grafik** Klasse verfügt über Methoden zum Zeichnen von Linien, Rechtecke, Pfaden und anderen Abbildungen. Es gibt auch mehrere **Pinsel** Klassen, die Informationen darüber speichern, wie geschlossene Abbildungen und Pfade mit Farben oder Mustern gefüllt werden.

## <a name="imaging"></a>Bildverarbeitung

Es ist schwierig oder unmöglich, bestimmte Arten von Bildern mit den Techniken von Vektorgrafiken anzuzeigen. Beispielsweise können die Bilder auf den Symbolleisten Schaltflächen und die Bilder, die als Symbole angezeigt werden, schwierig als Auflistungen von Linien und Kurven angegeben werden. Ein qualitativ hochauflösende digitales Foto eines überfüllten Baseball-Stadions wäre sogar noch schwieriger, mit Vektor Techniken zu erstellen. Bilder dieses Typs werden als Bitmaps, Arrays von Zahlen, die die Farben einzelner Punkte auf dem Bildschirm darstellen, gespeichert. Datenstrukturen, in denen Informationen zu Bitmaps gespeichert werden, sind tendenziell komplexer als die, die für Vektorgrafiken erforderlich sind. Daher gibt es mehrere Klassen in GDI+, die diesem Zweck zugeordnet sind. Ein Beispiel für eine solche Klasse ist **CachedBitmap**, die zum Speichern einer Bitmap im Arbeitsspeicher für schnellen Zugriff und Anzeige verwendet wird.

## <a name="typography"></a>Typografie

Typografiedarstellung ist die Anzeige von Text in einer Vielzahl von Schriftarten, Größen und Stilen. GDI+ bietet eine beeindruckende Menge an Unterstützung für diese komplexe Aufgabe. Eines der neuen Features in GDI+ ist Subpixel-Antialiasing, wodurch Text auf einem LCD-Bildschirm gerendert wird.

 

 



