---
description: In diesem Thema werden die frei Hand Analyse-APIs vorgestellt.
ms.assetid: a3126930-2802-43c7-9e98-3a73498ac3f5
title: Grundlegende Erkennungs-und Handschrift Analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9858ceedba245a733d4dc0055dd0747507654f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393241"
---
# <a name="basic-recognition-and-ink-analysis"></a><span data-ttu-id="59f3a-103">Grundlegende Erkennungs-und Handschrift Analyse</span><span class="sxs-lookup"><span data-stu-id="59f3a-103">Basic Recognition and Ink Analysis</span></span>

<span data-ttu-id="59f3a-104">In diesem Thema werden die frei Hand Analyse-APIs vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="59f3a-104">This topic introduces the Ink Analysis APIs.</span></span>

## <a name="simple-recognition"></a><span data-ttu-id="59f3a-105">Einfache Erkennung</span><span class="sxs-lookup"><span data-stu-id="59f3a-105">Simple Recognition</span></span>

<span data-ttu-id="59f3a-106">Die grundlegende Funktionalität, die von der frei Hand Analyse-API verfügbar gemacht wird, ist der Zugriff auf die Erkennungsergebnisse für eine bestimmte Freihand.</span><span class="sxs-lookup"><span data-stu-id="59f3a-106">The basic functionality exposed by the ink analysis API is access to the recognition results for a given piece of ink.</span></span> <span data-ttu-id="59f3a-107">Dies ist unkompliziert und einfach, wie im folgenden Beispielcode gezeigt.</span><span class="sxs-lookup"><span data-stu-id="59f3a-107">This is straightforward and simple to do, as shown in the following example code.</span></span>


```C++
// Instantiate a new InkAnalyzer object, passing in an Ink object and
// the synchronizing object.
InkAnalyzer ia = new InkAnalyzer(myInkOverlay.Ink, this);

// Associate the Strokes to be recognized with the InkAnalyzer.
ia.AddStrokes(myInkOverlay.Ink.Strokes);

// Synchronously recognize the Strokes.
ia.Analyze();

// Access the results and display.
string myResults = ia.GetRecognizedString();
MessageBox.Show(myResults);
```



<span data-ttu-id="59f3a-108">Bei den Ergebnissen des Erkennungs Vorgangs handelt es sich einfach um einen Zeichen folgen Wert, der den erkannten Wert des handschriftlichen frei Hand Zeichens darstellt.</span><span class="sxs-lookup"><span data-stu-id="59f3a-108">The results of the recognition operation are simply a string value representing the recognized value of the handwritten ink.</span></span> <span data-ttu-id="59f3a-109">Die frei Hand Analyse-API macht viel mehr Erkennungsfunktionen als nur die erkannte Zeichenfolge, aber dies ist der häufigste Vorgang.</span><span class="sxs-lookup"><span data-stu-id="59f3a-109">The ink analysis API exposes much more recognition functionality than just the recognized string, but that is the most common operation.</span></span>

## <a name="incremental-recognition"></a><span data-ttu-id="59f3a-110">Krementelle Erkennung</span><span class="sxs-lookup"><span data-stu-id="59f3a-110">Incremental Recognition</span></span>

<span data-ttu-id="59f3a-111">Der Erkennungsprozess dauert eine Weile und blockiert den Zugriff auf die Anwendung, indem der UI-Thread der Anwendung blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="59f3a-111">The recognition process takes time to complete, blocking access to the application by blocking the application's UI thread.</span></span> <span data-ttu-id="59f3a-112">Daher kann es teuer und frustrierend sein, dass der Endbenutzer synchron auf Ergebnisse wartet.</span><span class="sxs-lookup"><span data-stu-id="59f3a-112">It can therefore be costly and frustrating to the end-user to wait synchronously for results.</span></span> <span data-ttu-id="59f3a-113">Viele Tablet PC-Anwendungen erfordern das Erkennen von mehr als wenigen Zeilen Freihand, und ein inkrementeller Ansatz zum Erkennen von Strichen in einem Hintergrund Thread ist die optimale Strategie.</span><span class="sxs-lookup"><span data-stu-id="59f3a-113">Many Tablet PC applications require the recognition of more than a few lines of ink, and an incremental approach to recognizing strokes on a background thread is the optimal strategy.</span></span> <span data-ttu-id="59f3a-114">Der Vorteil eines inkrementellen Ansatzes anstelle eines Massen Vorgangs besteht darin, dass es die Erkennung der Striche über einen Zeitraum hinweg ermöglicht, wobei die Arbeit im Hintergrund Thread statt synchron im Vordergrund Thread verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="59f3a-114">The advantage of an incremental approach instead of a bulk operation is that it allows the recognition of the strokes to happen over a period of time, spreading out the work on the background thread instead of synchronously on the foreground thread.</span></span> <span data-ttu-id="59f3a-115">Um die inkrementelle Analyse zu unterstützen, verfügt das [**InkAnalyzer**](inkanalyzer.md) -Objekt über eine [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) -Methode, die die Erstellung und Verwaltung eines Hintergrundthreads für die Anwendung behandelt.</span><span class="sxs-lookup"><span data-stu-id="59f3a-115">To support incremental analysis, the [**InkAnalyzer**](inkanalyzer.md) object has a [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method, which handles the creation and management of a background thread for the application.</span></span> <span data-ttu-id="59f3a-116">Der **InkAnalyzer** übernimmt auch automatisch die Verwaltung der erkannten und bereits erkannten Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="59f3a-116">The **InkAnalyzer** also automatically takes care of managing what needs to be recognized and what has already been recognized.</span></span>

