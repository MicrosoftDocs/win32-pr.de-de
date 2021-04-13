---
description: Dieses Programm veranschaulicht, wie frei Hand Eingaben in eine andere Anwendung kopiert und eingefügt werden. Außerdem kann der Benutzer eine Auswahl von Strichen kopieren und das Ergebnis in das vorhandene Ink-Objekt einfügen.
ms.assetid: a0c42f1c-543d-44f8-83d9-fe810de410ff
title: Beispiel für frei Hand Ablage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95c5da0bc0ba9a7e3a1b4e1a5c52784f10fb2023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525970"
---
# <a name="ink-clipboard-sample"></a><span data-ttu-id="3762f-104">Beispiel für frei Hand Ablage</span><span class="sxs-lookup"><span data-stu-id="3762f-104">Ink Clipboard Sample</span></span>

<span data-ttu-id="3762f-105">Dieses Programm veranschaulicht, wie frei Hand Eingaben in eine andere Anwendung kopiert und eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3762f-105">This program demonstrates how to copy and paste ink into another application.</span></span> <span data-ttu-id="3762f-106">Außerdem kann der Benutzer eine Auswahl von Strichen kopieren und das Ergebnis in das vorhandene Ink-Objekt einfügen.</span><span class="sxs-lookup"><span data-stu-id="3762f-106">It also enables the user to copy a selection of strokes and paste the result into the existing ink object.</span></span>

<span data-ttu-id="3762f-107">Die folgenden Zwischenablage Modi sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="3762f-107">The following clipboard modes are available:</span></span>

-   <span data-ttu-id="3762f-108">Ink-serialisiertes Format (ISF)</span><span class="sxs-lookup"><span data-stu-id="3762f-108">Ink serialized format (ISF)</span></span>
-   <span data-ttu-id="3762f-109">Metadatei</span><span class="sxs-lookup"><span data-stu-id="3762f-109">Metafile</span></span>
-   <span data-ttu-id="3762f-110">Erweiterte Metadatei (Enhanced Metafile, EMF)</span><span class="sxs-lookup"><span data-stu-id="3762f-110">Enhanced Metafile (EMF)</span></span>
-   <span data-ttu-id="3762f-111">Bitmap</span><span class="sxs-lookup"><span data-stu-id="3762f-111">Bitmap</span></span>
-   <span data-ttu-id="3762f-112">Text Freihand</span><span class="sxs-lookup"><span data-stu-id="3762f-112">Text Ink</span></span>
-   <span data-ttu-id="3762f-113">Skizzen frei</span><span class="sxs-lookup"><span data-stu-id="3762f-113">Sketch Ink</span></span>

<span data-ttu-id="3762f-114">Text Freihand-und Skizzen frei Hand Eingaben sind zwei Arten von frei Hand Steuerelementen, die als Text bzw. gezeichnet werden</span><span class="sxs-lookup"><span data-stu-id="3762f-114">Text ink and sketch ink are two types of ink controls used as text or drawing respectively.</span></span> <span data-ttu-id="3762f-115">Es ist möglich, ISF, Text Freihand und Skizzen Freihand in vorhandene Freihand einzufügen.</span><span class="sxs-lookup"><span data-stu-id="3762f-115">It is possible to paste ISF, text ink, and sketch ink into existing ink.</span></span>

<span data-ttu-id="3762f-116">Neben der Zwischenablage veranschaulicht dieses Beispiel auch, wie Striche mit dem Lassopfad-Tool ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="3762f-116">In addition to the clipboard, this sample also illustrates how to select strokes with the lasso tool.</span></span> <span data-ttu-id="3762f-117">Der Benutzer kann ausgewählte Striche verschieben und seine Zeichnungs Attribute ändern.</span><span class="sxs-lookup"><span data-stu-id="3762f-117">The user can move selected strokes and modify their drawing attributes.</span></span> <span data-ttu-id="3762f-118">Diese Funktion ist eine Teilmenge der Auswahl Funktionen, die bereits vom Handschrift Steuerelement bereitgestellt werden. Sie wird hier zur Veranschaulichung implementiert.</span><span class="sxs-lookup"><span data-stu-id="3762f-118">This functionality is a subset of the selection functionality already provided by the ink overlay control; it is implemented here for illustrative purposes.</span></span>

