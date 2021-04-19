---
description: In diesem C- \# Beispiel wurde ein Papierformular als Portable Network Graphics (PNG-Datei) gescannt und zur Laufzeit als Hintergrundbild für ein InkPicture-Steuerelement angegeben. Im Beispiel wird ein Meldungs Feld verwendet, um Handschrift Erkennungsergebnisse anzuzeigen.
ms.assetid: fc9a39c2-9e4b-4d22-a118-3d24544897dd
title: Beispiel für gescannte Papier Form
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d60e1d62a4e023ba38e9a1fd2c4890288a542d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360678"
---
# <a name="scanned-paper-form-sample"></a><span data-ttu-id="62d58-104">Beispiel für gescannte Papier Form</span><span class="sxs-lookup"><span data-stu-id="62d58-104">Scanned Paper Form Sample</span></span>

<span data-ttu-id="62d58-105">In diesem C- \# Beispiel wurde ein Papierformular als Portable Network Graphics (PNG-Datei) gescannt und zur Laufzeit als Hintergrundbild für ein [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement angegeben.</span><span class="sxs-lookup"><span data-stu-id="62d58-105">In this C\# sample, a paper form has been scanned as a Portable Network Graphics (PNG) file and specified as the background image at run time for a [InkPicture](/previous-versions/aa514604(v=msdn.10)) control.</span></span> <span data-ttu-id="62d58-106">Im Beispiel wird ein Meldungs Feld verwendet, um Handschrift Erkennungsergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="62d58-106">The sample uses a message box to display handwriting recognition results.</span></span>

<span data-ttu-id="62d58-107">Das Beispiel enthält eine Extensible Markup Language-Datei (XML) Formdata.xml.</span><span class="sxs-lookup"><span data-stu-id="62d58-107">The sample includes an Extensible Markup Language (XML) file, Formdata.xml.</span></span> <span data-ttu-id="62d58-108">Die XML-Datei enthält den Namen der PNG-Datei.</span><span class="sxs-lookup"><span data-stu-id="62d58-108">The XML file contains the name of the PNG file.</span></span> <span data-ttu-id="62d58-109">Sie enthält auch `FieldInfo` Elemente, die rechteckige Bereiche in dem Formular definieren, in dem ein Benutzer Freihand eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="62d58-109">It also contains `FieldInfo` elements that define rectangular regions on the form where a user can enter ink.</span></span> <span data-ttu-id="62d58-110">Die Informationen im- `FieldInfo` Element werden im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="62d58-110">The information in the `FieldInfo` element is shown in the following example:</span></span>


```C++
    <FieldInfo>
        <Name>first name</Name>
        <Left>88</Left>
        <Top>65</Top>
        <Right>332</Right>
        <Bottom>94</Bottom>
    </FieldInfo>
```



<span data-ttu-id="62d58-111">Die Elemente "Left", "Top", "Right" und "Bottom" sind Definitionen von Pixelkoordinaten für jedes Feld.</span><span class="sxs-lookup"><span data-stu-id="62d58-111">The Left, Top, Right, and Bottom elements are definitions of pixel coordinates for each field.</span></span>

<span data-ttu-id="62d58-112">Im Beispiel wird ein neues [DataSet](/dotnet/api/system.data.dataset?view=netcore-3.1) mit den in Formdata.xml enthaltenen Daten initialisiert:</span><span class="sxs-lookup"><span data-stu-id="62d58-112">The sample initializes a new [DataSet](/dotnet/api/system.data.dataset?view=netcore-3.1) with the data contained in Formdata.xml:</span></span>


```C++
    formData = new DataSet("FormData");
    formData.ReadXml("formdata.xml"); 
```



