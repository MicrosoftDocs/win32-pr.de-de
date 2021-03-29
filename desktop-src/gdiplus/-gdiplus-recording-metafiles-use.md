---
description: Mit der Metafile-Klasse, die von der Image-Klasse erbt, können Sie eine Sequenz von Zeichnungs Befehlen aufzeichnen.
ms.assetid: 062de6c2-9f82-415d-860e-2d1afd2ac027
title: Aufzeichnen von Metafiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 129b8fe810b1394921c60540488c93676341c562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977560"
---
# <a name="recording-metafiles"></a>Aufzeichnen von Metafiles

Mit der [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Klasse, die von der [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse erbt, können Sie eine Sequenz von Zeichnungs Befehlen aufzeichnen. Die aufgezeichneten Befehle können im Arbeitsspeicher gespeichert, in einer Datei gespeichert oder in einem Stream gespeichert werden. Metadatendateien können Vektorgrafiken, Rasterbilder und Text enthalten.

Im folgenden Beispiel wird ein [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Objekt erstellt. Im Code wird das **Metafile** -Objekt verwendet, um eine Sequenz von Grafik Befehlen aufzuzeichnen und dann die aufgezeichneten Befehle in einer Datei namens SampleMetafile. EMF zu speichern. Beachten Sie, dass der **Metafile** -Konstruktor ein Gerätekontext handle empfängt, und der [**grafikkonstruktor**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) empfängt die Adresse des **metadateiobjekts** . Die Aufzeichnung wird beendet (und die aufgezeichneten Befehle werden in der Datei gespeichert), wenn das **Grafik** Objekt den Gültigkeitsbereich verlässt. In den letzten beiden Codezeilen wird die Metadatendatei angezeigt, indem ein neues **Grafik** Objekt erstellt und die Adresse des **metadateiobjekts** an die **DrawImage** -Methode dieses **Grafik** Objekts übergeben wird. Beachten Sie, dass der Code das gleiche **metadateiobjekt** verwendet, um die Metadatei aufzuzeichnen und anzuzeigen (wiederzugeben).


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
> Um eine Metadatei aufzuzeichnen, müssen Sie ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt auf Grundlage eines [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Objekts erstellen. Die Aufzeichnung der Metadatei wird beendet, wenn das **Grafik** Objekt gelöscht wird oder den Gültigkeitsbereich verlässt.

 

Eine Metadatei enthält Ihren eigenen Grafik Zustand, der durch das [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt definiert wird, das zum Aufzeichnen der Metadatei verwendet wird. Alle Eigenschaften des **Grafik** Objekts (Clip Bereich, World Transformation, Glättung und ähnliches), die Sie beim Aufzeichnen der Metadatei festlegen, werden in der Metadatei gespeichert. Wenn Sie die Metadatei anzeigen, wird die Zeichnung entsprechend den gespeicherten Eigenschaften durchgeführt.

Nehmen Sie im folgenden Beispiel an, dass der Glättungs Modus während der Aufzeichnung der Metadatei auf smoothingmudenormal festgelegt wurde. Obwohl der Glättungs Modus des [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts, das für die Wiedergabe verwendet wird, auf "smoothingmodehighquality" festgelegt ist, wird die Metadatei entsprechend der Einstellung "smoothingmudenormal" wiedergegeben. Dabei handelt es sich um den Glättungs Modus, der während der wichtigen Aufzeichnung festgelegt wird


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 



