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
# <a name="recording-metafiles"></a><span data-ttu-id="449c0-103">Aufzeichnen von Metafiles</span><span class="sxs-lookup"><span data-stu-id="449c0-103">Recording Metafiles</span></span>

<span data-ttu-id="449c0-104">Mit der [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Klasse, die von der [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse erbt, können Sie eine Sequenz von Zeichnungs Befehlen aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="449c0-104">The [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class, which inherits from the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, allows you to record a sequence of drawing commands.</span></span> <span data-ttu-id="449c0-105">Die aufgezeichneten Befehle können im Arbeitsspeicher gespeichert, in einer Datei gespeichert oder in einem Stream gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="449c0-105">The recorded commands can be stored in memory, saved to a file, or saved to a stream.</span></span> <span data-ttu-id="449c0-106">Metadatendateien können Vektorgrafiken, Rasterbilder und Text enthalten.</span><span class="sxs-lookup"><span data-stu-id="449c0-106">Metafiles can contain vector graphics, raster images, and text.</span></span>

<span data-ttu-id="449c0-107">Im folgenden Beispiel wird ein [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="449c0-107">The following example creates a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="449c0-108">Im Code wird das **Metafile** -Objekt verwendet, um eine Sequenz von Grafik Befehlen aufzuzeichnen und dann die aufgezeichneten Befehle in einer Datei namens SampleMetafile. EMF zu speichern.</span><span class="sxs-lookup"><span data-stu-id="449c0-108">The code uses the **Metafile** object to record a sequence of graphics commands and then saves the recorded commands in a file named SampleMetafile.emf.</span></span> <span data-ttu-id="449c0-109">Beachten Sie, dass der **Metafile** -Konstruktor ein Gerätekontext handle empfängt, und der [**grafikkonstruktor**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) empfängt die Adresse des **metadateiobjekts** .</span><span class="sxs-lookup"><span data-stu-id="449c0-109">Note that the **Metafile** constructor receives a device context handle, and the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor receives the address of the **Metafile** object.</span></span> <span data-ttu-id="449c0-110">Die Aufzeichnung wird beendet (und die aufgezeichneten Befehle werden in der Datei gespeichert), wenn das **Grafik** Objekt den Gültigkeitsbereich verlässt.</span><span class="sxs-lookup"><span data-stu-id="449c0-110">The recording stops (and the recorded commands are saved to the file) when the **Graphics** object goes out of scope.</span></span> <span data-ttu-id="449c0-111">In den letzten beiden Codezeilen wird die Metadatendatei angezeigt, indem ein neues **Grafik** Objekt erstellt und die Adresse des **metadateiobjekts** an die **DrawImage** -Methode dieses **Grafik** Objekts übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="449c0-111">The last two lines of code display the metafile by creating a new **Graphics** object and passing the address of the **Metafile** object to the **DrawImage** method of that **Graphics** object.</span></span> <span data-ttu-id="449c0-112">Beachten Sie, dass der Code das gleiche **metadateiobjekt** verwendet, um die Metadatei aufzuzeichnen und anzuzeigen (wiederzugeben).</span><span class="sxs-lookup"><span data-stu-id="449c0-112">Note that the code uses the same **Metafile** object to record and to display (play back) the metafile.</span></span>


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
> <span data-ttu-id="449c0-113">Um eine Metadatei aufzuzeichnen, müssen Sie ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt auf Grundlage eines [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Objekts erstellen.</span><span class="sxs-lookup"><span data-stu-id="449c0-113">To record a metafile, you must construct a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="449c0-114">Die Aufzeichnung der Metadatei wird beendet, wenn das **Grafik** Objekt gelöscht wird oder den Gültigkeitsbereich verlässt.</span><span class="sxs-lookup"><span data-stu-id="449c0-114">The recording of the metafile ends when that **Graphics** object is deleted or goes out of scope.</span></span>

 

<span data-ttu-id="449c0-115">Eine Metadatei enthält Ihren eigenen Grafik Zustand, der durch das [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt definiert wird, das zum Aufzeichnen der Metadatei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="449c0-115">A metafile contains its own graphics state, which is defined by the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object used to record the metafile.</span></span> <span data-ttu-id="449c0-116">Alle Eigenschaften des **Grafik** Objekts (Clip Bereich, World Transformation, Glättung und ähnliches), die Sie beim Aufzeichnen der Metadatei festlegen, werden in der Metadatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="449c0-116">Any properties of the **Graphics** object (clip region, world transformation, smoothing mode, and the like) that you set while recording the metafile will be stored in the metafile.</span></span> <span data-ttu-id="449c0-117">Wenn Sie die Metadatei anzeigen, wird die Zeichnung entsprechend den gespeicherten Eigenschaften durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="449c0-117">When you display the metafile, the drawing will be done according to those stored properties.</span></span>

<span data-ttu-id="449c0-118">Nehmen Sie im folgenden Beispiel an, dass der Glättungs Modus während der Aufzeichnung der Metadatei auf smoothingmudenormal festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="449c0-118">In the following example, assume that the smoothing mode was set to SmoothingModeNormal during the recording of the metafile.</span></span> <span data-ttu-id="449c0-119">Obwohl der Glättungs Modus des [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts, das für die Wiedergabe verwendet wird, auf "smoothingmodehighquality" festgelegt ist, wird die Metadatei entsprechend der Einstellung "smoothingmudenormal" wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="449c0-119">Even though the smoothing mode of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object used for playback is set to SmoothingModeHighQuality, the metafile will be played according to the SmoothingModeNormal setting.</span></span> <span data-ttu-id="449c0-120">Dabei handelt es sich um den Glättungs Modus, der während der wichtigen Aufzeichnung festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="449c0-120">It is the smoothing mode set during the recording that is important, not the smoothing mode set prior to playback.</span></span>


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 