<span data-ttu-id="62d58-113">Das in Formdata.xml angegebene Formular Bild wird als Hintergrund des [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuer Elements geladen:</span><span class="sxs-lookup"><span data-stu-id="62d58-113">The form image specified in Formdata.xml is loaded as the background of the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control:</span></span>


```C++
    inkPicture1.BackgroundImage = 
        System.Drawing.Image.FromFile(
        (string) formData.Tables["FormData"].Rows[0]["Image"]);
```



<span data-ttu-id="62d58-114">Die frei Hand Auflistung wird dann für das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement aktiviert:</span><span class="sxs-lookup"><span data-stu-id="62d58-114">Ink collection is then enabled for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control:</span></span>


```C++
    inkPicture1.InkEnabled = true;
```



## <a name="menu-event-handlers"></a><span data-ttu-id="62d58-115">Menü Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="62d58-115">Menu Event Handlers</span></span>

<span data-ttu-id="62d58-116">Die Anwendung umfasst Click-Ereignishandler für alle Menüs, die am oberen Rand des Formulars angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="62d58-116">The application includes click event handlers for all of the menus displayed along the top of the form.</span></span>

### <a name="recognize-menu-item"></a><span data-ttu-id="62d58-117">Menü Element "erkennen"</span><span class="sxs-lookup"><span data-stu-id="62d58-117">Recognize Menu Item</span></span>

<span data-ttu-id="62d58-118">Der Menübefehl zum Erkennen von Click-Ereignis Handlern deaktiviert die frei Hand Auflistung für das Steuerelement und überprüft die Handschrifterkennung.</span><span class="sxs-lookup"><span data-stu-id="62d58-118">The Recognize menu click event handler disables ink collection for the control and checks for a handwriting recognizer.</span></span> <span data-ttu-id="62d58-119">Wenn keine Erkennung installiert ist, wird ein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="62d58-119">If no recognizer is installed, a dialog box is displayed.</span></span> <span data-ttu-id="62d58-120">Ein Benutzer muss dann auf die Menüoption "Ink" oder "Pen" klicken, um das Steuerelement für die frei Hand Eingabe erneut zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="62d58-120">A user must then click the Ink or Pen menu option to re-enable the control for ink input.</span></span>

<span data-ttu-id="62d58-121">Wenn eine Erkennung installiert ist, ruft die `Recognize` Funktion die XML-Daten ab, die Pixelkoordinaten für jedes Formularfeld angeben.</span><span class="sxs-lookup"><span data-stu-id="62d58-121">If a recognizer is installed, the `Recognize` function retrieves the XML data that specifies pixel coordinates for each form field.</span></span> <span data-ttu-id="62d58-122">Die Koordinaten werden in Freihand Raumkoordinaten konvertiert, und für jedes Formularfeld wird ein Rechteck definiert.</span><span class="sxs-lookup"><span data-stu-id="62d58-122">The coordinates are converted to ink space coordinates, and a rectangle is defined for each form field.</span></span> <span data-ttu-id="62d58-123">Nachdem Rechtecke definiert wurden, sucht die Funktion die Striche, die sich überschneiden und innerhalb jedes Rechtecks liegen.</span><span class="sxs-lookup"><span data-stu-id="62d58-123">After rectangles are defined, the function finds the strokes that intersect and lie within each rectangle.</span></span> <span data-ttu-id="62d58-124">Zum Schluss führt Sie eine Erkennung der frei Hand Eingaben durch und zeigt die Ergebnisse in einem Meldungs Feld an.</span><span class="sxs-lookup"><span data-stu-id="62d58-124">Finally, it performs recognition on the ink and displays the results in a message box.</span></span>

### <a name="ink-menu-item"></a><span data-ttu-id="62d58-125">Ink-Menü Element</span><span class="sxs-lookup"><span data-stu-id="62d58-125">Ink Menu Item</span></span>

<span data-ttu-id="62d58-126">Das Handschrift-Ereignishandler aktiviert das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="62d58-126">The Ink menu click event handler enables the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control.</span></span>

### <a name="pen-menu-item"></a><span data-ttu-id="62d58-127">Stift-Menü Element</span><span class="sxs-lookup"><span data-stu-id="62d58-127">Pen Menu Item</span></span>

<span data-ttu-id="62d58-128">Der Ereignishandler für den Stift Menübefehl führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="62d58-128">The Pen menu click event handler performs the following tasks:</span></span>

-   <span data-ttu-id="62d58-129">Deaktiviert die frei Hand Auflistung für das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement (Dies ist erforderlich, bevor die [EditingMode](/previous-versions/ms582189(v=vs.100)) -Eigenschaft geändert wird).</span><span class="sxs-lookup"><span data-stu-id="62d58-129">Disables ink collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control (which is necessary before changing the [EditingMode](/previous-versions/ms582189(v=vs.100)) property).</span></span>
-   <span data-ttu-id="62d58-130">Legt die [EditingMode](/previous-versions/ms582189(v=vs.100)) -Eigenschaft zum Erfassen von frei Hand Eingaben fest.</span><span class="sxs-lookup"><span data-stu-id="62d58-130">Sets the [EditingMode](/previous-versions/ms582189(v=vs.100)) property to collect ink.</span></span>
-   <span data-ttu-id="62d58-131">Aktiviert die frei Hand Auflistung für das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement erneut und schaltet die Menüs "Pen", "Select" und "Eraser" um, um den aktiven Modus anzugeben.</span><span class="sxs-lookup"><span data-stu-id="62d58-131">Re-enables ink collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control and toggles the Pen, Select, and Eraser menus to indicate the active mode.</span></span>

### <a name="edit-menu-item"></a><span data-ttu-id="62d58-132">Menü Element bearbeiten</span><span class="sxs-lookup"><span data-stu-id="62d58-132">Edit Menu Item</span></span>

<span data-ttu-id="62d58-133">Der Ereignishandler für den Menübefehl Bearbeiten ähnelt dem Ereignishandler für den Stift-Menü.</span><span class="sxs-lookup"><span data-stu-id="62d58-133">The Edit menu click event handler is similar to the Pen menu event handler.</span></span> <span data-ttu-id="62d58-134">Sie führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="62d58-134">It performs the following tasks:</span></span>

-   <span data-ttu-id="62d58-135">Deaktiviert die frei Hand Auflistung.</span><span class="sxs-lookup"><span data-stu-id="62d58-135">Disables ink collection.</span></span>
-   <span data-ttu-id="62d58-136">Legt die [EditingMode](/previous-versions/ms582189(v=vs.100)) -Eigenschaft auf **Select** fest. Dadurch kann der Benutzer die frei Handauswahl ausführen.</span><span class="sxs-lookup"><span data-stu-id="62d58-136">Sets the [EditingMode](/previous-versions/ms582189(v=vs.100)) property to **Select**, which enables the user to perform ink selection.</span></span>
-   <span data-ttu-id="62d58-137">Aktiviert die frei Hand Auflistung und schaltet die Menü Stift-, Bearbeitungs-und eramingmenüs um, um den aktiven Modus anzugeben.</span><span class="sxs-lookup"><span data-stu-id="62d58-137">Re-enables ink collection and toggles the Pen, Edit, and Eraser menus to indicate the active mode.</span></span>

### <a name="eraser-menu-item"></a><span data-ttu-id="62d58-138">Menü Element "Eraser"</span><span class="sxs-lookup"><span data-stu-id="62d58-138">Eraser Menu Item</span></span>

<span data-ttu-id="62d58-139">Mit dem Menübefehl zum durch Klicken auf den Ereignishandler wird das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement [EditingMode](/previous-versions/ms582189(v=vs.100)) auf **Delete** festgelegt, sodass ein Benutzer frei Hand Eingaben löschen kann.</span><span class="sxs-lookup"><span data-stu-id="62d58-139">The Eraser menu click event handler sets the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control [EditingMode](/previous-versions/ms582189(v=vs.100)) to **Delete**, which enables a user to erase ink.</span></span> <span data-ttu-id="62d58-140">Außerdem schaltet er die Menü Elemente Pen, Edit und Eraser um.</span><span class="sxs-lookup"><span data-stu-id="62d58-140">It also toggles the Pen, Edit, and Eraser menu items.</span></span>

### <a name="clear-menu-item"></a><span data-ttu-id="62d58-141">Menü Element löschen</span><span class="sxs-lookup"><span data-stu-id="62d58-141">Clear Menu Item</span></span>

<span data-ttu-id="62d58-142">Der Menübefehl zum Löschen des Menüs löschen löscht die aktuelle [Striche](/previous-versions/ms552701(v=vs.100)) -Auflistung für das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement und löscht dadurch alle frei Hand Eingaben im Formular.</span><span class="sxs-lookup"><span data-stu-id="62d58-142">The Clear menu click event handler deletes the current [Strokes](/previous-versions/ms552701(v=vs.100)) collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control, thereby erasing all of the ink on the form.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="62d58-143">Schließen des Formulars</span><span class="sxs-lookup"><span data-stu-id="62d58-143">Closing the Form</span></span>

<span data-ttu-id="62d58-144">Im vom Windows Form-Designer generierten Code wird das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement der Komponentenliste des Formulars hinzugefügt, wenn das Formular initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="62d58-144">In the Windows Form Designer generated code, the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control is added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="62d58-145">Wenn das Formular geschlossen wird, wird das InkPicture-Steuerelement und die anderen Komponenten des Formulars [von der verwerfen](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) -Methode des Formulars entfernt.</span><span class="sxs-lookup"><span data-stu-id="62d58-145">When the form closes, the InkPicture control is disposed, as well as the other components of the form, by the form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62d58-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="62d58-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62d58-147">InkEdit-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="62d58-147">InkEdit Control</span></span>](inkedit-control.md)
</dt> <dt>

[<span data-ttu-id="62d58-148">InkPicture-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="62d58-148">InkPicture Control</span></span>](inkpicture-control.md)
</dt> </dl>

 

 
