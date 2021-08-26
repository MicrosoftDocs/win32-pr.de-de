---
description: Mit der Metafile-Klasse, die von der Image-Klasse erbt, können Sie eine Sequenz von Zeichnungsbefehlen aufzeichnen.
ms.assetid: 062de6c2-9f82-415d-860e-2d1afd2ac027
title: Aufzeichnen von Metadateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 047cdce842a9b44096ebd0f866e1b1551a5f951e138557062dff5e8f8d54f3ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014780"
---
# <a name="recording-metafiles"></a>Aufzeichnen von Metadateien

Mit [**der Metafile-Klasse,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) die von der [**Image-Klasse erbt,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) können Sie eine Sequenz von Zeichnungsbefehlen aufzeichnen. Die aufgezeichneten Befehle können im Arbeitsspeicher, in einer Datei oder in einem Stream gespeichert werden. Metadateien können Vektorgrafiken, Rasterbilder und Text enthalten.

Im folgenden Beispiel wird ein [**Metafile-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) erstellt. Der Code verwendet das **Metafile-Objekt** zum Aufzeichnen einer Sequenz von Grafikbefehlen und speichert dann die aufgezeichneten Befehle in einer Datei mit dem Namen SampleMetafile.emf. Beachten Sie, dass **der Metafile-Konstruktor** ein Gerätekontexthand handle empfängt und der [**Grafikkonstruktor**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) die Adresse des **Metafile-Objekts** empfängt. Die Aufzeichnung wird beendet (und die aufgezeichneten Befehle werden in der Datei gespeichert), wenn das **Graphics-Objekt** den Gültigkeitsbereich übergeht. Die letzten beiden Codezeilen zeigen die Metadatei an, indem sie ein neues **Graphics-Objekt** erstellen und die Adresse des **Metafile-Objekts** an die **DrawImage-Methode** dieses **Graphics-Objekts** übergeben. Beachten Sie, dass der Code dasselbe **Metafile-Objekt** verwendet, um die Metadatei zu erfassen und anzuzeigen (wieder anzuzeigen).


```
Metafile metafile(L"SampleMetafile.emf", hdc); 
{
   Graphics graphics(&metafile);
   Pen greenPen(Color(255, 0, 255, 0));
   SolidBrush solidBrush(Color(255, 0, 0, 255));

   // Add a rectangle and an ellipse to the metafile.
   graphics.DrawRectangle(&greenPen, Rect(50, 10, 25, 75));
   graphics.DrawEllipse(&greenPen, Rect(100, 10, 25, 75));

   // Add an ellipse (drawn with antialiasing) to the metafile.
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   graphics.DrawEllipse(&greenPen, Rect(150, 10, 25, 75));

   // Add some text (drawn with antialiasing) to the metafile.
   FontFamily fontFamily(L"Arial");
   Font font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   
   graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
   graphics.RotateTransform(30.0f);
   graphics.DrawString(L"Smooth Text", 11, &font, 
      PointF(50.0f, 50.0f), &solidBrush);
} // End of recording metafile.

// Play back the metafile.
Graphics playbackGraphics(hdc);
playbackGraphics.DrawImage(&metafile, 200, 100);
```



> [!Note]  
> Um eine Metadatei aufzeichnen zu können, müssen Sie ein [**Grafikobjekt**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basierend auf einem [**Metafile-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) erstellen. Die Aufzeichnung der Metadatei endet, wenn das **Grafikobjekt** gelöscht wird oder den Gültigkeitsbereich übergeht.

 

Eine Metadatei enthält ihren eigenen Grafikzustand, der durch das [**Graphics-Objekt**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) definiert wird, das zum Aufzeichnen der Metadatei verwendet wird. Alle Eigenschaften des **Grafikobjekts** (Clipbereich, Welttransformation, Glättungsmodus und deren Art), die Sie beim Aufzeichnen der Metadatei festlegen, werden in der Metadatei gespeichert. Wenn Sie die Metadatei anzeigen, erfolgt die Zeichnung gemäß diesen gespeicherten Eigenschaften.

Im folgenden Beispiel wird davon ausgegangen, dass der Glättungsmodus während der Aufzeichnung der Metadatei auf SmoothingModeNormal festgelegt wurde. Obwohl der Glättungsmodus des für die Wiedergabe verwendeten [**Grafikobjekts**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) auf SmoothingModeHighQuality festgelegt ist, wird die Metadatei gemäß der SmoothingModeNormal-Einstellung abgespielt. Es ist wichtig, dass der während der Aufzeichnung festgelegte Glättungsmodus wichtig ist, nicht der Glättungsmodus, der vor der Wiedergabe festgelegt wurde.


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 



