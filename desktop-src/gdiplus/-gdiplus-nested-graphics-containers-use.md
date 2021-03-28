---
description: Windows GDI+ stellt Container bereit, die Sie verwenden können, um einen Teil des Zustands in einem Grafik Objekt temporär zu ersetzen oder zu erweitern.
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: Geschachtelte Grafikcontainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f9d9feac3494b423d844cb1e3da359af33eaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959450"
---
# <a name="nested-graphics-containers"></a>Geschachtelte Grafikcontainer

Windows GDI+ stellt Container bereit, die Sie verwenden können, um einen Teil des Zustands in einem [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt temporär zu ersetzen oder zu erweitern. Sie erstellen einen Container durch Aufrufen der [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) -Methode eines **Grafik** Objekts. Sie können " **Graphics:: BeginContainer** " wiederholt aufrufen, um in einem Container zu erstellen.

## <a name="transformations-in-nested-containers"></a>Transformationen in der Liste der Container

Im folgenden Beispiel werden ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein Container innerhalb dieses **Grafik** Objekts erstellt. Die globale Transformation des **Grafik** Objekts ist eine Translation 100-Einheiten in der x-Richtung und 80-Einheiten in der y-Richtung. Die Welt Transformation des Containers ist eine 30-Grad-Rotation. Der Code führt den-Befehl aus.


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



zweimal. Der erste Grafik Befehl [**::D rawrechteck**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) befindet sich *innerhalb des Containers*. Das heißt, der Aufruf erfolgt zwischen den Aufrufen von [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) und [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer). Der zweite aufzurufende **Grafik::D rawrechteck** ist nach dem aufzurufenden **Grafik:: EndContainer**.


```
Graphics           graphics(hdc);
Pen                pen(Color(255, 255, 0, 0));
GraphicsContainer  graphicsContainer;

graphics.TranslateTransform(100.0f, 80.0f);

graphicsContainer = graphics.BeginContainer();
   graphics.RotateTransform(30.0f);
   graphics.DrawRectangle(&pen, -60, -30, 120, 60);
graphics.EndContainer(graphicsContainer);

graphics.DrawRectangle(&pen, -60, -30, 120, 60);
```



Im vorangehenden Code wird das aus dem Container gezogene Rechteck zuerst von der Welt Transformation des Containers (Drehung) und dann von der Welt Transformation des [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts (Translation) transformiert. Das von außerhalb des Containers gezeichnete Rechteck wird nur durch die Welt Transformation des **Grafik** Objekts (Translation) transformiert. Die folgende Abbildung zeigt die beiden Rechtecke.

![Screenshot eines Fensters mit zwei roten Rechtecke, die denselben Punkt zentriert haben, aber mit unterschiedlichen Drehungen](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a>Clipping in geschbten Containern

Im folgenden Beispiel wird veranschaulicht, wie die geschbten Container Clippingbereiche verarbeiten. Der Code erstellt ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und einen Container in diesem **Grafik** Objekt. Der Clippingbereich des **Grafik** Objekts ist ein Rechteck, und der Clippingbereich des Containers ist eine Ellipse. Der Code führt zwei Aufrufe an die [**Grafiken aus::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) -Methode. Der erste Grafik Befehl **::D rawline** befindet sich innerhalb des Containers, und der zweite aufzurufende **Grafik::D rawline** befindet sich außerhalb des Containers (nach dem aufzurufen von [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)). Die erste Zeile wird durch die Schnittmenge der beiden Clippingbereiche abgeschnitten. Die zweite Zeile wird nur durch den rechteckigen Clippingbereich des **Grafik** Objekts abgeschnitten.


```
Graphics           graphics(hdc);
GraphicsContainer  graphicsContainer;
Pen                redPen(Color(255, 255, 0, 0), 2);
Pen                bluePen(Color(255, 0, 0, 255), 2);
SolidBrush         aquaBrush(Color(255, 180, 255, 255));
SolidBrush         greenBrush(Color(255, 150, 250, 130));

graphics.SetClip(Rect(50, 65, 150, 120));
graphics.FillRectangle(&aquaBrush, 50, 65, 150, 120);

graphicsContainer = graphics.BeginContainer();
   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(75, 50, 100, 150);

  // Construct a region based on the path.
   Region region(&path);
   graphics.FillRegion(&greenBrush, &region);

   graphics.SetClip(&region);
   graphics.DrawLine(&redPen, 50, 0, 350, 300);
graphics.EndContainer(graphicsContainer);

graphics.DrawLine(&bluePen, 70, 0, 370, 300);
```



Die folgende Abbildung zeigt die beiden ausgeschnittenen Zeilen.

![Abbildung einer Ellipse innerhalb eines Rechtecks, bei der eine Zeile von der Ellipse und die andere durch das Rechteck abgeschnitten wurde](images/nestedcontainers2.png)

Wie die beiden vorherigen Beispiele zeigen, sind Transformationen und Clippingbereiche in geschposteten Containern kumulativ. Wenn Sie die globalen Transformationen für den Container und das [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt festlegen, gelten beide Transformationen für Elemente, die aus dem Container gezogen werden. Die Transformation des Containers wird zuerst angewendet, und die Transformation des **Grafik** Objekts wird als zweites angewendet. Wenn Sie die Ausschneide Bereiche des Containers und des **Grafik** Objekts festlegen, werden die Elemente, die aus dem Container gezogen werden, durch die Schnittmenge der beiden Clippingbereiche abgeschnitten.

## <a name="quality-settings-in-nested-containers"></a>Qualitätseinstellungen in der Liste der Container

Qualitätseinstellungen (" [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)", " [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)" und "like") in den nativen Containern sind nicht kumulativ. Stattdessen ersetzen die Qualitätseinstellungen des Containers vorübergehend die Qualitätseinstellungen eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts. Wenn Sie einen neuen Container erstellen, werden die Qualitätseinstellungen für diesen Container auf Standardwerte festgelegt. Nehmen Sie beispielsweise an, Sie verfügen über ein **Grafik** Objekt mit dem Glättungs Modus [* * * * SmoothingModeAntiAlias * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode). Wenn Sie einen Container erstellen, ist der Glättungs Modus innerhalb des Containers der standardmäßige Glättungs Modus. Sie können den Glättungs Modus des Containers festlegen, und alle Elemente, die aus dem Container gezogen werden, werden gemäß dem von Ihnen festgelegten Modus gezeichnet. Elemente, die nach dem Aufrufen von [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) gezeichnet werden, werden gemäß dem Glättungs Modus ([* * * * SmoothingModeAntiAlias * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)) gezeichnet, der vor dem Aufrufen von [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))vorhanden war.

## <a name="several-layers-of-nested-containers"></a>Mehrere Ebenen von als Container

Sie sind nicht auf einen Container in einem [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt beschränkt. Sie können eine Reihe von Containern erstellen, die jeweils in der vorherigen geschpotet sind, und Sie können die Welt Transformation, den Clippingbereich und die Qualitätseinstellungen der einzelnen geschposteten Container angeben. Wenn Sie eine Zeichnungs Methode aus dem innersten Container heraus aufzurufen, werden die Transformationen in der richtigen Reihenfolge angewendet, beginnend mit dem innersten Container und enden mit dem äußersten Container. Elemente, die aus dem innersten Container gezeichnet werden, werden durch die Schnittmenge aller Clippingbereiche abgeschnitten.

Im folgenden Beispiel wird ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt erstellt und der Text Rendering-Hinweis auf [* * * * textrenderinghintantialias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* * festgelegt. Der Code erstellt zwei Container, von denen eine geschachtelt ist. Der Text Rendering-Hinweis des äußeren Containers ist auf [* * * * TextRenderingHintSingleBitPerPixel * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* * festgelegt, und der Text Rendering-Hinweis des inneren Containers ist auf [* * * * textrenderinghintantialias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* * festgelegt. Der Code zeichnet drei Zeichen folgen: eine aus dem inneren Container, eine aus dem äußeren Container und eine aus dem **Grafik** Objekt selbst.


```
Graphics graphics(hdc);
GraphicsContainer innerContainer;
GraphicsContainer outerContainer;
SolidBrush brush(Color(255, 0, 0, 255));
FontFamily fontFamily(L"Times New Roman");
Font font(&fontFamily, 36, FontStyleRegular, UnitPixel);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);

outerContainer = graphics.BeginContainer();

   graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);

   innerContainer = graphics.BeginContainer();
      graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
      graphics.DrawString(L"Inner Container", 15, &font,
         PointF(20, 10), &brush);
   graphics.EndContainer(innerContainer);

   graphics.DrawString(L"Outer Container", 15, &font, PointF(20, 50), &brush);

graphics.EndContainer(outerContainer);

graphics.DrawString(L"Graphics Object", 15, &font, PointF(20, 90), &brush);
```



Die folgende Abbildung zeigt die drei Zeichen folgen. Die Zeichen folgen, die aus dem inneren Container und dem [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt gezeichnet werden, werden durch Antialiasing geglättet. Die aus dem äußeren Container gezeichnete Zeichenfolge wird aufgrund der TextRenderingHintSingleBitPerPixel-Einstellung nicht durch Antialiasing geglättet.

![Abbildung eines Rechtecks, das die gleiche Zeichenfolge enthält. nur die Zeichen in der ersten und letzten Zeile sind glatt.](images/nestedcontainers3.png)

 

 
