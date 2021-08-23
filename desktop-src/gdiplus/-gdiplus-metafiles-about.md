---
description: Windows GDI+ stellt die Metafile-Klasse bereit, sodass Sie Metadateien aufzeichnen und anzeigen können.
ms.assetid: a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077
title: Metadateien (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 190d03edd8857da3e840c2b3fde04314fa1fb1ddb01c8e69c684bccecf3e708d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778680"
---
# <a name="metafiles-gdi"></a>Metadateien (GDI+)

Windows GDI+ stellt die [**Metafile-Klasse**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) bereit, sodass Sie Metadateien aufzeichnen und anzeigen können. Eine Metadatei, auch vektorbild genannt, ist ein Bild, das als Sequenz von Zeichnungsbefehlen und -einstellungen gespeichert wird. Die in einem **Metafile-Objekt** aufgezeichneten Befehle und Einstellungen können im Arbeitsspeicher oder in einer Datei oder einem Stream gespeichert werden.

GDI+ können Metadateien anzeigen, die in den folgenden Formaten gespeichert wurden:

-   Windows Metafile-Format (WMF)
-   Erweiterte Metadatei (Enhanced Metafile, EMF)
-   EMF+

GDI+ können Metadateien im EMF- und EMF+-Format aufzeichnen, jedoch nicht im WMF-Format.

EMF+ ist eine Erweiterung für EMF, mit der GDI+ Datensätze gespeichert werden können. Es gibt zwei Varianten des EMF+-Formats: NUR EMF+ und EMF+ Dual. Nur EMF+-Metadateien enthalten nur GDI+ Datensätze. Solche Metadateien können durch GDI+, aber nicht durch Windows Graphics Device Interface (GDI) angezeigt werden. EMF+ Dual-Metadateien enthalten GDI+- und GDI-Datensätze. Jeder GDI+ Datensatz in einer EMF+ Dual-Metadatei wird mit einem alternativen GDI-Datensatz gekoppelt. Solche Metadateien können durch GDI+ oder GDI angezeigt werden.

Im folgenden Beispiel werden eine Einstellung und ein Zeichnungsbefehl in einer Datenträgerdatei aufgezeichnet. Beachten Sie, dass im Beispiel ein [**Graphics-Objekt**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) erstellt wird und der Konstruktor für das **Graphics-Objekt** die Adresse eines [**Metafile-Objekts**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) als Argument empfängt.


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



Wie im vorherigen Beispiel gezeigt, ist die [**Graphics-Klasse**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) der Schlüssel zum Aufzeichnen von Anweisungen und Einstellungen in einem [**Metafile-Objekt.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) Jeder Aufruf einer Methode eines **Graphics-Objekts** kann in einem **Metafile-Objekt** aufgezeichnet werden. Ebenso können Sie jede Eigenschaft eines **Grafikobjekts** festlegen und diese Einstellung in einem **Metafile-Objekt** aufzeichnen. Die Aufzeichnung wird beendet, wenn das **Grafikobjekt** gelöscht wird oder den Gültigkeitsbereich übergeht.

Im folgenden Beispiel wird die im vorherigen Beispiel erstellte Metadatei angezeigt. Die Metadatei wird mit der oberen linken Ecke bei (100, 100) angezeigt.


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



Im folgenden Beispiel werden mehrere Eigenschafteneinstellungen (Clippingbereich, Welttransformation und Glättungsmodus) in einem [**Metafile-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) aufgezeichnet. Anschließend zeichnet der Code mehrere Zeichnungsanweisungen auf. Die Anweisungen und Einstellungen werden in einer Datenträgerdatei gespeichert.


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



Im folgenden Beispiel wird das metafile-Bild angezeigt, das im vorherigen Beispiel erstellt wurde.


```
myGraphics = new Graphics(hdc);
myMetafile = new Metafile(L"MyDiskFile.emf");
myGraphics->DrawImage(myMetafile, 10, 10);
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes. Beachten Sie das Antialiasing, den elliptischen Clippingbereich und die Drehung um 30 Grad.

![Screenshot eines Fensters, das eine Ellipse enthält, die mit Zeilen gefüllt ist, die an einem Punkt außerhalb der Ellipse stammen](images/aboutgdip05-art00.png)

 

 



