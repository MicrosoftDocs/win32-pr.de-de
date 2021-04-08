---
title: Beispiel-Rendering-Code
description: Beispiel-Rendering-Code
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- Visualisierungen, Beispielcode
- benutzerdefinierte Visualisierungen, Beispielcode
- Visualisierungen, Rendering-Funktion
- benutzerdefinierte Visualisierungen, Rendering-Funktion
- Funktion "Rendering", Beispielcode
- Beispiele, Rendering-Funktion für Visualisierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1ee5d00bc1aed5bd8bd91880e43e2ac2d1f6bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037204"
---
# <a name="sample-render-code"></a><span data-ttu-id="1c2f9-109">Beispiel-Rendering-Code</span><span class="sxs-lookup"><span data-stu-id="1c2f9-109">Sample Render Code</span></span>

<span data-ttu-id="1c2f9-110">Hier sehen Sie einen Beispielcode, der die Funktion " **Rendering** " verwendet, um eine Linie auf dem Bildschirm zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-110">Here is some sample code that uses the **Render** function to draw a line across the screen.</span></span> <span data-ttu-id="1c2f9-111">Die Höhe der Zeile wird durch den Wellenform-Wert definiert.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-111">The height of the line is defined by the waveform value.</span></span>


```C++
STDMETHODIMP CStock::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    // Create new brushes and pens.
    HBRUSH hNewBrush = ::CreateSolidBrush( 0 );
    // Create a new solid pen the color of the foreground.
    HPEN hNewPen = ::CreatePen( PS_SOLID, 0, m_clrForeground );


    // Add the pen to the device context.
    HPEN hOldPen= static_cast<HPEN>(::SelectObject( hdc, hNewPen ));

    // Fill the background with the black brush.
    ::FillRect( hdc, prc, hNewBrush );

    // Get the y value from the waveform.
    int y = pLevels->waveform[0][0];

    // Draw the line from left to right.
    ::MoveToEx( hdc, prc->left, y, NULL);  
    ::LineTo(hdc, prc->right, y); 

    // Delete your brush.
    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }
    // Delete your pen.
    if (hNewPen)
    {
        ::SelectObject( hdc, hOldPen );
        ::DeleteObject( hNewPen );
    }

    // You're done for this round.
    return S_OK;
}

```



<span data-ttu-id="1c2f9-112">Die Funktion " **Rendering** " ist der Ort, an dem die Hauptarbeit Ihres Codes erfolgt.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-112">The **Render** function is where the main work of your code takes place.</span></span> <span data-ttu-id="1c2f9-113">Jedes Mal, wenn Windows Media Player eine Momentaufnahme der Audiodatei aufnimmt, wird diese Funktion aufgerufen, und der Code wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-113">Every time Windows Media Player takes a snapshot of the audio, it will call this function and your code will run.</span></span>

<span data-ttu-id="1c2f9-114">Dieser Code führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="1c2f9-114">This code performs the following tasks.</span></span> <span data-ttu-id="1c2f9-115">Weitere Informationen zu bestimmten Funktionen finden Sie im Microsoft Windows-Plattform-SDK für 32-Bit-Windows.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-115">Refer to the Microsoft Windows Platform SDK for 32-bit Windows for more details about specific functions.</span></span>

## <a name="creating-objects"></a><span data-ttu-id="1c2f9-116">Erstellen von Objekten</span><span class="sxs-lookup"><span data-stu-id="1c2f9-116">Creating Objects</span></span>

<span data-ttu-id="1c2f9-117">Normalerweise verwenden Sie die Zeichnungsfunktionen von Microsoft Windows Graphical Display Interface (GDI).</span><span class="sxs-lookup"><span data-stu-id="1c2f9-117">Usually you will be using the drawing functions that come with the Microsoft Windows Graphical Display Interface (GDI).</span></span> <span data-ttu-id="1c2f9-118">Sie müssen Stifte erstellen, um Linien und Pinsel zum Auffüllen von Bereichen zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-118">You need to create pens to draw lines and brushes to fill areas.</span></span>

<span data-ttu-id="1c2f9-119">Ein solider schwarzer Pinsel wird erstellt, um den Hintergrund zu füllen.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-119">A solid black brush is created to fill in the background.</span></span>

<span data-ttu-id="1c2f9-120">Ein Vollstift wird erstellt, um eine Linie zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-120">A solid pen is created to draw a line.</span></span> <span data-ttu-id="1c2f9-121">Die Farbe entspricht der Vordergrundfarbe, die von der Skin definiert wird, in der die Visualisierung angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-121">The color will be the foreground color as defined by the skin that is going to display the visualization.</span></span>

