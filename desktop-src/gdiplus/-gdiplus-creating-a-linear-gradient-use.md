---
description: GDI+ stellt horizontale, vertikale und diagonale lineare Farbverläufe bereit. Standardmäßig ändert sich die Farbe in einem linearen Farbverlauf gleichmäßig. Sie können jedoch einen linearen Farbverlauf anpassen, sodass sich die Farbe auf nicht einheitliche Weise ändert.
ms.assetid: 9b0236b2-be6b-4918-a106-5b0e6c3dd5ff
title: Erstellen eines linearen Farbverlaufs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d66b9f5a3a07061e8b3d19140c25a9f3a33052a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566146"
---
# <a name="creating-a-linear-gradient"></a><span data-ttu-id="bf2e2-105">Erstellen eines linearen Farbverlaufs</span><span class="sxs-lookup"><span data-stu-id="bf2e2-105">Creating a Linear Gradient</span></span>

<span data-ttu-id="bf2e2-106">GDI+ stellt horizontale, vertikale und diagonale lineare Farbverläufe bereit.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-106">GDI+ provides horizontal, vertical, and diagonal linear gradients.</span></span> <span data-ttu-id="bf2e2-107">Standardmäßig ändert sich die Farbe in einem linearen Farbverlauf gleichmäßig.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-107">By default, the color in a linear gradient changes uniformly.</span></span> <span data-ttu-id="bf2e2-108">Sie können jedoch einen linearen Farbverlauf anpassen, sodass sich die Farbe auf nicht einheitliche Weise ändert.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-108">However, you can customize a linear gradient so that the color changes in a non-uniform fashion.</span></span>

