---
description: Windows GDI+ stellt die Metafile-Klasse bereit, sodass Sie Metafiles aufzeichnen und anzeigen können.
ms.assetid: a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077
title: Metadatendateien (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae75c2185670563f9a9e624d868da5b0e299cbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343408"
---
# <a name="metafiles-gdi"></a>Metadatendateien (GDI+)

Windows GDI+ stellt die [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Klasse bereit, sodass Sie Metafiles aufzeichnen und anzeigen können. Eine Metadatei, auch als Vektorbild bezeichnet, ist ein Bild, das als Sequenz von Zeichnungs Befehlen und-Einstellungen gespeichert wird. Die in einem **Metafile** -Objekt aufgezeichneten Befehle und Einstellungen können im Arbeitsspeicher gespeichert oder in einer Datei oder einem Stream gespeichert werden.

In GDI+ können Metadateien angezeigt werden, die in den folgenden Formaten gespeichert wurden:

-   Windows Metafile-Format (WMF)
-   Erweiterte Metadatei (Enhanced Metafile, EMF)
-   EMF +

GDI+ kann Metadateien in den EMF-und EMF +-Formaten aufzeichnen, aber nicht im WMF-Format.

EMF + ist eine Erweiterung von EMF, mit der GDI+-Datensätze gespeichert werden können. Es gibt zwei Variationen des EMF +-Formats: EMF + only und EMF + Dual. Nur "EMF +"-Metadateien enthalten nur GDI+-Datensätze. Solche Metadatendateien können von GDI+, aber nicht von Windows Graphics Device Interface (GDI) angezeigt werden. "EMF + Dual Metadateien" enthält GDI+-und GDI-Datensätze. Jeder GDI+-Datensatz in einer EMF + Dual-Metadatei wird mit einem alternativen GDI-Datensatz gekoppelt. Solche Metadatendateien können von GDI+ oder GDI angezeigt werden.

Im folgenden Beispiel wird eine Einstellung und ein Zeichnungs Befehl in einer Datenträger Datei aufgezeichnet. Beachten Sie, dass im Beispiel ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt erstellt wird und dass der Konstruktor für das **Grafik** Objekt die Adresse eines [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Objekts als Argument erhält.


```
myMetafile = new Metafile(L"MyDiskFile.emf", hdc);
myGraphics = new Graphics(myMetafile);
   myPen = new Pen(Color(255, 0, 0, 200));
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->DrawLine(myPen, 0, 0, 60, 40);
delete myGraphics;
delete myPen;
delete myMetafile;
```



Wie das vorherige Beispiel zeigt, ist die [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse der Schlüssel zum Aufzeichnen von Anweisungen und Einstellungen in einem [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Objekt. Alle Aufrufe einer Methode eines **Grafik** Objekts können in einem **Metafile** -Objekt aufgezeichnet werden. Ebenso können Sie jede Eigenschaft eines **Grafik** Objekts festlegen und diese Einstellung in einem **Metafile** -Objekt aufzeichnen. Die Aufzeichnung wird beendet, wenn das **Grafik** Objekt gelöscht wird oder den Gültigkeitsbereich verlässt.

Im folgenden Beispiel wird die im vorherigen Beispiel erstellte Metadatendatei angezeigt. Die Metadatendatei wird mit der linken oberen Ecke bei (100, 100) angezeigt.


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



Im folgenden Beispiel werden mehrere Eigenschafts Einstellungen (Clippingbereich, Welt Transformation und Glättungs Modus) in einem [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Objekt aufgezeichnet. Anschließend zeichnet der Code mehrere Zeichnungs Anweisungen auf. Die Anweisungen und Einstellungen werden in einer Datenträger Datei gespeichert.


```
myMetafile = new Metafile(L"MyDiskFile2.emf", hdc); 
myGraphics = new Graphics(myMetafile);
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->RotateTransform(30);

   // Create an elliptical clipping region.
   GraphicsPath myPath;
   myPath.AddEllipse(0, 0, 200, 100);
   Region myRegion(&myPath);
   myGraphics->SetClip(&myRegion);

   Pen myPen(Color(255, 0, 0, 255));
   myGraphics->DrawPath(&myPen, &myPath);

   for(INT j = 0; j <= 300; j += 10)
   {
      myGraphics->DrawLine(&myPen, 0, 0, 300 - j, j);
   }
delete myGraphics;
delete myMetafile;
```



Im folgenden Beispiel wird das im vorherigen Beispiel erstellte Metadateibild angezeigt.


```
myGraphics = new Graphics(hdc);
myMetafile = new Metafile(L"MyDiskFile.emf");
myGraphics->DrawImage(myMetafile, 10, 10);
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes. Beachten Sie das Antialiasing, den Ellipsen Clippingbereich und die 30-Grad-Rotation.

![Screenshot eines Fensters, das eine Ellipse mit Zeilen enthält, die an einem Punkt außerhalb der Ellipse stehen](images/aboutgdip05-art00.png)

 

 