<span data-ttu-id="59f3a-117">Daher gibt es zwei Mechanismen zum Erreichen von Erkennungs Ergebnissen:</span><span class="sxs-lookup"><span data-stu-id="59f3a-117">Thus, there are two mechanisms for attaining recognition results:</span></span>

-   <span data-ttu-id="59f3a-118">Die [**Analyse**](iinkanalyzer-analyze.md) Methode (synchrone Analyse), die am besten für Folgendes funktioniert:</span><span class="sxs-lookup"><span data-stu-id="59f3a-118">The [**Analyze**](iinkanalyzer-analyze.md) method (synchronous analysis), which works best for:</span></span>

    -   <span data-ttu-id="59f3a-119">Kleine Menge an frei Hand Eingaben.</span><span class="sxs-lookup"><span data-stu-id="59f3a-119">Small amounts of ink.</span></span>
    -   <span data-ttu-id="59f3a-120">Wenn Ergebnisse erforderlich sind, bevor mit dem nächsten Vorgang in der Anwendung fortgefahren wird, z. b. Wenn eine Korrektur Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="59f3a-120">When results are required before proceeding to the next operation in the application, such as when displaying a correction user interface.</span></span>

-   <span data-ttu-id="59f3a-121">Die [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) -Methode (asynchrone Analyse), die am besten für Folgendes funktioniert:</span><span class="sxs-lookup"><span data-stu-id="59f3a-121">The [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method (asynchronous analysis), which works best for:</span></span>

    -   <span data-ttu-id="59f3a-122">Eine beliebige Menge an frei Hand Eingaben.</span><span class="sxs-lookup"><span data-stu-id="59f3a-122">Any amount of ink.</span></span>
    -   <span data-ttu-id="59f3a-123">Bei Verwendung eines Zeit Geber-Pulas ungefähr alle 600 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="59f3a-123">When utilized with a timer pulsing approximately every 600 milliseconds.</span></span>

> [!Note]  
> <span data-ttu-id="59f3a-124">600 Millisekunden ist die aktuelle Empfehlung. diese zeitliche Steuerung unterliegt jedoch Änderungen, die noch weiter getestet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="59f3a-124">600 milliseconds is the current recommendation, but this timing is subject to change pending further testing.</span></span>

 

<span data-ttu-id="59f3a-125">Um den [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) -Vorgang zu verwenden, verwaltet das [**InkCollector**](inkcollector-class.md) -Objekt (oder ähnliche Objekte oder Steuerelemente wie das [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md)oder [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) in Windows Presentation Foundation) die Erfassung und das Rendering der Hand Striche.</span><span class="sxs-lookup"><span data-stu-id="59f3a-125">To use the [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) operation, the [**InkCollector**](inkcollector-class.md) object (or similar objects or controls such as the [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md), or [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) in Windows Presentation Foundation) manages the collection and rendering of the ink strokes.</span></span> <span data-ttu-id="59f3a-126">Wenn **InkCollector** mit den frei Hand Analyse-APIs gekoppelt ist, können Anwendungen die Erkennungsergebnisse aktualisieren, indem Sie den [**InkAnalyzer**](inkanalyzer.md) über jeden neuen, der Anwendung hinzugefügten Strich informieren.</span><span class="sxs-lookup"><span data-stu-id="59f3a-126">If the **InkCollector** is paired with the ink analysis APIs, applications can keep the recognition results updated by informing the [**InkAnalyzer**](inkanalyzer.md) about each new stroke added to the application.</span></span> <span data-ttu-id="59f3a-127">Dadurch kann der **InkAnalyzer** die Striche inkrementell und in einem Hintergrund Thread erkennen.</span><span class="sxs-lookup"><span data-stu-id="59f3a-127">This allows for the **InkAnalyzer** to recognize the strokes incrementally and on a background thread.</span></span>

<span data-ttu-id="59f3a-128">Um inkrementelle Hintergrundanalysen durchzuführen, müssen Anwendungen drei Schritte implementieren (für verwalteten Code angezeigt):</span><span class="sxs-lookup"><span data-stu-id="59f3a-128">To accomplish incremental background analysis, applications need to implement three steps (shown for managed code):</span></span>

1. <span data-ttu-id="59f3a-129">Fügen Sie den Strich immer dann dem [**InkAnalyzer**](inkanalyzer.md) hinzu, wenn das [**Stroke**](inkoverlay-stroke.md) -Ereignis des [**InkOverlay**](inkoverlay-class.md) -Objekts ausgelöst wird:</span><span class="sxs-lookup"><span data-stu-id="59f3a-129">Add the stroke to the [**InkAnalyzer**](inkanalyzer.md) whenever the [**InkOverlay**](inkoverlay-class.md) object's [**Stroke**](inkoverlay-stroke.md) event is raised:</span></span>


```C++
/// Event Handler from InkOverlay's Stroke event
/// This event is fired when a new stroke is drawn. 
/// In this case, it is necessary to update the ink analyzer's 
/// Strokes collection. The event is fired even when the eraser 
/// stroke is created.
/// The event handler must filter out the eraser strokes.
/// <param name="sender">The control that raised the event.</param>
/// <param name="e">The event arguments.</param>
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
{
        // Add the new stroke to the InkAnalyzer's stroke collection
        theInkAnalyzer.AddStroke(e.Stroke);
        this.Refresh();
}
```



2. <span data-ttu-id="59f3a-130">Aufrufen von [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) -Vorgängen in einem festgelegten Intervall.</span><span class="sxs-lookup"><span data-stu-id="59f3a-130">Invoke the [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) operations at a set interval.</span></span>


```C++
//Setup a timer tick handler
private System.Windows.Forms.Timer analysisTimer;
analysisTimer = new Timer();
analysisTimer.Tick += new System.EventHandler(this.analysisTimer_Tick);

// The timer is enabled and set to tick every 600 milliseconds.
analysisTimer.Enabled = true;
analysisTimer.Interval = 600;
// ...
//The background analysis operation is invoked with every tick
private void analysisTimer_Tick(object sender, System.EventArgs e)
{
    theInkAnalyzer.BackgroundAnalyze();
}
```



> [!Note]  
> <span data-ttu-id="59f3a-131">Hinweis Anwendungen sollten nicht einfach den Hintergrundanalyse Vorgang nach jedem neuen Strich aufrufen.</span><span class="sxs-lookup"><span data-stu-id="59f3a-131">Note Applications should not simply invoke the background analysis operation after every new stroke.</span></span> <span data-ttu-id="59f3a-132">Dies schlägt fehl (gibt den Wert **false** zurück), wenn bereits ein Hintergrund Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59f3a-132">This will fail (returning a value of **false**) if a background operation is already running.</span></span> <span data-ttu-id="59f3a-133">Der Grund für dieses Verhalten besteht darin, die Anzahl der erforderlichen Hintergrundthreads und Abstimmungs Vorgänge einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="59f3a-133">The reason for this behavior is to limit the number of background threads and reconciliation operations required.</span></span>

 

3. <span data-ttu-id="59f3a-134">Lauschen Sie auf das [resultsupveralteten](/previous-versions/ms567607(v=vs.100)) -Ereignis (verwalteter Code) oder das [**Ergebnis**](-ianalysisevents-results.md) Ereignis (C++-Code), um zu bestimmen, wann der Hintergrundprozess abgeschlossen wurde:</span><span class="sxs-lookup"><span data-stu-id="59f3a-134">Listen for the [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) event (managed code) or [**Results**](-ianalysisevents-results.md) event (C++ code) to determine when the background process has finished:</span></span>


```C++
// ...
theInkAnalyzer.Results += new ResultsEventHandler(ia_Results);
// ...

private void ia_Results(object sender, ResultsEventArgs e)
{
    String myResults = e.InkAnalyzer.GetRecognizedString();
    MessageBox.Show(myResults);
}
```



<span data-ttu-id="59f3a-135">Nun, da die Verarbeitung der frei Hand Eingaben in einem Hintergrund Thread erfolgt, kann die Anwendung Änderungen an der frei Hand Eingabe annehmen, während der Hintergrund Vorgang funktioniert.</span><span class="sxs-lookup"><span data-stu-id="59f3a-135">Now that the processing of the ink is being done on a background thread, the application has the ability to accept changes to the ink while the background operation is working.</span></span> <span data-ttu-id="59f3a-136">Wenn wir einen synchronen Thread verwenden, ist dies nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="59f3a-136">If we use a synchronous thread this is not possible.</span></span> <span data-ttu-id="59f3a-137">Die Arbeit wird im UI-Thread ausgeführt, was die Fähigkeit zum vornehmen von Änderungen blockiert.</span><span class="sxs-lookup"><span data-stu-id="59f3a-137">The work executes on the UI thread, blocking the ability to make changes.</span></span> <span data-ttu-id="59f3a-138">Zu den Änderungen gehören das Hinzufügen von mehr Freihand zum Dokument, das Löschen von frei Hand Eingaben oder das Transformieren der Position oder Darstellung der vorhandenen frei Hand Eingabe</span><span class="sxs-lookup"><span data-stu-id="59f3a-138">Changes include adding more ink to the document, deleting ink, or transforming the location or appearance of the existing ink.</span></span> <span data-ttu-id="59f3a-139">Bei Änderungen, die während des Hintergrund Vorgangs auftreten, werden die Ergebnisse möglicherweise ungültig.</span><span class="sxs-lookup"><span data-stu-id="59f3a-139">Changes that occur during the background operation may in fact invalidate the results.</span></span> <span data-ttu-id="59f3a-140">Wenn Sie z. b. einen Strich aus einem Wort löschen, wird der Erkennungswert dieses Worts geändert.</span><span class="sxs-lookup"><span data-stu-id="59f3a-140">For example, deleting a stroke from a word changes the recognition value of that word.</span></span> <span data-ttu-id="59f3a-141">Die [**InkAnalyzer**](inkanalyzer.md) -API verfügt über einen integrierten Abstimmungsprozess, der automatisch bestimmt, welche Teile des Hintergrund Vorgangs ungültig werden, wenn das Ergebnis der frei Hand Eingaben während der Analyse geändert wird.</span><span class="sxs-lookup"><span data-stu-id="59f3a-141">The [**InkAnalyzer**](inkanalyzer.md) API has a built-in reconciliation process that automatically determines what parts of the background operation become invalid as the result of the ink changing while analyzing.</span></span>

<span data-ttu-id="59f3a-142">Der automatische Abstimmungs Vorgang wird aufgrund von drei Faktoren durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="59f3a-142">The automatic reconciliation process is accomplished because of three factors:</span></span>

1.  <span data-ttu-id="59f3a-143">Die [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="59f3a-143">The [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property.</span></span>

    -   <span data-ttu-id="59f3a-144">Jedes Mal, wenn die Anwendung ([**AddStroke**](iinkanalyzer-addstroke.md) [**-Methode)**](iinkanalyzer-removestroke.md) einen Strich zum oder aus dem [**InkAnalyzer**](inkanalyzer.md)hinzufügt, wird der physische Speicherort des Strichs aufgezeichnet, und beim nächsten Aufrufen eines Analyse Vorgangs wird vom **InkAnalyzer** sichergestellt, dass der Strich bzw. der von diesem Strich belegte Bereich analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="59f3a-144">Each time the application adds ([**AddStroke**](iinkanalyzer-addstroke.md) method) or removes ([**RemoveStroke**](iinkanalyzer-removestroke.md) method) a stroke to or from the [**InkAnalyzer**](inkanalyzer.md), the physical location of the stroke is captured and the next time an analysis operation is invoked, the **InkAnalyzer** ensures that stroke, or the area occupied by that stroke, is analyzed.</span></span>
    -   <span data-ttu-id="59f3a-145">Wenn die Anwendung vorhandene frei Hand Eingaben ändert, den Speicherort ändert oder andere Zeichnungs Attribute der frei Hand Eingabe ändert, kann der Speicherort der Änderung (die Begrenzungen der frei Hand Eingabe) der [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) -Eigenschaft des [**InkAnalyzer**](inkanalyzer.md)-Objekts hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="59f3a-145">Whenever the application modifies existing ink, changes the location, or changes other drawing attributes of the ink, the location of the change (the bounds of the ink) can be added to the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property of the [**InkAnalyzer**](inkanalyzer.md).</span></span> <span data-ttu-id="59f3a-146">Dadurch wird sichergestellt, dass die Bereiche beim nächsten Start des Analyse Vorgangs auf richtige Ergebnisse geprüft werden.</span><span class="sxs-lookup"><span data-stu-id="59f3a-146">This ensures that the next time the application starts the analysis operation those areas are checked for correct results.</span></span>
    -   <span data-ttu-id="59f3a-147">Daher verfolgt die [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) -Eigenschaft zwischen Analyse Ausführungen, welche Bereiche des Dokuments und welche Striche geprüft werden müssen, um die korrekte Handschrift Analyse und die Erkennungsergebnisse zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="59f3a-147">Thus, the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property keeps track, between analysis runs, of what areas of the document and-in turn-which strokes need to be checked for correct ink analysis and recognition results.</span></span>

2.  <span data-ttu-id="59f3a-148">Eingeschränkte Analyse.</span><span class="sxs-lookup"><span data-stu-id="59f3a-148">Limited analysis.</span></span>

    -   <span data-ttu-id="59f3a-149">Jedes Mal, wenn die Anwendung den Analyse Vorgang aufruft, identifiziert die [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) -Eigenschaft, welche Striche analysiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="59f3a-149">Each time the application invokes the analysis operation, the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property identifies which strokes need to be analyzed.</span></span> <span data-ttu-id="59f3a-150">Dadurch kann der Vorgang durch den Analyse Vorgang auf die geänderten Bereiche beschränkt werden, und alle anderen Regionen werden ignoriert, und es wird der Zeitaufwand für die erneute Analyse von frei Hand Eingaben optimiert.</span><span class="sxs-lookup"><span data-stu-id="59f3a-150">This allows the analysis operation to limit the operation to only the dirty regions and ignore all other regions, optimizing the amount of time spent re-analyzing ink.</span></span>
    -   <span data-ttu-id="59f3a-151">Der [**InkAnalyzer**](inkanalyzer.md) ignoriert nicht vollständig alle anderen Bereiche auf der Seite, sondern kann stattdessen benachbarte Bereiche überprüfen, um festzustellen, ob sich die Änderungen, die in der geänderten Region vorgenommen wurden, auf diese benachbarten Regionen auswirken.</span><span class="sxs-lookup"><span data-stu-id="59f3a-151">The [**InkAnalyzer**](inkanalyzer.md) does not completely ignore all other regions on the page, but instead may examine neighboring areas to determine if the changes made in the dirty region affect those neighboring regions.</span></span> <span data-ttu-id="59f3a-152">Beispielsweise klassifiziert der Analyzer "is" im folgenden Ink-Beispiel als einzelnen **InkWord** -Typ der [**ContextNode**](icontextnode.md) -Klasse:</span><span class="sxs-lookup"><span data-stu-id="59f3a-152">For example, the analyzer classifies "Is", in the following ink sample, as a single **InkWord** type of the [**ContextNode**](icontextnode.md) class:</span></span>

!["ist" Hand geschrieben](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

<span data-ttu-id="59f3a-154">Das Löschen der "s" führt zu einem geänderten Bereich (markiert mit einem roten Feld).</span><span class="sxs-lookup"><span data-stu-id="59f3a-154">Deleting the "s" results in a dirty region (marked with a red box).</span></span>

![Handgeschriebenes "i"](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

<span data-ttu-id="59f3a-156">Nach der Analyse ändert der Analyzer die Klassifizierung für das "I" in einen **inkzeichentyp** , auch wenn er sich außerhalb des geänderten Bereichs befindet, denn ohne den unterstützenden "s"-Strich hat der Ink Analyzer eine 50/50-Wahrscheinlichkeit, dass die frei Hand Eingaben als Zeichen oder Wort klassifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="59f3a-156">After analysis, the analyzer changes the classification for the "I" to an **InkDrawing** type, even though it is outside of the dirty region, because without the supporting "s" stroke the ink analyzer has a 50/50 chance of the ink being classified as a drawing or a word.</span></span>

-   <span data-ttu-id="59f3a-157">Intern zwischen gespeicherter Zustand.</span><span class="sxs-lookup"><span data-stu-id="59f3a-157">Internally cached state.</span></span>

    -   <span data-ttu-id="59f3a-158">Wenn eine Anwendung einen Hintergrundanalyse Vorgang aufruft, speichert der [**InkAnalyzer**](inkanalyzer.md) eine Momentaufnahme der aufgeschnittenen Daten zwischen.</span><span class="sxs-lookup"><span data-stu-id="59f3a-158">When an application invokes a background analysis operation the [**InkAnalyzer**](inkanalyzer.md) caches a snapshot of the pruned data.</span></span> <span data-ttu-id="59f3a-159">Wenn Sie eine Momentaufnahme erstellen, kann der **InkAnalyzer** entweder daran arbeiten, die Daten unabhängig von den Daten zu analysieren, die von der Anwendung verwendet werden, oder die Momentaufnahme als Vergleichspunkt verwenden, um zu bestimmen, welche Änderungen von der Anwendung während der Hintergrundanalyse vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="59f3a-159">By taking a snapshot the **InkAnalyzer** can either work on analyzing the data independently of the data being used by the application, or use the snapshot as the comparison point to determine what changes were made by the application while background analyzing.</span></span>
    -   <span data-ttu-id="59f3a-160">Das Zwischenspeichern des Zustands und das Vergleichen von Änderungen ist besser als das Beibehalten einer Liste aller Änderungen, die aus einem primären Grund aufgetreten sind: Daten Proxy.</span><span class="sxs-lookup"><span data-stu-id="59f3a-160">Caching the state and comparing changes is better than keeping a list of all changes that occurred for one primary reason: data proxy.</span></span> <span data-ttu-id="59f3a-161">Dabei handelt es sich um ein erweitertes Szenario, das weiter unten in diesem Dokument beschrieben wird. Es umfasst aber auch die Anwendung, die den [**InkAnalyzer**](inkanalyzer.md) nur mit den aktuellen Freihand-und nicht-frei Hand Daten aktualisiert, bevor der aufgerufene Analyse Vorgang und die Ergebnisse eines Analyse Vorgangs verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="59f3a-161">This is an advanced scenario described later in this document, but it involves the application updating the [**InkAnalyzer**](inkanalyzer.md) with only the current ink and non-ink data prior to the invoked analysis operation and prior to processing the results of an analysis operation.</span></span>

## <a name="simple-ink-analysis"></a><span data-ttu-id="59f3a-162">Einfache Handschrift Analyse</span><span class="sxs-lookup"><span data-stu-id="59f3a-162">Simple Ink Analysis</span></span>

<span data-ttu-id="59f3a-163">In den beiden vorherigen Szenarien (einfache Erkennung und inkrementelle Erkennung) wird beschrieben, wie auf Erkennungswerte zugegriffen wird</span><span class="sxs-lookup"><span data-stu-id="59f3a-163">The previous two scenarios (simple recognition and incremental recognition) outline how to access recognition values but do not mention how to access the ink analysis or classification results.</span></span> <span data-ttu-id="59f3a-164">Die Standardkonfiguration von [**InkAnalyzer**](inkanalyzer.md)führt sowohl frei Hand Analysealgorithmen als auch Erkennungsalgorithmen aus.</span><span class="sxs-lookup"><span data-stu-id="59f3a-164">The default configuration of the [**InkAnalyzer**](inkanalyzer.md), runs both ink analysis algorithms and recognition algorithms.</span></span> <span data-ttu-id="59f3a-165">Diese Konfiguration ergibt die genauesten Ergebnisse, da die beiden Technologien zusammenarbeiten, um die Genauigkeit zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="59f3a-165">This configuration yields the most accurate results, because the two technologies work together to increase accuracy.</span></span> <span data-ttu-id="59f3a-166">Das heißt, die frei Hand Analyse-Engines helfen dabei, die Zeichnung von der Schreibweise zu trennen und das Schreiben in eine horizontale Ebene zu normalisieren. Dies ist die optimale Eingabe Ebene für die Erkennungs-Engines.</span><span class="sxs-lookup"><span data-stu-id="59f3a-166">That is, the ink analysis engines help to separate the drawing from the writing and normalize angled writing into a horizontal plane, which is the optimum input plane for the recognition engines.</span></span>

<span data-ttu-id="59f3a-167">Für den Zugriff auf die Ergebnisse der frei Hand Analyse verwendet Ihre Anwendung die Methoden " [**analysieren**](iinkanalyzer-analyze.md) " oder " [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) " genau wie in den vorherigen beiden Erkennungs Szenarien beschrieben.</span><span class="sxs-lookup"><span data-stu-id="59f3a-167">To access the ink analysis results, your application uses the [**Analyze**](iinkanalyzer-analyze.md) or [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) methods exactly as described in the previous two recognition scenarios.</span></span> <span data-ttu-id="59f3a-168">Nichts ändert sich, weil die Handschrift Analyse und Erkennungsalgorithmen bereits ausgeführt werden, wenn diese Methoden aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="59f3a-168">Nothing changes because the ink analysis and recognition algorithms are already being run when those methods are called.</span></span> <span data-ttu-id="59f3a-169">Allerdings ist der Zugriff auf die Ergebnisse komplizierter als das Lesen des Werts einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="59f3a-169">However, accessing the results is more complicated than reading the value of a string.</span></span> <span data-ttu-id="59f3a-170">Im folgenden Codebeispiel werden z. b. die Gruppierung und die Speicherorte aller **InkWord** -Segmente und **InkDrawing** -Segmente veranschaulicht, indem ein Rechteck um die Gruppe der Striche gerendert wird, aus denen die Klassifizierung besteht.</span><span class="sxs-lookup"><span data-stu-id="59f3a-170">As an example, the following code sample shows the grouping and locations of all the **InkWord** segments and **InkDrawing** segments by rendering a rectangle around the group of strokes that make up the classification.</span></span>

<span data-ttu-id="59f3a-171">Dieses Beispiel verwendet einfach das **Paint** -Ereignis des Formulars, um Farbige Rechtecke um die Wörter oder Zeichnungen zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="59f3a-171">This example simply uses the form's **Paint** event to render colored rectangles around the words or drawings.</span></span> <span data-ttu-id="59f3a-172">Die [**findnodesoft ype**](iinkanalyzer-findnodesoftype.md) -Methode gibt eine Auflistung von-Objekten zurück, die nur vorhanden ist, wenn der Analyse Vorgang ausgeführt wurde und die Ergebnisse Klassifizierungen mit dem angegebenen [**ContextNode**](icontextnode.md) -Typ enthalten.</span><span class="sxs-lookup"><span data-stu-id="59f3a-172">The [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method returns a collection of objects that exists only if the analysis operation has been executed and the results contain classifications with the specified [**ContextNode**](icontextnode.md) type.</span></span> <span data-ttu-id="59f3a-173">Wenn kein **ContextNode** des gewünschten Typs im Dokument vorhanden ist, werden die Schritte zum Zeichnen der Rechtecke übersprungen.</span><span class="sxs-lookup"><span data-stu-id="59f3a-173">If no **ContextNode** of the desired type exists in the document, the steps to draw the rectangles are skipped.</span></span>

<span data-ttu-id="59f3a-174">Jedes Objekt, das von der [**findnodesoft ype**](iinkanalyzer-findnodesoftype.md) -Methode zurückgegeben wird, verfügt über Eigenschaften, die sich auf diese Art von Klassifizierung beziehen.</span><span class="sxs-lookup"><span data-stu-id="59f3a-174">Each object returned from the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method will have properties that relate to that kind of classification.</span></span> <span data-ttu-id="59f3a-175">Beispielsweise verweist der **InkWordNode** auf alle Striche, die ein einzelnes Wort im Dokument bilden, und verweist auf die erkannte Zeichenfolge für dieses Wort.</span><span class="sxs-lookup"><span data-stu-id="59f3a-175">For example the **InkWordNode** references all the strokes that make up a single word in the document and reference the recognized string for that word.</span></span> <span data-ttu-id="59f3a-176">**InkDrawingNode** verweist auf alle Striche, die das einzelne zeichnen im Dokument bilden, und verweist auf den Namen der Form für diese Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="59f3a-176">The **InkDrawingNode** references all the strokes that make up the single drawing in the document and reference the shape name for that drawing.</span></span>

<span data-ttu-id="59f3a-177">Die [**findnodesoft ype**](iinkanalyzer-findnodesoftype.md) -Methode ähnelt der [**DivisionResult:: ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) -Methode, die Auflistungen von [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) entweder von Schreib-oder Zeichnungs Typen zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="59f3a-177">The [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method is very similar to the [**DivisionResult::ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) method that returned collections of [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) of either writing or drawing types.</span></span>


```C++
private void Form1_Paint(object sender, PaintEventArgs e)
{
    //Setup the pen to draw
    using(Pen penBox = new Pen(Color.Red, 1))
    {
        // Find all the InkWord ContextNodes in the results
        ContextNodeCollection InkWordNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkWord);
        // For each InkWord node found, cast the ContextNode to a type specific
        // "InkWordNode" to easily access the rotated bounding box property.
        foreach (ContextNode InkWord in InkWordNodes)
        {
            //Draw the rotated bounding box.
            e.Graphics.DrawPolygon(penBox,
                    ((InkWordNode)InkWord).GetRotatedBoundingBox());
        }

        // Find all the InkDrawing ContextNodes in the results
        ContextNodeBaseCollection InkDrawingNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkDrawing);

        penBox.Color = Color.Green;

        // For each InkDrawing node found, access the node's location property to
        // draw a rectangle around the drawing.
        foreach (ContextNode InkDrawing in InkDrawingNodes)
        {
            e.Graphics.DrawRectangle(penBox, InkDrawing.Location.GetBounds());
        }
    }
}
```



<span data-ttu-id="59f3a-178">Um das vorherige Codebeispiel in die Perspektive zu versetzen, betrachten Sie das folgende Ink-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="59f3a-178">To put the previous code example into perspective, consider the following ink sample:</span></span>

![Ink Sample "This is some Ink".](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

<span data-ttu-id="59f3a-181">Wenn Sie die [**findnodesoft ype**](iinkanalyzer-findnodesoftype.md) -Methode aufzurufen und das statische Feld für **InkWord** übergeben, gibt die Analyse eine Auflistung von vier **InkWordNode** -Objekten zurück:</span><span class="sxs-lookup"><span data-stu-id="59f3a-181">If you call the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method and pass in the static field for **InkWord**, the analyzer returns a collection of four **InkWordNode** objects:</span></span>

![Ausgabe des Analyzers "This is some Ink"](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

<span data-ttu-id="59f3a-183">Wenn Sie die [**findnodesoft ype**](iinkanalyzer-findnodesoftype.md) -Methode aufzurufen und das statische Feld für **InkDrawing** übergeben, gibt die Analyse eine Auflistung von einem **InkDrawingNode** -Objekt zurück:</span><span class="sxs-lookup"><span data-stu-id="59f3a-183">If you call the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method and pass in the static field for **InkDrawing**, the analyzer returns a collection of one **InkDrawingNode** object:</span></span>

![Bild, das "Oval" anzeigt, das Ergebnis des InkDrawing-Analyzers](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

<span data-ttu-id="59f3a-185">Nachdem das **Paint** -Ereignis ausgelöst wurde, rendert der Beispielcode Rechtecke um jedes der-Objekte:</span><span class="sxs-lookup"><span data-stu-id="59f3a-185">After the **Paint** event has fired, the sample code renders rectangles around each of the objects:</span></span>

![ursprüngliches zeichnen mit Rechtecke um das Objekt und Wörter gerendert](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

<span data-ttu-id="59f3a-187">In diesem Beispiel wird nur die [**findnodesoft ype**](iinkanalyzer-findnodesoftype.md) -Methode behandelt, aber da die frei Hand Analyse-Engines einen umfassenderen Satz von Freihand Typen erkennen können, entspricht die-Methode auch allen Typen von Knoten, die von den frei Hand Analysemodulen (z. b. Zeilen, Absätzen und anderen Strukturen) erkennbar sind.</span><span class="sxs-lookup"><span data-stu-id="59f3a-187">This example only touches on the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method, but because the ink analysis engines can detect a richer set of ink types, the method also correspond to all types of nodes detectable by the ink analysis engines (such as lines, paragraphs, and other structures).</span></span>

## <a name="using-ink-analysis-with-point-erase"></a><span data-ttu-id="59f3a-188">Verwenden der Ink-Analyse mit Punkt Löschung</span><span class="sxs-lookup"><span data-stu-id="59f3a-188">Using Ink Analysis with Point Erase</span></span>

<span data-ttu-id="59f3a-189">Die Anwendung muss Anpassungen bei der Aktualisierung von Strichen durchführen, um eine gute Leistung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="59f3a-189">Your application needs to make adjustments in the way it updates strokes when performing point erase to ensure good performance.</span></span> <span data-ttu-id="59f3a-190">Ersetzen Sie zunächst auf der Anwendungsebene den Tablettstiftpunkt des vorhandenen Strichs durch den Tablettstiftpunkt des neuen Strichs, und aktualisieren Sie dann [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) auf diesem Strich, und aktualisieren Sie den geänderten Bereich mit den Begrenzungen des Strichs.</span><span class="sxs-lookup"><span data-stu-id="59f3a-190">Firstly, at the application layer, replace the stylus point of the existing Stroke with the stylus point of the new stroke, then call [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) on that stroke and update the dirty region with the stroke's bounds.</span></span> <span data-ttu-id="59f3a-191">Dies bewirkt, dass der [**InkAnalyzer**](inkanalyzer.md) die aktualisierten hubdaten abruft, wenn die nächste Runde der Hintergrundanalyse beginnt.</span><span class="sxs-lookup"><span data-stu-id="59f3a-191">This will cause the [**InkAnalyzer**](inkanalyzer.md) to fetch the updated stroke data when the next round of background analysis starts.</span></span> <span data-ttu-id="59f3a-192">Dieses Verfahren wird im folgenden Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="59f3a-192">This technique is demonstrated in the following example.</span></span>


```C++
using System;
using System.Diagnostics;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;

class PointEraseAnalysisSample : Application
{
  InkAnalyzer _analyzer;
  InkCanvas _canvas;
  bool _isPointErasing = false;
  bool _strokesManipulated = false;

  protected override void OnStartup(StartupEventArgs e)
  {
      base.OnStartup(e);
      Window win = new Window();

      _canvas = new InkCanvas();
      _canvas.Background = new LinearGradientBrush(Colors.Yellow, Colors.LightYellow, 60d);
      _canvas.EditingModeInverted = InkCanvasEditingMode.EraseByPoint;
      _canvas.Strokes.StrokesChanged += new StrokeCollectionChangedEventHandler(Strokes_StrokesChanged);
      _canvas.AddHandler(InkCanvas.MouseUpEvent, new MouseButtonEventHandler(_canvas_MouseUp), true);

      _analyzer = new InkAnalyzer(this.Dispatcher);
      _analyzer.ResultsUpdated += new ResultsUpdatedEventHandler(_analyzer_ResultsUpdated);

      win.Content = _canvas;
      win.Show();
  }

  void _analyzer_ResultsUpdated(object sender, ResultsUpdatedEventArgs e)
  {
      if (!_analyzer.DirtyRegion.IsEmpty)
      {
          _analyzer.BackgroundAnalyze();
          return;
      }

      Console.WriteLine(_analyzer.GetRecognizedString());
  }

  void _canvas_MouseUp(object sender, MouseButtonEventArgs e)
  {
      if (_isPointErasing)
      {
          _isPointErasing = false;
          _analyzer.BackgroundAnalyze();
      }
  }

  void Strokes_StrokesChanged(object sender, StrokeCollectionChangedEventArgs e)
  {
      if (_strokesManipulated)
      {
          // ignore StrokesChanged if we changed them ourselves
          _strokesManipulated = false;
          return;
      }

      if (_canvas.ActiveEditingMode == InkCanvasEditingMode.EraseByPoint &&
          e.Added.Count == 1 && e.Removed.Count == 1)
      {
          // set flag so we call BackgroundAnalyze in MouseUp
          _isPointErasing = true;

          // set flag so we ignore the next StrokesChanged
          _strokesManipulated = true;

          // replace the stylus points on the removed stroke with the added stroke
          e.Removed[0].StylusPoints = e.Added[0].StylusPoints;
          
          // force IA to update the stroke data for the removed stroke
          _analyzer.ClearStrokeData(e.Removed[0]);

          // replace the added stroke with the updated removed stroke back into InkCanvas
          _canvas.Strokes.Replace(e.Added[0], new StrokeCollection(new Stroke[] {e.Removed[0]})); 
          
          return;
      }

      if (e.Added.Count > 0)
      {
          _analyzer.AddStrokes(e.Added);
      }

      if (e.Removed.Count > 0)
      {
          _analyzer.RemoveStrokes(e.Removed);
      }

      _analyzer.BackgroundAnalyze();
  }

  [STAThread]
  static void Main(string[] args)
  {
      new PointEraseAnalysisSample().Run();
  }
}
```



## <a name="related-topics"></a><span data-ttu-id="59f3a-193">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59f3a-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59f3a-194">Übersicht über die Link Analyse</span><span class="sxs-lookup"><span data-stu-id="59f3a-194">Ink Analysis Overview</span></span>](ink-analysis-overview.md)
</dt> <dt>

[<span data-ttu-id="59f3a-195">Verwendung der frei Hand Analyse-API</span><span class="sxs-lookup"><span data-stu-id="59f3a-195">Ink Analysis API Usage</span></span>](ink-analysis-api-usage.md)
</dt> </dl>

 

 
