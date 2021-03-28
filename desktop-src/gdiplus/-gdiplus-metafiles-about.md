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
# <a name="metafiles-gdi"></a><span data-ttu-id="40ce4-103">Metadatendateien (GDI+)</span><span class="sxs-lookup"><span data-stu-id="40ce4-103">Metafiles (GDI+)</span></span>

<span data-ttu-id="40ce4-104">Windows GDI+ stellt die [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Klasse bereit, sodass Sie Metafiles aufzeichnen und anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="40ce4-104">Windows GDI+ provides the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class so that you can record and display metafiles.</span></span> <span data-ttu-id="40ce4-105">Eine Metadatei, auch als Vektorbild bezeichnet, ist ein Bild, das als Sequenz von Zeichnungs Befehlen und-Einstellungen gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="40ce4-105">A metafile, also called a vector image, is an image that is stored as a sequence of drawing commands and settings.</span></span> <span data-ttu-id="40ce4-106">Die in einem **Metafile** -Objekt aufgezeichneten Befehle und Einstellungen können im Arbeitsspeicher gespeichert oder in einer Datei oder einem Stream gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="40ce4-106">The commands and settings recorded in a **Metafile** object can be stored in memory or saved to a file or stream.</span></span>

<span data-ttu-id="40ce4-107">In GDI+ können Metadateien angezeigt werden, die in den folgenden Formaten gespeichert wurden:</span><span class="sxs-lookup"><span data-stu-id="40ce4-107">GDI+ can display metafiles that have been stored in the following formats:</span></span>

-   <span data-ttu-id="40ce4-108">Windows Metafile-Format (WMF)</span><span class="sxs-lookup"><span data-stu-id="40ce4-108">Windows Metafile Format (WMF)</span></span>
-   <span data-ttu-id="40ce4-109">Erweiterte Metadatei (Enhanced Metafile, EMF)</span><span class="sxs-lookup"><span data-stu-id="40ce4-109">Enhanced Metafile (EMF)</span></span>
-   <span data-ttu-id="40ce4-110">EMF +</span><span class="sxs-lookup"><span data-stu-id="40ce4-110">EMF+</span></span>

<span data-ttu-id="40ce4-111">GDI+ kann Metadateien in den EMF-und EMF +-Formaten aufzeichnen, aber nicht im WMF-Format.</span><span class="sxs-lookup"><span data-stu-id="40ce4-111">GDI+ can record metafiles in the EMF and EMF+ formats, but not in the WMF format.</span></span>

<span data-ttu-id="40ce4-112">EMF + ist eine Erweiterung von EMF, mit der GDI+-Datensätze gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="40ce4-112">EMF+ is an extension to EMF that allows GDI+ records to be stored.</span></span> <span data-ttu-id="40ce4-113">Es gibt zwei Variationen des EMF +-Formats: EMF + only und EMF + Dual.</span><span class="sxs-lookup"><span data-stu-id="40ce4-113">There are two variations on the EMF+ format: EMF+ Only and EMF+ Dual.</span></span> <span data-ttu-id="40ce4-114">Nur "EMF +"-Metadateien enthalten nur GDI+-Datensätze.</span><span class="sxs-lookup"><span data-stu-id="40ce4-114">EMF+ Only metafiles contain only GDI+ records.</span></span> <span data-ttu-id="40ce4-115">Solche Metadatendateien können von GDI+, aber nicht von Windows Graphics Device Interface (GDI) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="40ce4-115">Such metafiles can be displayed by GDI+ but not by Windows Graphics Device Interface (GDI).</span></span> <span data-ttu-id="40ce4-116">"EMF + Dual Metadateien" enthält GDI+-und GDI-Datensätze.</span><span class="sxs-lookup"><span data-stu-id="40ce4-116">EMF+ Dual metafiles contain GDI+ and GDI records.</span></span> <span data-ttu-id="40ce4-117">Jeder GDI+-Datensatz in einer EMF + Dual-Metadatei wird mit einem alternativen GDI-Datensatz gekoppelt.</span><span class="sxs-lookup"><span data-stu-id="40ce4-117">Each GDI+ record in an EMF+ Dual metafile is paired with an alternate GDI record.</span></span> <span data-ttu-id="40ce4-118">Solche Metadatendateien können von GDI+ oder GDI angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="40ce4-118">Such metafiles can be displayed by GDI+ or by GDI.</span></span>

<span data-ttu-id="40ce4-119">Im folgenden Beispiel wird eine Einstellung und ein Zeichnungs Befehl in einer Datenträger Datei aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="40ce4-119">The following example records one setting and one drawing command in a disk file.</span></span> <span data-ttu-id="40ce4-120">Beachten Sie, dass im Beispiel ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt erstellt wird und dass der Konstruktor für das **Grafik** Objekt die Adresse eines [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Objekts als Argument erhält.</span><span class="sxs-lookup"><span data-stu-id="40ce4-120">Note that the example creates a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and that the constructor for the **Graphics** object receives the address of a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object as an argument.</span></span>


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



<span data-ttu-id="40ce4-121">Wie das vorherige Beispiel zeigt, ist die [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse der Schlüssel zum Aufzeichnen von Anweisungen und Einstellungen in einem [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="40ce4-121">As the preceding example shows, the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is the key to recording instructions and settings in a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="40ce4-122">Alle Aufrufe einer Methode eines **Grafik** Objekts können in einem **Metafile** -Objekt aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="40ce4-122">Any call made to a method of a **Graphics** object can be recorded in a **Metafile** object.</span></span> <span data-ttu-id="40ce4-123">Ebenso können Sie jede Eigenschaft eines **Grafik** Objekts festlegen und diese Einstellung in einem **Metafile** -Objekt aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="40ce4-123">Likewise, you can set any property of a **Graphics** object and record that setting in a **Metafile** object.</span></span> <span data-ttu-id="40ce4-124">Die Aufzeichnung wird beendet, wenn das **Grafik** Objekt gelöscht wird oder den Gültigkeitsbereich verlässt.</span><span class="sxs-lookup"><span data-stu-id="40ce4-124">The recording ends when the **Graphics** object is deleted or goes out of scope.</span></span>

<span data-ttu-id="40ce4-125">Im folgenden Beispiel wird die im vorherigen Beispiel erstellte Metadatendatei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="40ce4-125">The following example displays the metafile created in the preceding example.</span></span> <span data-ttu-id="40ce4-126">Die Metadatendatei wird mit der linken oberen Ecke bei (100, 100) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="40ce4-126">The metafile is displayed with its upper-left corner at (100, 100).</span></span>


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



<span data-ttu-id="40ce4-127">Im folgenden Beispiel werden mehrere Eigenschafts Einstellungen (Clippingbereich, Welt Transformation und Glättungs Modus) in einem [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Objekt aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="40ce4-127">The following example records several property settings (clipping region, world transformation, and smoothing mode) in a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="40ce4-128">Anschließend zeichnet der Code mehrere Zeichnungs Anweisungen auf.</span><span class="sxs-lookup"><span data-stu-id="40ce4-128">Then the code records several drawing instructions.</span></span> <span data-ttu-id="40ce4-129">Die Anweisungen und Einstellungen werden in einer Datenträger Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="40ce4-129">The instructions and settings are saved in a disk file.</span></span>


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



<span data-ttu-id="40ce4-130">Im folgenden Beispiel wird das im vorherigen Beispiel erstellte Metadateibild angezeigt.</span><span class="sxs-lookup"><span data-stu-id="40ce4-130">The following example displays the metafile image created in the preceding example.</span></span>


```
myGraphics = new Graphics(hdc);
myMetafile = new Metafile(L"MyDiskFile.emf");
myGraphics->DrawImage(myMetafile, 10, 10);
```



<span data-ttu-id="40ce4-131">Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.</span><span class="sxs-lookup"><span data-stu-id="40ce4-131">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="40ce4-132">Beachten Sie das Antialiasing, den Ellipsen Clippingbereich und die 30-Grad-Rotation.</span><span class="sxs-lookup"><span data-stu-id="40ce4-132">Note the antialiasing, the elliptical clipping region, and the 30-degree rotation.</span></span>

![Screenshot eines Fensters, das eine Ellipse mit Zeilen enthält, die an einem Punkt außerhalb der Ellipse stehen](images/aboutgdip05-art00.png)

 

 