<span data-ttu-id="3762f-119">In diesem Beispiel werden die folgenden Funktionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="3762f-119">The following features are used in this sample:</span></span>

-   <span data-ttu-id="3762f-120">Das [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3762f-120">The [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>
-   <span data-ttu-id="3762f-121">Unterstützung für frei Hand Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="3762f-121">Ink clipboard support.</span></span>
-   <span data-ttu-id="3762f-122">Die Verwendung von Lassopfad mit der [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3762f-122">The use of the lasso with the [Microsoft.Ink.Ink.HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method.</span></span>

<span data-ttu-id="3762f-123">Dieses Beispiel veranschaulicht das Rendern von frei Hand Eingaben, das Kopieren der frei Hand Eingaben und das anschließende Einfügen der frei Hand Eingaben in eine andere Anwendung wie Microsoft Paint.</span><span class="sxs-lookup"><span data-stu-id="3762f-123">This sample demonstrates rendering ink, copying that ink, and then pasting the ink into another application such as Microsoft Paint.</span></span>

## <a name="collecting-ink-and-setting-up-the-form"></a><span data-ttu-id="3762f-124">Sammeln von frei Hand Eingaben und Einrichten des Formulars</span><span class="sxs-lookup"><span data-stu-id="3762f-124">Collecting Ink and Setting Up the Form</span></span>

<span data-ttu-id="3762f-125">Verweisen Sie zunächst auf die Tablet PC Automation-Schnittstellen, die mit dem Microsoft Windows <entity type="reg"/> XP Tablet PC Edition Software Development Kit (SDK) installiert werden.</span><span class="sxs-lookup"><span data-stu-id="3762f-125">First, reference the Tablet PC Automation interfaces, which are installed with the Microsoft Windows<entity type="reg"/> XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="3762f-126">Im nächsten Schritt deklariert das Formular einige Konstanten und Felder, die später in diesem Beispiel notiert werden.</span><span class="sxs-lookup"><span data-stu-id="3762f-126">Next, the form declares some constants and fields that are noted later in this sample.</span></span>


```C++
// Declare constant for the size of the border around selected strokes
private const int SelectedInkWidthIncrease = 105;

// Declare constant for the size of a lasso point
private const int DotSize = 6;

// Declare constant for the spacing between lasso points
private const int DotSpacing = 7;

// Declare constant for the selection rectangle padding
private const int SelectionRectBuffer = 8;

// Declare constant for the lasso hit test percent (specifies how much
// of the stoke must fall within the lasso in order to be selected).
private const float LassoPercent = 50;
...
// Declare the InkCollector object
private InkCollector myInkCollector = null;

// The points in the selection lasso
private ArrayList lassoPoints = null;

// The array of rectangle selection handles
private PictureBox[] selectionHandles;

// The rectangle that bounds the selected strokes
private Rectangle selectionRect = Rectangle.Empty;

// The strokes that have been selected by the lasso
private Strokes selectedStrokes = null;
...
// Declare the colors used in the selection lasso
private Color dotEdgeColor = Color.White;
private Color dotColor = SystemColors.Highlight;
private Color connectorColor = Color.Black;

// Declare the pens used to draw the selection lasso
private Pen connectorPen = null;
private Pen dotEdgePen = null;
private Pen dotPen = null;
```



<span data-ttu-id="3762f-127">Schließlich wird das Formular im [Lade](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) Ereignishandler des Formulars initialisiert, ein [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt für das Formular erstellt und der frei Hand Sammler aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3762f-127">Finally, in the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler, the form is initialized, an [InkCollector](/previous-versions/ms583683(v=vs.100)) object for the form is created and the ink collector is enabled.</span></span>


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a><span data-ttu-id="3762f-128">Behandeln von Menü Ereignissen</span><span class="sxs-lookup"><span data-stu-id="3762f-128">Handling Menu Events</span></span>

<span data-ttu-id="3762f-129">Die Ereignishandler für Menü Elemente aktualisieren hauptsächlich den Status des Formulars.</span><span class="sxs-lookup"><span data-stu-id="3762f-129">The menu item event handlers primarily update the form's state.</span></span>

<span data-ttu-id="3762f-130">Der Befehl CLEAR entfernt das Auswahl Rechteck und löscht die Striche aus dem [Ink](/previous-versions/ms583670(v=vs.100)) -Objekt des frei Hand Sammlers.</span><span class="sxs-lookup"><span data-stu-id="3762f-130">The Clear command removes the selection rectangle, and deletes the strokes from the ink collector's [Ink](/previous-versions/ms583670(v=vs.100)) object.</span></span>

<span data-ttu-id="3762f-131">Der Exit-Befehl deaktiviert den Ink Collector, bevor die Anwendung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="3762f-131">The Exit command disables the ink collector before exiting the application.</span></span>

<span data-ttu-id="3762f-132">Im Menü bearbeiten können Sie die Befehle zum Ausschneiden und kopieren basierend auf dem Auswahl Zustand des Formulars aktivieren und den Befehl Einfügen basierend auf dem Inhalt der Zwischenablage aktivieren, der mithilfe der [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) -Methode des [Ink](/previous-versions/ms583670(v=vs.100)) -Objekts festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="3762f-132">The Edit menu enables the Cut and Copy commands based on the selection state of the form, and enables the Paste command based on the contents of the clipboard, determined by using the [Ink](/previous-versions/ms583670(v=vs.100)) object's [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) method.</span></span>

<span data-ttu-id="3762f-133">Die Befehle zum Ausschneiden und kopieren verwenden beide eine Hilfsmethode, um frei Hand Eingaben in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="3762f-133">The Cut and Copy commands both use a helper method to copy ink to the clipboard.</span></span> <span data-ttu-id="3762f-134">Der Ausschneide Befehl verwendet eine Hilfsmethode, um die ausgewählten Striche zu löschen.</span><span class="sxs-lookup"><span data-stu-id="3762f-134">The Cut command uses a helper method to delete the selected strokes.</span></span>

<span data-ttu-id="3762f-135">Der Befehl "Einfügen" prüft zunächst die [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) -Methode des [Ink](/previous-versions/ms583670(v=vs.100)) -Objekts, um festzustellen, ob das Objekt in der Zwischenablage eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3762f-135">The Paste command first checks the [Ink](/previous-versions/ms583670(v=vs.100)) object's [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) method to see if the object on the clipboard can be pasted.</span></span> <span data-ttu-id="3762f-136">Der Befehl "Einfügen" berechnet dann die linke obere Ecke des Einfügebereichs, konvertiert die Koordinaten von Pixeln in frei Hand Raum und fügt die Striche aus der Zwischenablage in den frei Hand Sammler ein.</span><span class="sxs-lookup"><span data-stu-id="3762f-136">The Paste command then computes the upper-left corner for the paste region, converts the coordinates from pixels to ink space, and pastes the strokes from the clipboard to the ink collector.</span></span> <span data-ttu-id="3762f-137">Schließlich wird das Auswahlfeld aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3762f-137">Finally, the selection box is updated.</span></span>


```C++
if (myInkCollector.Ink.CanPaste())
{
   // Compute the location where the ink should be pasted;
    // this location should be shifted from the origin
    // to account for the width of the selection rectangle's handle.
    Point offset = new Point(leftTopHandle.Width+1,leftTopHandle.Height+1);
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref offset);
    }
    // Use Ink API to paste the clipboard data into the Ink
    Strokes pastedStrokes = myInkCollector.Ink.ClipboardPaste(offset);

    // If the contents of the clipboard were a valid format 
    // (Ink Serialized Format or Embeddable OLE Object) and at
    // least one stroke was pasted into the ink, use a helper 
    // method to update the stroke selection.  Otherwise,
    // the result is null and this paste becomes a no-op.  
    if (null != pastedStrokes)
    {
        SetSelection(pastedStrokes);
    }
}
```



<span data-ttu-id="3762f-138">Die SELECT-und Ink-Befehle aktualisieren den Anwendungsmodus und die Standard Zeichnungs Attribute, löschen die aktuelle Auswahl, aktualisieren den Menü Zustand und aktualisieren das Formular.</span><span class="sxs-lookup"><span data-stu-id="3762f-138">The Select and Ink commands update the application mode and the default drawing attributes, clear the current selection, update the menu state, and refresh the form.</span></span> <span data-ttu-id="3762f-139">Andere Handler greifen auf den Anwendungs Zustand zurück, um die richtige Funktion auszuführen, entweder das Auslagern oder das Ablegen von frei Hand Eingaben.</span><span class="sxs-lookup"><span data-stu-id="3762f-139">Other handlers rely on the application state to perform the correct function, either lassoing or laying down ink.</span></span> <span data-ttu-id="3762f-140">Außerdem fügt der Befehl Select dem Ink Collector die [newcollector](/previous-versions/ms567621(v=vs.100)) -und [Stroke](/previous-versions/ms567622(v=vs.100)) -Ereignishandler hinzu, und der Ink-Befehl entfernt diese Ereignishandler aus dem Ink Collector.</span><span class="sxs-lookup"><span data-stu-id="3762f-140">In addition, the Select command adds the [NewPackets](/previous-versions/ms567621(v=vs.100)) and [Stroke](/previous-versions/ms567622(v=vs.100)) event handlers to the ink collector and the Ink command removes these event handlers from the ink collector.</span></span>

<span data-ttu-id="3762f-141">Die Formate, die in der Zwischenablage verfügbar sind, wenn Striche kopiert werden, werden im Menü Format aufgelistet, und der Benutzer wählt das Format zum Kopieren der frei Hand Eingabe aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="3762f-141">The formats that are available on the Clipboard when strokes are copied are listed on the Format menu, and the user selects the format for copying the ink from this list.</span></span> <span data-ttu-id="3762f-142">Zu den verfügbaren Typen von Formaten gehören das frei Hand Format (Ink Serialized Format, ISF), Metadateien, Erweiterte Metadateien und Bitmap.</span><span class="sxs-lookup"><span data-stu-id="3762f-142">The types of formats available include Ink Serialized Format (ISF), metafile, enhanced metafile, and bitmap.</span></span> <span data-ttu-id="3762f-143">Die Formatierungen von Skizzen Freihand und Text Freihand schließen sich gegenseitig aus und basieren darauf, dass die frei Hand Eingaben als OLE-Objekt in die Zwischenablage kopiert werden</span><span class="sxs-lookup"><span data-stu-id="3762f-143">The sketch ink and text ink formats are mutually exclusive, and rely on the ink being copied to the clipboard as an OLE object.</span></span>

<span data-ttu-id="3762f-144">Das Menü Format ermöglicht dem Benutzer das Ändern der Farb-und breiten Eigenschaften des Stifts und aller ausgewählten Striche.</span><span class="sxs-lookup"><span data-stu-id="3762f-144">The Style menu enables the user to change the color and width properties of the pen and any selected strokes.</span></span>

<span data-ttu-id="3762f-145">Beispielsweise wird mit dem roten Befehl die [Color](/previous-versions/ms582103(v=vs.100)) -Eigenschaft der [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) -Eigenschaft des Ink Collector auf die Farbe Rot festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3762f-145">For example, the Red command sets the [Color](/previous-versions/ms582103(v=vs.100)) property of the ink collector's [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) property to the color red.</span></span> <span data-ttu-id="3762f-146">Da die [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) -Eigenschaft des [Cursor](/previous-versions/ms552104(v=vs.100)) Objekts nicht festgelegt wurde, erben alle neuen frei Hand Eingaben, die in den Ink Collector gezeichnet werden, auf die Standard Zeichenfarbe.</span><span class="sxs-lookup"><span data-stu-id="3762f-146">Because the [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) property of the [Cursor](/previous-versions/ms552104(v=vs.100)) object has not been set, any new ink drawn to the ink collector inherits to default drawing color.</span></span> <span data-ttu-id="3762f-147">Wenn derzeit eine beliebige Striche ausgewählt sind, wird auch die Farb Eigenschaft der Zeichnungs Attribute des Strichs ebenfalls aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3762f-147">Also, if any strokes are currently selected, each stroke's drawing attributes Color property is updated as well.</span></span>


```C++
private void SetColor(Color newColor)
{
    myInkCollector.DefaultDrawingAttributes.Color = newColor;

    // In addition to updating the ink collector, also update
    // the drawing attributes of all selected strokes.
    if (HasSelection())
    {
        foreach (Stroke s in selectedStrokes)
        {
            s.DrawingAttributes.Color = newColor;
        }
    }

    Refresh();
}
```



## <a name="handling-mouse-events"></a><span data-ttu-id="3762f-148">Behandeln von Mausereignissen</span><span class="sxs-lookup"><span data-stu-id="3762f-148">Handling Mouse Events</span></span>

<span data-ttu-id="3762f-149">Der [MouseMove](/previous-versions/ms567617(v=vs.100)) -Ereignishandler überprüft den Anwendungsmodus.</span><span class="sxs-lookup"><span data-stu-id="3762f-149">The [MouseMove](/previous-versions/ms567617(v=vs.100)) event handler checks the application mode.</span></span> <span data-ttu-id="3762f-150">Wenn der Modus moveink ist und eine Maustaste gedrückt ist, verschiebt der Handler die Striche mithilfe der Move-Methode der [Striche](/previous-versions/ms552701(v=vs.100)) -Auflistung und aktualisiert das Auswahlfeld.</span><span class="sxs-lookup"><span data-stu-id="3762f-150">If the mode is MoveInk and a mouse button is down, then the handler moves the strokes by using the [Strokes](/previous-versions/ms552701(v=vs.100)) collection's Move method and updates the selection box.</span></span> <span data-ttu-id="3762f-151">Andernfalls prüft der Handler, ob das Auswahl Rechteck den Cursor enthält, aktiviert die Ink-Auflistung entsprechend und legt den Cursor entsprechend fest.</span><span class="sxs-lookup"><span data-stu-id="3762f-151">Otherwise, the handler checks to determine whether the selection rectangle contains the cursor, enables ink collection accordingly, and also sets the cursor accordingly.</span></span>

<span data-ttu-id="3762f-152">Der [mousetdown](/previous-versions/ms567616(v=vs.100)) -Ereignishandler überprüft die Cursor Einstellung.</span><span class="sxs-lookup"><span data-stu-id="3762f-152">The [MouseDown](/previous-versions/ms567616(v=vs.100)) event handler checks the cursor setting.</span></span> <span data-ttu-id="3762f-153">Wenn der Cursor auf [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1)festgelegt ist, legt der Handler den Anwendungsmodus auf moveink fest und zeichnet die Cursorposition auf.</span><span class="sxs-lookup"><span data-stu-id="3762f-153">If the cursor is set to [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), then the handler sets the application mode to MoveInk and records the cursor location.</span></span> <span data-ttu-id="3762f-154">Wenn eine aktuelle Auswahl vorliegt, löschen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="3762f-154">Otherwise, if there is a current selection, clear it.</span></span>

<span data-ttu-id="3762f-155">Der [MouseUp](/previous-versions/ms567618(v=vs.100)) -Ereignishandler überprüft den Anwendungsmodus.</span><span class="sxs-lookup"><span data-stu-id="3762f-155">The [MouseUp](/previous-versions/ms567618(v=vs.100)) event handler checks the application mode.</span></span> <span data-ttu-id="3762f-156">Wenn der Modus "moveink" ist, legt der Handler den Anwendungsmodus basierend auf dem aktivierten Zustand des Select-Befehls fest.</span><span class="sxs-lookup"><span data-stu-id="3762f-156">If the mode is MoveInk, then the handler sets the application mode based on the Select command's checked state.</span></span>

<span data-ttu-id="3762f-157">Das [newpacket](/previous-versions/ms567621(v=vs.100)) -Ereignis wird im Auswahlmodus ausgelöst, wenn der Ink Collector neue Paketdaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="3762f-157">The [NewPackets](/previous-versions/ms567621(v=vs.100)) event is raised in selection mode when the ink collector receives new packet data.</span></span> <span data-ttu-id="3762f-158">Wenn sich die Anwendung im Auswahlmodus befindet, müssen die neuen Pakete abgefangen und zum Zeichnen der Auswahl-Lasso verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3762f-158">If the application is in selection mode, it is necessary to intercept the new packets and use them to draw the selection lasso.</span></span>

<span data-ttu-id="3762f-159">Die Koordinaten jedes Pakets werden in Pixel konvertiert, auf den Zeichenbereich beschränkt und der Auflistung von Punkten von Lasso hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3762f-159">Each packet's coordinate is converted to pixels, constrained to the drawing area, and added to the lasso's collection of points.</span></span> <span data-ttu-id="3762f-160">Anschließend wird eine Hilfsmethode aufgerufen, um die Lassopfad im Formular zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="3762f-160">A helper method is then called to draw the lasso on the form.</span></span>

## <a name="handling-a-new-stroke"></a><span data-ttu-id="3762f-161">Behandeln eines neuen Strichs</span><span class="sxs-lookup"><span data-stu-id="3762f-161">Handling a New Stroke</span></span>

<span data-ttu-id="3762f-162">Das [Stroke](/previous-versions/ms567622(v=vs.100)) -Ereignis wird im Auswahlmodus ausgelöst, wenn ein neuer Strich gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3762f-162">The [Stroke](/previous-versions/ms567622(v=vs.100)) event is raised in the selection mode when a new stroke is drawn.</span></span> <span data-ttu-id="3762f-163">Wenn sich die Anwendung im Auswahlmodus befindet, entspricht dieser Strich dem Lassopfad, und es ist erforderlich, die Informationen zu den ausgewählten Strichen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3762f-163">If the application is in selection mode, this stroke corresponds to the lasso and it is necessary to update the selected strokes' information.</span></span>

<span data-ttu-id="3762f-164">Der Handler bricht das [Stroke](/previous-versions/ms567622(v=vs.100)) -Ereignis ab, prüft auf mehr als zwei Lassopfad-Punkte, kopiert die Points-Auflistung in ein Array von [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) -Objekten und konvertiert die Koordinaten der Punkte im Array von Pixel in frei Hand Raum.</span><span class="sxs-lookup"><span data-stu-id="3762f-164">The handler cancels the [Stroke](/previous-versions/ms567622(v=vs.100)) event, checks for more than two lasso points, copies the Points collection to an array of [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) objects, and converts the coordinates of the points in the array from pixels to ink space.</span></span> <span data-ttu-id="3762f-165">Anschließend verwendet der Handler die [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) -Methode des [Ink](/previous-versions/ms583670(v=vs.100)) -Objekts, um die von den Lassopfad-Punkten ausgewählten Striche zu erhalten und den Auswahl Zustand des Formulars zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3762f-165">Then, the handler uses the [Ink](/previous-versions/ms583670(v=vs.100)) object's [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method to get the strokes selected by the lasso points and updates the selection state of the form.</span></span> <span data-ttu-id="3762f-166">Schließlich wird der Strich, der das Ereignis ausgelöst hat, aus der Auflistung ausgewählter Striche entfernt, die Lassopfad Points-Auflistung wird geleert, und eine Hilfsmethode zeichnet das Auswahl Rechteck.</span><span class="sxs-lookup"><span data-stu-id="3762f-166">Finally, the stroke that raised the event is removed from the collection of selected strokes, the lasso Points collection is emptied, and a helper method draws the selection rectangle.</span></span>


```C++
// This stroke corresponds to the lasso - 
// cancel it so that it is not added into the ink
e.Cancel = true;  

Strokes hitStrokes = null;

// If there are enough lasso points, perform a hit test
// to determine which strokes were selected. 
if (lassoPoints.Count > 2)
{

    // Convert the lasso points from pixels to ink space
    Point[] inkLassoPoints = (Point[])lassoPoints.ToArray(typeof(Point));
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref inkLassoPoints);
    }
    // Perform a hit test on this ink collector's ink to
    // determine which points were selected by the lasso stroke.
    //
    // Note that there is a slight inefficiency here since the
    // lasso stroke is part of the ink and, therefore, part of the
    // hit test - even though we don't need it.   It would have 
    // been more efficient to remove the stroke from the ink before 
    // calling HitTest.  However, it is not good practice to modify 
    // the stroke inside of its own event handler.
    hitStrokes = myInkCollector.Ink.HitTest(inkLassoPoints, LassoPercent);
    hitStrokes.Remove(e.Stroke);
}

// Reset the lasso points
lassoPoints.Clear();
lastDrawnLassoDot = Point.Empty;

// Use helper method to set the selection
SetSelection(hitStrokes);
```



## <a name="copying-ink-to-the-clipboard"></a><span data-ttu-id="3762f-167">Kopieren von Freihand in die Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="3762f-167">Copying Ink to the Clipboard</span></span>

<span data-ttu-id="3762f-168">Die Hilfsmethode copyinktoclipboard erstellt einen [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) -Wert, überprüft den Status des Menüs, um die Formate zu aktualisieren, die in die Zwischenablage eingefügt werden sollen, und verwendet die [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) -Methode des [Ink](/previous-versions/ms583670(v=vs.100)) -Objekts, um die Striche in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="3762f-168">The CopyInkToClipboard helper method creates an [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) value, checks the Format menu's state to update the formats to put on the clipboard, and uses the [Ink](/previous-versions/ms583670(v=vs.100)) object's [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) method to copy the strokes to the clipboard.</span></span>


```C++
// Declare the ink clipboard formats to put on the clipboard
InkClipboardFormats formats = new InkClipboardFormats();

// Use selected format menu items to set the clipboard 
// formats
...

// If at least one format was selected, invoke the Ink
// API's ClipboardCopy method.  Note that selectedStrokes
// could be null, but that this is ok - if selectedStrokes
// is null, all of the ink is copied.
if (formats != InkClipboardFormats.None)
{
    myInkCollector.Ink.ClipboardCopy(selectedStrokes,formats,clipboardModes);
}
else
{
    MessageBox.Show("No clipboard formats selected");
}
```



## <a name="updating-a-selection"></a><span data-ttu-id="3762f-169">Aktualisieren einer Auswahl</span><span class="sxs-lookup"><span data-stu-id="3762f-169">Updating a Selection</span></span>

<span data-ttu-id="3762f-170">Mit der setSelection-Hilfsmethode wird die protokollierte selectedStrokes-Methode aktualisiert. wenn die Auflistung **null** oder **leer** ist, wird das Auswahl Rechteck auf das leere Rechteck festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3762f-170">The SetSelection helper method updates the selectedStrokes filed and if the collection is **NULL** or **EMPTY**, the selection rectangle is set to the empty rectangle.</span></span> <span data-ttu-id="3762f-171">Wenn die ausgewählte [Striche](/previous-versions/ms552701(v=vs.100)) -Auflistung nicht leer ist, führt die setSelection-Methode die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="3762f-171">If the selected [Strokes](/previous-versions/ms552701(v=vs.100)) collection is not empty the SetSelection method performs the following steps:</span></span>

-   <span data-ttu-id="3762f-172">Bestimmt das umgebende Rechteck mithilfe der [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) -Methode der Striche-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="3762f-172">Determines the bounding rectangle by using the [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) method of the strokes collection</span></span>
-   <span data-ttu-id="3762f-173">Konvertiert die Rechteck Koordinaten aus dem frei Handzeichen Bereich in Pixel.</span><span class="sxs-lookup"><span data-stu-id="3762f-173">Converts the rectangle coordinates from ink space to pixels</span></span>
-   <span data-ttu-id="3762f-174">Vergrößert das Rechteck, um zwischen ihm und den ausgewählten Strichen einen visuellen Bereich bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3762f-174">Inflates the rectangle to provide some visual space between it and the selected strokes</span></span>
-   <span data-ttu-id="3762f-175">Erstellt Auswahl Handles für das aktuelle Auswahlfeld.</span><span class="sxs-lookup"><span data-stu-id="3762f-175">Creates selection handles for the current selection box</span></span>

<span data-ttu-id="3762f-176">Schließlich legt die setSelection-Methode die Sichtbarkeit der Auswahl Handles fest und legt die [AutoRedraw](/previous-versions/ms571706(v=vs.100)) -Eigenschaft des Ink Collector auf **false** fest, wenn Striche ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="3762f-176">Finally, the SetSelection method sets the visibility of the selection handles and sets the ink collector's [AutoRedraw](/previous-versions/ms571706(v=vs.100)) property to **FALSE**, if strokes are selected.</span></span>


```C++
// Tracks whether the rectangle that bounds the selected
// strokes should be displayed
bool isSelectionVisible = false;

// Update the selected strokes collection
selectedStrokes = strokes;

// If no strokes are selected, set the selection rectangle
// to empty
if (!HasSelection())
{
    selectionRect = Rectangle.Empty;
}
    // Otherwise, at least one stroke is selected and it is necessary
    // to display the selection rectangle.
else
{
    isSelectionVisible = true;

    // Retrieve the bounding box of the strokes
    selectionRect = selectedStrokes.GetBoundingBox();
    using (Graphics g = CreateGraphics())
    {
        InkSpaceToPixel(g, ref selectionRect);
    }

    // Pad the selection rectangle so that the selected ink 
    // doesn't overlap with the selection rectangle's handles.
    selectionRect.Inflate(SelectionRectBuffer, SelectionRectBuffer);

    // compute the center of the rectangle that bounds the 
    // selected strokes
    int xAvg = (selectionRect.Right+selectionRect.Left)/2;
    int yAvg = (selectionRect.Top+selectionRect.Bottom)/2;

    // Draw the resize handles
    // top left
    SetLocation(selectionHandles[0],selectionRect.Left, selectionRect.Top);
    // top
    SetLocation(selectionHandles[1],xAvg, selectionRect.Top);
    // top right 
    SetLocation(selectionHandles[2],selectionRect.Right, selectionRect.Top);

    // left 
    SetLocation(selectionHandles[3],selectionRect.Left, yAvg);
    // right
    SetLocation(selectionHandles[4],selectionRect.Right, yAvg);

    // bottom left
    SetLocation(selectionHandles[5],selectionRect.Left, selectionRect.Bottom);
    // bottom
    SetLocation(selectionHandles[6],xAvg, selectionRect.Bottom);
    // bottom right
    SetLocation(selectionHandles[7],selectionRect.Right, selectionRect.Bottom);
}

// Set the visibility of each selection handle in the 
// selection rectangle.  If there is no selection, all 
// handles should be hidden.  Otherwise, all handles should
// be visible.
foreach(PictureBox pb in selectionHandles)
{
    pb.Visible = isSelectionVisible;
}

// Turn off autoredrawing if there is a selection - otherwise,
// the selected ink is not displayed as selected.
myInkCollector.AutoRedraw = !isSelectionVisible;

// Since the selection has changed, repaint the screen.
Refresh();
```



## <a name="drawing-the-lasso"></a><span data-ttu-id="3762f-177">Zeichnen von Lasso</span><span class="sxs-lookup"><span data-stu-id="3762f-177">Drawing the Lasso</span></span>

<span data-ttu-id="3762f-178">Der Lassopfad wird als eine Reihe von offenen Punkten gezeichnet, die dem Pfad des Lassopfad-Strichs und einer gestrichelten Verbindungslinie zwischen den beiden Enden folgen.</span><span class="sxs-lookup"><span data-stu-id="3762f-178">The lasso is drawn as a series of open dots that follow the path of the lasso stroke and a dashed connector line between the two ends.</span></span> <span data-ttu-id="3762f-179">Das [newpakete](/previous-versions/ms567621(v=vs.100)) -Ereignis wird ausgelöst, wenn das Lassopfad gezeichnet wird, und der Ereignishandler übergibt die Strich Informationen an die drawlasso-Methode.</span><span class="sxs-lookup"><span data-stu-id="3762f-179">The [NewPackets](/previous-versions/ms567621(v=vs.100)) event is raised as the lasso is being drawn, and the event handler passes the stroke information to the DrawLasso method.</span></span>

<span data-ttu-id="3762f-180">Die drawlasso-Hilfsmethode entfernt zuerst die alte Verbindungslinie und durchläuft dann die Punkte im Strich.</span><span class="sxs-lookup"><span data-stu-id="3762f-180">The DrawLasso helper method first removes the old connector line and then iterates over the points in the stroke.</span></span> <span data-ttu-id="3762f-181">Dann berechnet drawlasso, wo die Punkte auf dem Strich platziert werden, und zeichnet Sie.</span><span class="sxs-lookup"><span data-stu-id="3762f-181">Then, DrawLasso calculates where to place the dots along the stroke and draws them.</span></span> <span data-ttu-id="3762f-182">Schließlich zeichnet er eine neue Connector-Linie.</span><span class="sxs-lookup"><span data-stu-id="3762f-182">Finally, it draws a new connector line.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="3762f-183">Schließen des Formulars</span><span class="sxs-lookup"><span data-stu-id="3762f-183">Closing the Form</span></span>

<span data-ttu-id="3762f-184">Die [verwerfen-Methode des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) gibt das [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt myinkcollector frei.</span><span class="sxs-lookup"><span data-stu-id="3762f-184">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object, myInkCollector.</span></span>

 

 
