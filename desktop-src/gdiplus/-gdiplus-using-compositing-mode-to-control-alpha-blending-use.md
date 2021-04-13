---
description: 'Es kann vorkommen, dass Sie eine Offscreen-Bitmap erstellen möchten, die über die folgenden Eigenschaften verfügt:'
ms.assetid: 2a7590ce-daf4-4892-a838-603e3f89b1bb
title: Verwenden des Compositing-Modus zum Steuern der Alpha Mischung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db54c71ac9687a1ddf28db09b922b7799d0ebaa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978912"
---
# <a name="using-compositing-mode-to-control-alpha-blending"></a><span data-ttu-id="ed4ca-103">Verwenden des Compositing-Modus zum Steuern der Alpha Mischung</span><span class="sxs-lookup"><span data-stu-id="ed4ca-103">Using Compositing Mode to Control Alpha Blending</span></span>

<span data-ttu-id="ed4ca-104">Es kann vorkommen, dass Sie eine Offscreen-Bitmap erstellen möchten, die über die folgenden Eigenschaften verfügt:</span><span class="sxs-lookup"><span data-stu-id="ed4ca-104">There might be times when you want to create an off-screen bitmap that has the following characteristics:</span></span>

-   <span data-ttu-id="ed4ca-105">Farben haben alpha-Werte, die kleiner als 255 sind.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-105">Colors have alpha values that are less than 255.</span></span>
-   <span data-ttu-id="ed4ca-106">Farben werden bei der Erstellung der Bitmap nicht mit einander gemischt.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-106">Colors are not alpha blended with each other as you create the bitmap.</span></span>
-   <span data-ttu-id="ed4ca-107">Wenn Sie die fertige Bitmap anzeigen, werden Farben in der Bitmap mit den Hintergrundfarben auf dem Anzeigegerät gemischt.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-107">When you display the finished bitmap, colors in the bitmap are alpha blended with the background colors on the display device.</span></span>

