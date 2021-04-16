---
description: 'In Windows GDI+ werden drei Koordinaten Bereiche verwendet: "World", "page" und "Device".'
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: Typen von Koordinatensystemen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05908196662918eb93f4fa6e2b356a6989ed5a58
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104558304"
---
# <a name="types-of-coordinate-systems"></a>Typen von Koordinatensystemen

In Windows GDI+ werden drei Koordinaten Bereiche verwendet: "World", "page" und "Device". Wenn Sie den-Befehl ausführen `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , befinden sich die Punkte, die Sie an die [**Grafik übergeben::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) -Methode – (0,0) und (160, 80) – im weltweiten Koordinaten Bereich. Bevor GDI+ die Linie auf dem Bildschirm zeichnen kann, durchlaufen die Koordinaten eine Sequenz von Transformationen. Eine Transformation konvertiert globale Koordinaten in Seiten Koordinaten, und eine andere Transformation wandelt Seiten Koordinaten in Geräte Koordinaten um.

Angenommen, Sie möchten mit einem Koordinatensystem arbeiten, dessen Ursprung im Text des Client Bereichs liegt, und nicht in der oberen linken Ecke. Angenommen, Sie möchten, dass der Ursprung 100 Pixel vom linken Rand des Client Bereichs und 50 Pixel vom oberen Rand des Client Bereichs sein soll. Die folgende Abbildung zeigt ein solches Koordinatensystem.

![Screenshot eines Fensters mit der Bezeichnung "Koordinatenachsen"](images/aboutgdip05-art01.png)

Wenn Sie den-Befehl ausführen `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , erhalten Sie die in der folgenden Abbildung gezeigte Zeile.

![Screenshot des vorherigen Fensters, aber mit einer blauen Linie, die diagonal vom Ursprung aus erweitert wird](images/aboutgdip05-art02.png)

Die Koordinaten der Endpunkte der Zeile in den drei Koordinaten Räumen lauten wie folgt:



|        |                         |
|--------|-------------------------|
| World  | (0,0) bis (160, 80)     |
| Seite   | (100, 50) bis (260, 130) |
| Sicherungsmedium | (100, 50) bis (260, 130) |



 

Beachten Sie, dass der Seiten Koordinaten Bereich seinen Ursprung in der oberen linken Ecke des Client Bereichs hat. Dies ist immer der Fall. Beachten Sie außerdem, dass die Geräte Koordinaten den Seiten Koordinaten entsprechen, da die Maßeinheit das Pixel ist. Wenn Sie die Maßeinheit auf einen anderen Wert als Pixel festlegen (z. b. Zoll), unterscheiden sich die Geräte Koordinaten von den Seiten Koordinaten.

Die Transformation zum Zuordnen von Weltkoordinaten zu Seiten Koordinaten wird als globale *Transformation* bezeichnet und wird von einem [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt verwaltet. Im vorherigen Beispiel handelt es sich bei der Welt Transformation um eine Translation 100-Einheiten in der x-Richtung und 50-Einheiten in der y-Richtung. Im folgenden Beispiel wird die globale Transformation eines **Grafik** Objekts festgelegt, und anschließend wird das **Grafik** Objekt verwendet, um die in der vorherigen Abbildung gezeigte Zeile zu zeichnen.


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



Die Transformation, die den Geräte Koordinaten Seiten Koordinaten zuordnet, wird als *Seiten Transformation* bezeichnet. Die [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse bietet vier Methoden zum Bearbeiten und Überprüfen der Seiten Transformation: [**Graphics:: setpageunit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics:: getpageunit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics:: setpagescale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)und [**Graphics:: getPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale). Die **Grafik** Klasse bietet auch zwei Methoden, [**Graphics:: getdpix**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) und [**Graphics:: getdpiy**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), um die horizontalen und vertikalen Punkte pro Zoll des Anzeige Geräts zu untersuchen.

Sie können die [**Graphics:: setpageunit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) -Methode der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse verwenden, um eine Maßeinheit anzugeben. Im folgenden Beispiel wird eine Zeile von (0,0) zu (2, 1) gezeichnet, wobei Punkt (2, 1) 2 Zoll nach rechts und 1 Zoll vom Punkt (0,0) ist.


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> Wenn Sie beim Erstellen des Stifts keine Stift Breite angeben, wird im vorherigen Beispiel eine Linie mit einer Breite von einem Zoll gezeichnet. Sie können die Stift Breite im zweiten Argument für den [**Stift**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) -Konstruktor angeben:
> <br/><br/>
> `Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.

 

Wenn wir davon ausgehen, dass das Anzeigegerät 96 Punkte pro Zoll in horizontaler Richtung und 96 Punkte pro Zoll in vertikaler Richtung aufweist, haben die Endpunkte der Linie im vorherigen Beispiel die folgenden Koordinaten in den drei Koordinaten Räumen:



|        |                     |
|--------|---------------------|
| World  | (0,0) bis (2, 1)    |
| Seite   | (0,0) bis (2, 1)    |
| Sicherungsmedium | (0,0, bis (192, 96) |



 

Sie können die Transformationen für Welt und Seite kombinieren, um eine Vielzahl von Effekten zu erzielen. Angenommen, Sie möchten Zoll als Maßeinheit verwenden, und Sie möchten, dass der Ursprung ihres Koordinatensystems 2 Zoll vom linken Rand des Client Bereichs und 1/2 Zoll vom oberen Rand des Client Bereichs ist. Im folgenden Beispiel werden die Welt-und Seiten Transformationen eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts festgelegt, und anschließend wird eine Linie von (0,0) zu (2, 1) gezeichnet.


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



In der folgenden Abbildung ist die Linie und das Koordinatensystem dargestellt.

![Screenshot des vorherigen Fensters, aber breiter, wobei die Achsen auf der linken Seite positioniert sind und anders gekennzeichnet sind](images/aboutgdip05-art03.png)

Wenn wir davon ausgehen, dass das Anzeigegerät 96 Punkte pro Zoll in horizontaler Richtung und 96 Punkte pro Zoll in vertikaler Richtung aufweist, haben die Endpunkte der Linie im vorherigen Beispiel die folgenden Koordinaten in den drei Koordinaten Räumen:



|        |                         |
|--------|-------------------------|
| World  | (0,0) bis (2, 1)        |
| Seite   | (2, 0,5) bis (4, 1,5)    |
| Sicherungsmedium | (192, 48) bis (384, 144) |



 

 

 