## <a name="adding-the-object-to-the-dc"></a><span data-ttu-id="1c2f9-122">Hinzufügen des Objekts zum DC</span><span class="sxs-lookup"><span data-stu-id="1c2f9-122">Adding the Object to the DC</span></span>

<span data-ttu-id="1c2f9-123">Sie müssen den Stift dem Gerätekontext (DC) hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-123">You need to add the pen to the device context (DC).</span></span> <span data-ttu-id="1c2f9-124">Der Domänen Controller ist der Teil des Arbeitsspeichers, in dem alle Zeichnungsdaten und Objekte gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-124">The DC is the portion of memory that all drawing data and objects are stored in.</span></span> <span data-ttu-id="1c2f9-125">Im Wesentlichen ist der Domänen Controller der Fenster Traffic Manager, mit dem alles grafisch nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-125">Essentially the DC is the window traffic manager that keeps track of everything graphical.</span></span>

<span data-ttu-id="1c2f9-126">Sie *müssen das von* Ihnen erstellte Pen-Objekt umwandeln und als alten Stift speichern.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-126">You need to *cast* the pen object you created and store it as an old pen.</span></span> <span data-ttu-id="1c2f9-127">Verwenden Sie diese Codierungstechnik für alle neuen Stifte.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-127">Use this coding technique for all new pens.</span></span> <span data-ttu-id="1c2f9-128">Diese Technik ist für die 32-Bit-Programmierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-128">This technique is required for 32-bit programming.</span></span>

## <a name="filling-in-the-background"></a><span data-ttu-id="1c2f9-129">Ausfüllen des Hintergrunds</span><span class="sxs-lookup"><span data-stu-id="1c2f9-129">Filling in the Background</span></span>

<span data-ttu-id="1c2f9-130">Sie können jetzt zeichnen.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-130">You now are ready to draw.</span></span> <span data-ttu-id="1c2f9-131">Die **fillRect** -Funktion wird das Rechteck des Fensters auffüllen, wie durch die Parameter der Funktion " **Rendering** " definiert.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-131">The **FillRect** function will fill the rectangle of the window, as defined by the parameters of the **Render** function.</span></span> <span data-ttu-id="1c2f9-132">Das Rechteck ist mit einem schwarzen Pinsel gefüllt.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-132">The rectangle is filled with a black brush.</span></span>

## <a name="getting-audio-data"></a><span data-ttu-id="1c2f9-133">Audiodaten werden erhalten.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-133">Getting Audio Data</span></span>

<span data-ttu-id="1c2f9-134">Als Nächstes ruft der Code einige Audiodaten aus Windows Media Player ab.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-134">Next the code gets some audio data from Windows Media Player.</span></span> <span data-ttu-id="1c2f9-135">Mithilfe des Wellenform-Arrays können Sie den aktuellen Wert der audiopotenz zu dem Zeitpunkt, zu dem die Momentaufnahme erstellt wurde, erhalten.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-135">By using the waveform array, you can get the current value of the audio power at the moment the snapshot was taken.</span></span> <span data-ttu-id="1c2f9-136">In diesem Fall nehmen Sie die Audiodaten des linken Kanals an.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-136">In this case, you are taking the audio data of the left channel.</span></span> <span data-ttu-id="1c2f9-137">Der erste Wert im Array ist der erste 1024. der audiostrommomentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-137">The first value in the array is the first 1024th of the audio power snapshot.</span></span>

<span data-ttu-id="1c2f9-138">Diese Informationen werden verwendet, um eine Zeile anzuzeigen, deren Höhe mit der audiostrommomentaufnahme übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-138">This information will be used to display a line whose height will match the audio power snapshot.</span></span>

## <a name="draw-the-line"></a><span data-ttu-id="1c2f9-139">Linie zeichnen</span><span class="sxs-lookup"><span data-stu-id="1c2f9-139">Draw the Line</span></span>

<span data-ttu-id="1c2f9-140">Die Linie wird von links nach rechts mithilfe der Funktionen " **muveumex** " und " **LineTo** GDI" gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-140">The line is drawn from left to right using the **MoveToEx** and **LineTo** GDI functions.</span></span>