<span data-ttu-id="ed4ca-108">Um eine solche Bitmap zu erstellen, erstellen Sie ein leeres [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekt, und erstellen Sie dann auf der Grundlage dieser Bitmap ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-108">To create such a bitmap, construct a blank [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object, and then construct a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on that bitmap.</span></span> <span data-ttu-id="ed4ca-109">Legen Sie den Zusammensetzung-Modus des **Grafik** Objekts auf compositingmodesourcecopy fest.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-109">Set the compositing mode of the **Graphics** object to CompositingModeSourceCopy.</span></span>

<span data-ttu-id="ed4ca-110">Im folgenden Beispiel wird ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt erstellt, das auf einem [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekt basiert.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-110">The following example creates a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="ed4ca-111">Der Code verwendet das **Grafik** Objekt zusammen mit zwei semitransparenten Pinseln (Alpha = 160), um die Bitmap zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-111">The code uses the **Graphics** object along with two semitransparent brushes (alpha = 160) to paint on the bitmap.</span></span> <span data-ttu-id="ed4ca-112">Der Code füllt eine rote Ellipse und eine grüne Ellipse mithilfe der semitransparenten Pinsel.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-112">The code fills a red ellipse and a green ellipse using the semitransparent brushes.</span></span> <span data-ttu-id="ed4ca-113">Die grüne Ellipse überlappt die rote Ellipse, das grüne wird jedoch nicht mit der roten Ellipse kombiniert, da der Zusammensetzung-Modus des **Grafik** Objekts auf compositingmodesourcecopy festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-113">The green ellipse overlaps the red ellipse, but the green is not blended with the red because the compositing mode of the **Graphics** object is set to CompositingModeSourceCopy.</span></span>

<span data-ttu-id="ed4ca-114">Im nächsten Schritt bereitet der Code das Zeichnen auf dem Bildschirm vor, indem [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) aufgerufen und ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt auf der Grundlage eines Geräte Kontexts erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-114">Next the code prepares to draw on the screen by calling [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) and creating a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a device context.</span></span> <span data-ttu-id="ed4ca-115">Der Code zeichnet die Bitmap zweimal auf dem Bildschirm: einmal auf einem weißen Hintergrund und einmal in einem mehrfarbigen Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-115">The code draws the bitmap on the screen twice: once on a white background and once on a multicolored background.</span></span> <span data-ttu-id="ed4ca-116">Die Pixel in der Bitmap, die Teil der beiden Ellipsen sind, haben eine Alpha Komponente von 160, sodass die Ellipsen mit den Hintergrundfarben auf dem Bildschirm kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-116">The pixels in the bitmap that are part of the two ellipses have an alpha component of 160, so the ellipses are blended with the background colors on the screen.</span></span>


```
// Create a blank bitmap.
Bitmap bitmap(180, 100);
// Create a Graphics object that can be used to draw on the bitmap.
Graphics bitmapGraphics(&bitmap);
// Create a red brush and a green brush, each with an alpha value of 160.
SolidBrush redBrush(Color(210, 255, 0, 0));
SolidBrush greenBrush(Color(210, 0, 255, 0));
// Set the compositing mode so that when overlapping ellipses are drawn,
// the colors of the ellipses are not blended.
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
// Fill an ellipse using a red brush that has an alpha value of 160.
bitmapGraphics.FillEllipse(&redBrush, 0, 0, 150, 70);
// Fill a second ellipse using green brush that has an alpha value of 160. 
// The green ellipse overlaps the red ellipse, but the green is not 
// blended with the red.
bitmapGraphics.FillEllipse(&greenBrush, 30, 30, 150, 70);
// Prepare to draw on the screen.
hdc = BeginPaint(hWnd, &ps);
Graphics* pGraphics = new Graphics(hdc);
pGraphics->SetCompositingQuality(CompositingQualityGammaCorrected);
// Draw a multicolored background.
SolidBrush brush(Color((ARGB)Color::Aqua));
pGraphics->FillRectangle(&brush, 200, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Yellow));
pGraphics->FillRectangle(&brush, 260, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Fuchsia));
pGraphics->FillRectangle(&brush, 320, 0, 60, 100);
   
// Display the bitmap on a white background.
pGraphics->DrawImage(&bitmap, 0, 0);
// Display the bitmap on a multicolored background.
pGraphics->DrawImage(&bitmap, 200, 0);
delete pGraphics;
EndPaint(hWnd, &ps);
```



<span data-ttu-id="ed4ca-117">Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-117">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="ed4ca-118">Beachten Sie, dass die Ellipsen mit dem Hintergrund kombiniert werden, aber nicht miteinander vermischt werden.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-118">Note that the ellipses are blended with the background, but they are not blended with each other.</span></span>

![Abbildung: zwei anders farbige Ellipsen, die jeweils mit dem mehrfarbigen Hintergrund kombiniert werden](images/sourcecopy.png)

<span data-ttu-id="ed4ca-120">Das vorangehende Codebeispiel enthält die folgende-Anweisung:</span><span class="sxs-lookup"><span data-stu-id="ed4ca-120">The preceding code example has the following statement:</span></span>


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



<span data-ttu-id="ed4ca-121">Wenn Sie möchten, dass die Ellipsen miteinander und mit dem Hintergrund kombiniert werden sollen, ändern Sie die Anweisung wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ed4ca-121">If you want the ellipses to be blended with each other as well as with the background, change that statement to the following:</span></span>


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



<span data-ttu-id="ed4ca-122">Die folgende Abbildung zeigt die Ausgabe des überarbeiteten Codes.</span><span class="sxs-lookup"><span data-stu-id="ed4ca-122">The following illustration shows the output of the revised code.</span></span>

![Verwenden des Zusammensetzung-Modus zum Steuern der Alpha Blending-Darstellung](images/sourceover.png)

 

 