-   [<span data-ttu-id="bf2e2-109">Horizontale lineare Farbverläufe</span><span class="sxs-lookup"><span data-stu-id="bf2e2-109">Horizontal Linear Gradients</span></span>](#horizontal-linear-gradients)
-   [<span data-ttu-id="bf2e2-110">Anpassen von linearen Farbverläufen</span><span class="sxs-lookup"><span data-stu-id="bf2e2-110">Customizing Linear Gradients</span></span>](#customizing-linear-gradients)
-   [<span data-ttu-id="bf2e2-111">Diagonale lineare Farbverläufe</span><span class="sxs-lookup"><span data-stu-id="bf2e2-111">Diagonal Linear Gradients</span></span>](#diagonal-linear-gradients)

## <a name="horizontal-linear-gradients"></a><span data-ttu-id="bf2e2-112">Horizontale lineare Farbverläufe</span><span class="sxs-lookup"><span data-stu-id="bf2e2-112">Horizontal Linear Gradients</span></span>

<span data-ttu-id="bf2e2-113">Im folgenden Beispiel wird ein horizontaler linearer Farbverlaufs Pinsel verwendet, um eine Linie, eine Ellipse und ein Rechteck auszufüllen:</span><span class="sxs-lookup"><span data-stu-id="bf2e2-113">The following example uses a horizontal linear gradient brush to fill a line, an ellipse, and a rectangle:</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // opaque red
   Color(255, 0, 0, 255));  // opaque blue

Pen pen(&linGrBrush);

graphics.DrawLine(&pen, 0, 10, 200, 10);
graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



<span data-ttu-id="bf2e2-114">Der [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) -Konstruktor erhält vier Argumente: zwei Punkte und zwei Farben.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-114">The [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) constructor receives four arguments: two points and two colors.</span></span> <span data-ttu-id="bf2e2-115">Der erste Punkt (0, 10) ist mit der ersten Farbe (rot) verknüpft, und der zweite Punkt (200, 10) wird der zweiten Farbe (blau) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-115">The first point (0, 10) is associated with the first color (red), and the second point (200, 10) is associated with the second color (blue).</span></span> <span data-ttu-id="bf2e2-116">Erwartungsgemäß wird die von (0, 10) zu (200, 10) gezogene Linie allmählich von rot in blau geändert.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-116">As you would expect, the line drawn from (0, 10) to (200, 10) changes gradually from red to blue.</span></span>

<span data-ttu-id="bf2e2-117">Die 10S in den Punkten (50, 10) und (200, 10) sind nicht wichtig.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-117">The 10s in the points (50, 10) and (200, 10) are not important.</span></span> <span data-ttu-id="bf2e2-118">Wichtig ist, dass die beiden Punkte dieselbe zweite Koordinate aufweisen – die Linie, die Sie verbindet, ist horizontal.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-118">What's important is that the two points have the same second coordinate — the line connecting them is horizontal.</span></span> <span data-ttu-id="bf2e2-119">Die Ellipse und das Rechteck ändern sich auch allmählich von rot in blau, wenn die horizontale Koordinate von 0 bis 200 wechselt.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-119">The ellipse and the rectangle also change gradually from red to blue as the horizontal coordinate goes from 0 to 200.</span></span>

<span data-ttu-id="bf2e2-120">Die folgende Abbildung zeigt die Zeile, die Ellipse und das Rechteck.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-120">The following illustration shows the line, the ellipse, and the rectangle.</span></span> <span data-ttu-id="bf2e2-121">Beachten Sie, dass der Farbverlauf selbst wiederholt wird, wenn sich die horizontale Koordinate über 200 erhöht.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-121">Note that the color gradient repeats itself as the horizontal coordinate increases beyond 200.</span></span>

![die Abbildung zeigt einen horizontalen Farbverlauf, der eine Linie und eine Ellipse füllt, und ein Rechteck, das länger als die Ellipse ist.](images/lineargradient1.png)

## <a name="customizing-linear-gradients"></a><span data-ttu-id="bf2e2-123">Anpassen von linearen Farbverläufen</span><span class="sxs-lookup"><span data-stu-id="bf2e2-123">Customizing Linear Gradients</span></span>

<span data-ttu-id="bf2e2-124">Im vorherigen Beispiel ändern sich die Farbkomponenten linear, wenn Sie von einer horizontalen Koordinate von 0 zu einer horizontalen Koordinate von 200 wechseln.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-124">In the preceding example, the color components change linearly as you move from a horizontal coordinate of 0 to a horizontal coordinate of 200.</span></span> <span data-ttu-id="bf2e2-125">Beispielsweise weist ein Punkt, dessen erste Koordinate die Hälfte zwischen 0 und 200 ist, eine blaue Komponente auf, die sich in der Mitte zwischen 0 und 255 befindet.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-125">For example, a point whose first coordinate is halfway between 0 and 200 will have a blue component that is halfway between 0 and 255.</span></span>

<span data-ttu-id="bf2e2-126">Mit GDI+ können Sie die Art und Weise anpassen, in der eine Farbe von einem Rand eines Farbverlaufs zum anderen abweicht.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-126">GDI+ allows you to adjust the way a color varies from one edge of a gradient to the other.</span></span> <span data-ttu-id="bf2e2-127">Angenommen, Sie möchten einen Farbverlaufs Pinsel erstellen, der gemäß der folgenden Tabelle von schwarz in rot geändert wird.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-127">Suppose you want to create a gradient brush that changes from black to red according to the following table.</span></span>



| <span data-ttu-id="bf2e2-128">Horizontale Koordinate</span><span class="sxs-lookup"><span data-stu-id="bf2e2-128">Horizontal coordinate</span></span> | <span data-ttu-id="bf2e2-129">RGB-Komponenten</span><span class="sxs-lookup"><span data-stu-id="bf2e2-129">RGB components</span></span> |
|-----------------------|----------------|
| <span data-ttu-id="bf2e2-130">0</span><span class="sxs-lookup"><span data-stu-id="bf2e2-130">0</span></span>                     | <span data-ttu-id="bf2e2-131">(0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="bf2e2-131">(0, 0, 0)</span></span>      |
| <span data-ttu-id="bf2e2-132">40</span><span class="sxs-lookup"><span data-stu-id="bf2e2-132">40</span></span>                    | <span data-ttu-id="bf2e2-133">(128, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="bf2e2-133">(128, 0, 0)</span></span>    |
| <span data-ttu-id="bf2e2-134">200</span><span class="sxs-lookup"><span data-stu-id="bf2e2-134">200</span></span>                   | <span data-ttu-id="bf2e2-135">(255, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="bf2e2-135">(255, 0, 0)</span></span>    |



 

<span data-ttu-id="bf2e2-136">Beachten Sie, dass die rote Komponente die halbe Intensität hat, wenn die horizontale Koordinate nur 20 Prozent der Art von 0 bis 200 ist.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-136">Note that the red component is at half intensity when the horizontal coordinate is only 20 percent of the way from 0 to 200.</span></span>

<span data-ttu-id="bf2e2-137">Im folgenden Beispiel wird die [**LinearGradientBrush:: setblend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) -Methode eines [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) -Objekts aufgerufen, um drei relative Intensitäten mit drei relativen Positionen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-137">The following example calls the [**LinearGradientBrush::SetBlend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) method of a [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) object to associate three relative intensities with three relative positions.</span></span> <span data-ttu-id="bf2e2-138">Wie in der obigen Tabelle ist eine relative Intensität von 0,5 mit einer relativen Position von 0,2 verknüpft.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-138">As in the preceding table, a relative intensity of 0.5 is associated with a relative position of 0.2.</span></span> <span data-ttu-id="bf2e2-139">Der Code füllt eine Ellipse und ein Rechteck mit dem Farbverlaufs Pinsel.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-139">The code fills an ellipse and a rectangle with the gradient brush.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 0, 0, 0),     // opaque black 
   Color(255, 255, 0, 0));  // opaque red

REAL relativeIntensities[] = {0.0f, 0.5f, 1.0f};
REAL relativePositions[]   = {0.0f, 0.2f, 1.0f};

linGrBrush.SetBlend(relativeIntensities, relativePositions, 3);

graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



<span data-ttu-id="bf2e2-140">In der folgenden Abbildung werden die resultierende Ellipse und das Rechteck gezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-140">The following illustration shows the resulting ellipse and rectangle.</span></span>

![die Abbildung zeigt einen horizontalen Farbverlauf, der eine Ellipse und ein Rechteck füllt, das länger als die Ellipse ist.](images/lineargradient2.png)

## <a name="diagonal-linear-gradients"></a><span data-ttu-id="bf2e2-142">Diagonale lineare Farbverläufe</span><span class="sxs-lookup"><span data-stu-id="bf2e2-142">Diagonal Linear Gradients</span></span>

<span data-ttu-id="bf2e2-143">Die Farbverläufe in den vorangehenden Beispielen waren horizontal. Das heißt, die Farbe ändert sich allmählich, wenn Sie sich entlang einer horizontalen Linie bewegen.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-143">The gradients in the preceding examples have been horizontal; that is, the color changes gradually as you move along any horizontal line.</span></span> <span data-ttu-id="bf2e2-144">Sie können auch vertikale Farbverläufe und diagonale Farbverläufe definieren.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-144">You can also define vertical gradients and diagonal gradients.</span></span> <span data-ttu-id="bf2e2-145">Der folgende Code übergibt die Punkte (0,0) und (200, 100) an einen [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) -Konstruktor.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-145">The following code passes the points (0, 0) and (200, 100) to a [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) constructor.</span></span> <span data-ttu-id="bf2e2-146">Die Farbe blau ist (0,0) zugeordnet, und die Farbe grün ist zugeordnet (200, 100).</span><span class="sxs-lookup"><span data-stu-id="bf2e2-146">The color blue is associated with (0, 0), and the color green is associated with (200, 100).</span></span> <span data-ttu-id="bf2e2-147">Eine Linie (mit der Stift Breite 10) und eine Ellipse werden mit dem linearen Farbverlaufs Pinsel gefüllt.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-147">A line (with pen width 10) and an ellipse are filled with the linear gradient brush.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 0),
   Point(200, 100),
   Color(255, 0, 0, 255),   // opaque blue
   Color(255, 0, 255, 0));  // opaque green

Pen pen(&linGrBrush, 10);

graphics.DrawLine(&pen, 0, 0, 600, 300);
graphics.FillEllipse(&linGrBrush, 10, 100, 200, 100);
```



<span data-ttu-id="bf2e2-148">Die folgende Abbildung zeigt die Zeile und die Ellipse.</span><span class="sxs-lookup"><span data-stu-id="bf2e2-148">The following illustration shows the line and the ellipse.</span></span> <span data-ttu-id="bf2e2-149">Beachten Sie, dass sich die Farbe in der Ellipse allmählich ändert, wenn Sie eine beliebige Zeile bewegen, die parallel zur Zeile, die durchläuft (0,0) und (200, 100).</span><span class="sxs-lookup"><span data-stu-id="bf2e2-149">Note that the color in the ellipse changes gradually as you move along any line that is parallel to the line passing through (0, 0) and (200, 100).</span></span>

![Abbildung mit einem diagonalen Farbverlauf, der eine Ellipse und eine diagonal Linie füllt](images/lineargradient3.png)

 

 



