---
description: Windows GDI+ stellt Container bereit, mit denen Sie einen Teil des Zustands in einem Graphics-Objekt vorübergehend ersetzen oder erweitern können.
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: Geschachtelte Grafikcontainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d88b3a768e5b156eb5d28410ad69d58227e9660618764ca4b084b5e35662b839
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114980"
---
# <a name="nested-graphics-containers"></a>Geschachtelte Grafikcontainer

Windows GDI+ stellt Container bereit, mit denen Sie einen Teil des Zustands in einem [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) vorübergehend ersetzen oder erweitern können. Sie erstellen einen Container, indem Sie die [**Graphics::BeginContainer-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) eines **Graphics-Objekts** aufrufen. Sie können **Graphics::BeginContainer** wiederholt aufrufen, um geschachtelte Container zu bilden.

## <a name="transformations-in-nested-containers"></a>Transformationen in geschachtelten Containern

Im folgenden Beispiel werden ein [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und ein Container in diesem **Graphics-Objekt** erstellt. Die Welttransformation des **Grafikobjekts** ist eine Übersetzung von 100 Einheiten in x- und 80 Einheiten in y-Richtung. Die weltweite Transformation des Containers ist eine Drehung um 30 Grad. Der Code ruft auf.


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



Zweimal. Der erste Aufruf von [**Graphics::D rawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) befindet *sich im Container*. Das heißt, der Aufruf befindet sich zwischen den Aufrufen von [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) und [**Graphics::EndContainer.**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) Der zweite Aufruf von **Graphics::D rawRectangle** erfolgt nach dem Aufruf von **Graphics::EndContainer**.


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



Im vorangehenden Code wird das rechteckige, aus dem Container gezeichnete Rechteck zuerst durch die Welttransformation des Containers (Drehung) und dann durch die Welttransformation des [**Grafikobjekts**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) (Übersetzung) transformiert. Das Rechteck, das von außerhalb des Containers gezeichnet wird, wird nur durch die Welttransformation des **Grafikobjekts** (Übersetzung) transformiert. Die folgende Abbildung zeigt die beiden Rechtecke.

![Screenshot eines Fensters mit zwei roten Rechtecke, die den gleichen Punkt zentrieren, jedoch mit unterschiedlichen Drehungen](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a>Clipping in geschachtelten Containern

Im folgenden Beispiel wird veranschaulicht, wie geschachtelte Container Clippingbereiche behandeln. Der Code erstellt ein [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und einen Container in diesem **Graphics-Objekt.** Der Clippingbereich des **Graphics-Objekts** ist ein Rechteck, und der Clippingbereich des Containers ist eine Ellipse. Der Code ruft die [**Graphics::D rawLine-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) auf. Der erste Aufruf von **Graphics::D rawLine** befindet sich innerhalb des Containers, und der zweite Aufruf von **Graphics::D rawLine** befindet sich außerhalb des Containers (nach dem Aufruf von [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)). Die erste Zeile wird durch die Schnittmenge der beiden Clippingbereiche abgeschnitten. Die zweite Zeile wird nur durch den rechteckigen Ausschneidebereich des **Graphics-Objekts** abgeschnitten.


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



Die folgende Abbildung zeigt die beiden abgeschnittenen Zeilen.

![Abbildung einer Ellipse in einem Rechteck, wobei eine Zeile von der Ellipse und die andere vom Rechteck abgeschnitten wird](images/nestedcontainers2.png)

Wie die beiden vorherigen Beispiele zeigen, sind Transformationen und Clippingbereiche in geschachtelten Containern kumulativ. Wenn Sie die Welttransformationen des Containers und des [**Grafikobjekts**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) festlegen, gelten beide Transformationen für Elemente, die aus dem Container gezeichnet werden. Die Transformation des Containers wird zuerst angewendet, und die Transformation des **Graphics-Objekts** wird als Zweites angewendet. Wenn Sie die Clippingbereiche des Containers und des **Grafikobjekts** festlegen, werden elemente, die aus dem Container gezeichnet werden, durch die Schnittmenge der beiden Clippingbereiche abgeschnitten.

## <a name="quality-settings-in-nested-containers"></a>Quality Einstellungen in geschachtelten Containern

Qualitätseinstellungen [**(SmoothingMode,**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)und ähnliches) in geschachtelten Containern sind nicht kumulativ. Stattdessen ersetzen die Qualitätseinstellungen des Containers vorübergehend die Qualitätseinstellungen eines [**Graphics-Objekts.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Wenn Sie einen neuen Container erstellen, werden die Qualitätseinstellungen für diesen Container auf Standardwerte festgelegt. Angenommen, Sie verfügen über ein **Graphics-Objekt** mit dem Glättungsmodus ["SmoothingModeAntiAlias".](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) Wenn Sie einen Container erstellen, ist der Glättungsmodus innerhalb des Containers der Standardglättungsmodus. Sie können den Glättungsmodus des Containers festlegen, und alle elemente, die aus dem Container gezeichnet werden, werden entsprechend dem von Ihnen festgelegten Modus gezeichnet. Elemente, die nach dem Aufruf von [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) gezeichnet wurden, werden gemäß dem Glättungsmodus (["SmoothingModeAntiAlias!"](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)) gezeichnet, der vor dem Aufruf von [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))vorhanden war.

## <a name="several-layers-of-nested-containers"></a>Mehrere Ebenen von geschachtelten Containern

Sie sind nicht auf einen Container in einem [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) beschränkt. Sie können eine Sequenz von Containern erstellen, die jeweils im vorherigen geschachtelt sind, und Sie können die Welttransformation, den Clippingbereich und die Qualitätseinstellungen für jeden dieser geschachtelten Container angeben. Wenn Sie eine Zeichnungsmethode innerhalb des innersten Containers aufrufen, werden die Transformationen in der reihenfolge angewendet, beginnend mit dem innersten Container und endend mit dem äußersten Container. Elemente, die aus dem innersten Container gezeichnet werden, werden durch die Schnittmenge aller Ausschneidebereiche abgeschnitten.

Im folgenden Beispiel wird ein [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) erstellt und dessen Textrenderinghinweis auf ["TextRenderingHintAntiAlias"](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)festgelegt. Der Code erstellt zwei Container, einen innerhalb des anderen geschachtelt. Der Textrenderinghinweis des äußeren Containers ist auf ["TextRenderingHintSingleBitPerPixel"](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)festgelegt, und der Textrenderinghinweis des inneren Containers ist auf ["TextRenderingHintAntiAlias"](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)festgelegt. Der Code zeichnet drei Zeichenfolgen: eine aus dem inneren Container, eine aus dem äußeren Container und eine aus dem **Graphics-Objekt** selbst.


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



Die folgende Abbildung zeigt die drei Zeichenfolgen. Die aus dem inneren Container und dem [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) gezeichneten Zeichenfolgen werden durch Antialiasing geglättet. Die aus dem äußeren Container gezeichnete Zeichenfolge wird aufgrund der TextRenderingHintSingleBitPerPixel-Einstellung nicht durch Antialiasing geglättet.

![Abbildung eines Rechtecks, das die gleiche Zeichenfolge enthält; nur die Zeichen in der ersten und letzten Zeile sind reibungslos.](images/nestedcontainers3.png)

 

 