<span data-ttu-id="1c2f9-141">Zuerst verschieben Sie den Stift an den Ausgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-141">First you move the pen to the starting point.</span></span> <span data-ttu-id="1c2f9-142">In diesem Fall werden x und y verwendet, um die Werte von links nach rechts und von oben nach unten zu definieren, die dem Benutzer auf dem Bildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-142">In this case, x and y are used to define the left-to-right and top-to-bottom values the user will see on the screen.</span></span> <span data-ttu-id="1c2f9-143">X wird durch die Rechteck-PRC und insbesondere durch den Wert von PRC->left definiert.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-143">X is defined by the rectangle prc and specifically by the value of prc->left.</span></span> <span data-ttu-id="1c2f9-144">Y ist zu diesem Zeitpunkt als Wert der Wellenform-Daten definiert.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-144">Y is defined as the value of the waveform data at that moment.</span></span>

<span data-ttu-id="1c2f9-145">Anschließend zeichnen Sie eine Linie auf die andere Seite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-145">Then you draw a line to the other side of the window.</span></span> <span data-ttu-id="1c2f9-146">Der Punkt, zu dem Sie die Linie zeichnen, ist wieder ein x-, y-Wert.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-146">The point you draw the line to is again an x, y value.</span></span> <span data-ttu-id="1c2f9-147">X wird durch die Rechteck-PRC definiert, aber diesmal von PRC->Recht.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-147">X is defined by the rectangle prc, but this time by prc->right.</span></span> <span data-ttu-id="1c2f9-148">Y wird weiterhin durch die Wellenform Daten definiert und entspricht dem Punkt, von dem Sie gestartet haben, da Sie eine gerade Linie von links nach rechts zeichnen.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-148">Y is still defined by the waveform data and is the same as the point you started from, because you are drawing a straight line from left to right.</span></span>

## <a name="clean-up-everything"></a><span data-ttu-id="1c2f9-149">Alles bereinigen</span><span class="sxs-lookup"><span data-stu-id="1c2f9-149">Clean up Everything</span></span>

<span data-ttu-id="1c2f9-150">Sie müssen die von Ihnen erstellten Objekte löschen.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-150">You must delete the objects you create.</span></span> <span data-ttu-id="1c2f9-151">Insbesondere müssen Sie alle Pinsel und Stifte löschen, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-151">Specifically you must delete any and all brushes and pens you create.</span></span> <span data-ttu-id="1c2f9-152">Es empfiehlt sich, Stifte und Pinsel zu löschen, wenn Sie Sie nicht mehr verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-152">It is good practice to delete pens and brushes when you finish using them.</span></span>

<span data-ttu-id="1c2f9-153">Wenn Sie Sie nicht löschen, bevor Sie die Implementierung der **Rendering** -Funktion abschließen, stürzt die Visualisierung innerhalb weniger Minuten ab.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-153">If you do not delete them before finishing your implementation of the **Render** function, your visualization will crash in a minute or less.</span></span> <span data-ttu-id="1c2f9-154">Sie müssen die Anzahl der Stifte und Pinsel beibehalten und alle einzelnen Stifte zerstören.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-154">You must keep a count of your pens and brushes and destroy every single one.</span></span> <span data-ttu-id="1c2f9-155">Achten Sie besonders darauf, keine Stifte innerhalb einer Code Schleife zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-155">Be especially careful not to create pens inside a code loop.</span></span>

<span data-ttu-id="1c2f9-156">Verwenden Sie die im Beispiel angegebene Codierungsmethode, um ihre Stifte und Pinsel zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-156">Use the coding technique given in the example to destroy your pens and brushes.</span></span>

-   <span data-ttu-id="1c2f9-157">**Wichtig** Zerstören Sie Ihre Stifte und Pinsel!</span><span class="sxs-lookup"><span data-stu-id="1c2f9-157">**Important** Destroy your pens and brushes!</span></span>

<span data-ttu-id="1c2f9-158">Wenn Sie die Bereinigung abgeschlossen haben, stellen Sie sicher, dass Sie den Wert OK zurückgibt, \_ damit Windows Media Player weiß, dass Sie das Zeichnen abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-158">When you have finished cleaning up, be sure to return S\_OK so that Windows Media Player knows you are finished drawing.</span></span> <span data-ttu-id="1c2f9-159">Sobald Sie fertig sind, wird das Zeichnen in das Fenster übertragen, eine weitere Momentaufnahme wird erstellt, das **Rendering** fordert den Code auf, Sie erneut zu zeichnen, usw.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-159">Once you finish, your drawing will be transferred to the window, another snapshot will be taken, **Render** will ask your code to draw again, and so on.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c2f9-160">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1c2f9-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c2f9-161">**Implementieren von Rendering**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-161">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




