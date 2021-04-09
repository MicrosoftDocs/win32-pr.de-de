---
title: Sicherstellen, dass Benutzeroberflächen Elemente ordnungsgemäß benannt sind
description: In diesem Thema wird beschrieben, wie Sie die Namen der Benutzeroberflächen Elemente in Ihren Microsoft Win32-Anwendungen angeben, damit Microsoft Active Accessibility die Namen für Client Anwendungen mithilfe von "IAccessible \ 32;" korrekt verfügbar machen kann. Name-Eigenschaft.
ms.assetid: 5b8f23cb-9906-4cc4-83d4-73fdf96ed681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db3c4f1fc129aea9b793bac1935d678645b28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948801"
---
# <a name="ensuring-that-ui-elements-are-correctly-named"></a><span data-ttu-id="9509b-103">Sicherstellen, dass Benutzeroberflächen Elemente ordnungsgemäß benannt sind</span><span class="sxs-lookup"><span data-stu-id="9509b-103">Ensuring that UI Elements are Correctly Named</span></span>

<span data-ttu-id="9509b-104">In diesem Thema wird beschrieben, wie Sie die Namen der Benutzeroberflächen Elemente in Ihren Microsoft Win32-Anwendungen angeben, damit Microsoft Active Accessibility die Namen von Client Anwendungen mithilfe der Eigenschaft " [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [Name](name-property.md)" genau verfügbar machen kann.</span><span class="sxs-lookup"><span data-stu-id="9509b-104">This topic describes the correct way to specify the names of the UI elements in your Microsoft Win32 applications so that Microsoft Active Accessibility can accurately expose the names to client applications through the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [Name property](name-property.md).</span></span>

<span data-ttu-id="9509b-105">Die Informationen in diesem Abschnitt gelten nur für Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="9509b-105">The information in this section applies to Microsoft Active Accessibility only.</span></span> <span data-ttu-id="9509b-106">Dies gilt nicht für Anwendungen, die Microsoft UI Automation verwenden, oder für Anwendungen, die auf Markup Sprachen basieren, z. b. html, Dynamic HTML (DHTML) oder XML.</span><span class="sxs-lookup"><span data-stu-id="9509b-106">It does not apply to applications that use Microsoft UI Automation or those based on markup languages such as HTML, Dynamic HTML (DHTML), or XML.</span></span>

-   [<span data-ttu-id="9509b-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="9509b-107">Overview</span></span>](#overview)
-   [<span data-ttu-id="9509b-108">Fehler durch falsche Benennung</span><span class="sxs-lookup"><span data-stu-id="9509b-108">How Incorrect Naming Causes Problems</span></span>](#how-incorrect-naming-causes-problems)
-   [<span data-ttu-id="9509b-109">Abrufen der Name-Eigenschaft durch MSAA</span><span class="sxs-lookup"><span data-stu-id="9509b-109">How MSAA Gets the Name Property</span></span>](#how-msaa-gets-the-name-property)
-   [<span data-ttu-id="9509b-110">Suchen und Beheben von Benennungs Problemen</span><span class="sxs-lookup"><span data-stu-id="9509b-110">How to Find and Correct Naming Problems</span></span>](#how-to-find-and-correct-naming-problems)
-   [<span data-ttu-id="9509b-111">So benennen Sie eine TrackBar ordnungsgemäß</span><span class="sxs-lookup"><span data-stu-id="9509b-111">How to Correctly Name a Trackbar</span></span>](#how-to-correctly-name-a-trackbar)
-   [<span data-ttu-id="9509b-112">Verwenden von nicht sichtbaren Bezeichnungen zum Benennen von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="9509b-112">How to Use Invisible Labels to Name Controls</span></span>](#how-to-use-invisible-labels-to-name-controls)
-   [<span data-ttu-id="9509b-113">Verwenden der direkten Anmerkung zum Angeben der Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9509b-113">How to Use Direct Annotation to Specify the Name Property</span></span>](#how-to-use-direct-annotation-to-specify-the-name-property)
    -   [<span data-ttu-id="9509b-114">Schritte zum Hinzufügen einer Anmerkung zu der Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9509b-114">Steps for Annotating the Name Property</span></span>](#steps-for-annotating-the-name-property)
    -   [<span data-ttu-id="9509b-115">Beispiel für das kommentieren der Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9509b-115">Example of Annotating the Name Property</span></span>](#example-of-annotating-the-name-property)
-   [<span data-ttu-id="9509b-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9509b-116">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="9509b-117">Übersicht</span><span class="sxs-lookup"><span data-stu-id="9509b-117">Overview</span></span>

<span data-ttu-id="9509b-118">In Microsoft Active Accessibility wird jedes Benutzeroberflächen Element in einer Anwendung durch ein Objekt dargestellt, das die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="9509b-118">In Microsoft Active Accessibility, each UI element in an application is represented by an object that exposes the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="9509b-119">Client Anwendungen verwenden die Eigenschaften und Methoden der **IAccessible** -Schnittstelle für die Interaktion mit dem UI-Element und das Abrufen von Informationen über die Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9509b-119">Client applications use the properties and methods of the **IAccessible** interface to interact with the UI element and to retrieve information about it.</span></span> <span data-ttu-id="9509b-120">Eine der wichtigsten Eigenschaften, die von der **IAccessible** -Schnittstelle verfügbar gemacht wird, ist die [Name-Eigenschaft](name-property.md).</span><span class="sxs-lookup"><span data-stu-id="9509b-120">One of the most important properties exposed by the **IAccessible** interface is the [Name property](name-property.md).</span></span> <span data-ttu-id="9509b-121">Client Anwendungen verlassen sich auf die Name-Eigenschaft, um dem Benutzer ein Benutzeroberflächen Element zu suchen, zu identifizieren oder zu ankündigen.</span><span class="sxs-lookup"><span data-stu-id="9509b-121">Client applications rely on the Name property to find, identify, or announce a UI element to the user.</span></span> <span data-ttu-id="9509b-122">Wenn die Name-Eigenschaft eines bestimmten UI-Elements von Microsoft Active Accessibility nicht ordnungsgemäß verfügbar gemacht werden kann, ist es nicht möglich, dass Client Anwendungen dieses UI-Element dem Benutzer präsentieren, und das Benutzeroberflächen Element ist für Benutzer mit Behinderungen nicht zugänglich.</span><span class="sxs-lookup"><span data-stu-id="9509b-122">If Microsoft Active Accessibility cannot properly expose the Name property of a particular UI element, client applications will be unable to present that UI element to the user, and the UI element will be inaccessible to users with disabilities.</span></span>

## <a name="how-incorrect-naming-causes-problems"></a><span data-ttu-id="9509b-123">Fehler durch falsche Benennung</span><span class="sxs-lookup"><span data-stu-id="9509b-123">How Incorrect Naming Causes Problems</span></span>

<span data-ttu-id="9509b-124">Zum Veranschaulichen der Probleme, die durch eine falsche Benennung von UI-Elementen verursacht werden, sollten Sie das in der folgenden Abbildung gezeigte namens Eingabeformular in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="9509b-124">To illustrate the problems caused by incorrect naming of UI elements, consider the name entry form shown in the following illustration.</span></span>

![Darstellung eines einfachen Formulars für die Eingabe von vor-und Nachname](images/incorrect-form.png)

<span data-ttu-id="9509b-126">Obwohl die Benutzeroberflächen Elemente im Formular okay aussehen, ist die programmgesteuerte Implementierung falsch.</span><span class="sxs-lookup"><span data-stu-id="9509b-126">Although the UI elements in the form look okay, the programmatic implementation is incorrect.</span></span> <span data-ttu-id="9509b-127">An einen Microsoft Active Accessibility-Client, z. b. eine Bildschirm Sprachausgabe, lautet die [Name-Eigenschaft](name-property.md) des Top-Bearbeitungs Steuer Elements "Nachname:", und die Name-Eigenschaft des unteren Bearbeitungs Steuer Elements ist eine leere Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="9509b-127">To a Microsoft Active Accessibility client such as a screen reader, the [Name property](name-property.md) of the top edit control is "Last Name:", and the Name property of the bottom edit control is an empty string ("").</span></span> <span data-ttu-id="9509b-128">Die Sprachausgabe liest das oberste Bearbeitungs Steuerelement als "Nachname", obwohl der Benutzer erwartet, dass der Vorname den Vornamen erhält.</span><span class="sxs-lookup"><span data-stu-id="9509b-128">The screen reader will read the top edit control as "Last Name", although the user is expected to type in the first name.</span></span> <span data-ttu-id="9509b-129">Die Sprachausgabe liest das zweite Bearbeitungs Steuerelement als "kein Name", sodass der Benutzer nicht weiß, was in das zweite Bearbeitungs Steuerelement eingetippt werden muss.</span><span class="sxs-lookup"><span data-stu-id="9509b-129">The screen reader will read the second edit control as "no name", so the user will have no idea what to type into the second edit control.</span></span> <span data-ttu-id="9509b-130">Die Sprachausgabe kann den Benutzer nicht dazu unterstützen, Daten in diese einfache Form einzugeben.</span><span class="sxs-lookup"><span data-stu-id="9509b-130">The screen reader is unable to assist the user in entering data into this simple form.</span></span>

<span data-ttu-id="9509b-131">Ein weiteres Problem mit dem Formular besteht darin, dass keinem der Bearbeitungs Steuerelemente Tastenkombinationen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="9509b-131">Another problem with the form is that no shortcut keys are assigned to either of the edit controls.</span></span> <span data-ttu-id="9509b-132">Der Benutzer wird gezwungen, entweder die Tab-Taste zu den Steuerelementen zu bewegen oder die Maus zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9509b-132">The user is forced to either tab to the controls or use the mouse.</span></span>

<span data-ttu-id="9509b-133">In den folgenden Abschnitten wird die Quelle dieser Probleme erläutert und Richtlinien für deren Behebung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="9509b-133">The following sections explain the source of these problems and provide guidelines for correcting them.</span></span>

## <a name="how-msaa-gets-the-name-property"></a><span data-ttu-id="9509b-134">Abrufen der Name-Eigenschaft durch MSAA</span><span class="sxs-lookup"><span data-stu-id="9509b-134">How MSAA Gets the Name Property</span></span>

<span data-ttu-id="9509b-135">Die [Name-Eigenschafts](name-property.md) Zeichenfolge wird von Microsoft Active Accessibility abhängig vom Typ des Benutzeroberflächen Elements von verschiedenen Speicherorten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9509b-135">Microsoft Active Accessibility gets the [Name property](name-property.md) string from different locations depending on the type of the UI element.</span></span> <span data-ttu-id="9509b-136">Für die meisten Elemente der Benutzeroberfläche, denen Fenster Text zugeordnet ist, verwendet Microsoft Active Accessibility den Fenster Text als Name-Eigenschafts Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9509b-136">For most UI elements that have associated window text, Microsoft Active Accessibility uses the window text as the Name property string.</span></span> <span data-ttu-id="9509b-137">Beispiele für diese Art von Benutzeroberflächen Element sind Steuerelemente wie Schaltflächen, Menü Elemente und Quick Infos.</span><span class="sxs-lookup"><span data-stu-id="9509b-137">Examples of this type of UI element include controls such as buttons, menu items, and tooltips.</span></span>

<span data-ttu-id="9509b-138">Bei den folgenden Steuerelementen ignoriert Microsoft Active Accessibility den Fenster Text und sucht stattdessen nach einer statischen Text Bezeichnung (oder Gruppenfeld Bezeichnung), die dem Steuerelement in der Aktivier Reihenfolge unmittelbar vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="9509b-138">For the following controls, Microsoft Active Accessibility ignores the window text and instead looks for a static text label (or group box label) immediately preceding the control in the tab order.</span></span>

-   <span data-ttu-id="9509b-139">Kombinations Felder</span><span class="sxs-lookup"><span data-stu-id="9509b-139">Combo Boxes</span></span>
-   <span data-ttu-id="9509b-140">Datums-und Uhrzeit-Picker</span><span class="sxs-lookup"><span data-stu-id="9509b-140">Date and Time Pickers</span></span>
-   <span data-ttu-id="9509b-141">Bearbeiten und Rich Edit-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="9509b-141">Edit and Rich Edit controls</span></span>
-   <span data-ttu-id="9509b-142">IP-Adress Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="9509b-142">IP Address controls</span></span>
-   <span data-ttu-id="9509b-143">Listenfelder</span><span class="sxs-lookup"><span data-stu-id="9509b-143">List Boxes</span></span>
-   <span data-ttu-id="9509b-144">Auflisten von Ansichten</span><span class="sxs-lookup"><span data-stu-id="9509b-144">List Views</span></span>
-   <span data-ttu-id="9509b-145">Status anzeigen</span><span class="sxs-lookup"><span data-stu-id="9509b-145">Progress Bars</span></span>
-   <span data-ttu-id="9509b-146">Bild Lauf leisten</span><span class="sxs-lookup"><span data-stu-id="9509b-146">Scrollbars</span></span>
-   <span data-ttu-id="9509b-147">Statische Steuerelemente, die das SS- \_ Symbol oder den SS- \_ bitmapstil aufweisen</span><span class="sxs-lookup"><span data-stu-id="9509b-147">Static controls that have the SS\_ICON or SS\_BITMAP style</span></span>
-   <span data-ttu-id="9509b-148">Trackbars</span><span class="sxs-lookup"><span data-stu-id="9509b-148">Trackbars</span></span>
-   <span data-ttu-id="9509b-149">Struktur Ansichten</span><span class="sxs-lookup"><span data-stu-id="9509b-149">Tree Views</span></span>

<span data-ttu-id="9509b-150">Wenn die vorangehenden Steuerelemente nicht von statischen Text Bezeichnungen begleitet werden oder die Bezeichnungen nicht ordnungsgemäß implementiert sind, kann Microsoft Active Accessibility nicht die richtige [Name-Eigenschaft](name-property.md) für Client Anwendungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9509b-150">If the preceding controls are not accompanied by static text labels, or if the labels are not implemented correctly, Microsoft Active Accessibility cannot provide the correct [Name property](name-property.md) to client applications.</span></span>

<span data-ttu-id="9509b-151">Den meisten vorangehenden Steuerelementen ist tatsächlich ein Fenster Text zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9509b-151">Most of the preceding controls actually do have associated window text.</span></span> <span data-ttu-id="9509b-152">Der Ressourcen-Editor generiert automatisch den Fenster Text, der aus einer generischen Zeichenfolge wie z. b. "Edit1" oder "listbox3" besteht.</span><span class="sxs-lookup"><span data-stu-id="9509b-152">The resource editor automatically generates the window text, which consists of a generic string such as "edit1" or "listbox3".</span></span> <span data-ttu-id="9509b-153">Obwohl Entwickler den generierten Fenster Text durch sinnvolleren Text ersetzen können, werden die meisten nie durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9509b-153">Although developers can replace the generated window text with more meaningful text, most never do.</span></span> <span data-ttu-id="9509b-154">Da der generierte Fenster Text für den Benutzer keine Bedeutung hat, wird er von Microsoft Active Accessibility ignoriert und stattdessen die zugehörige statische Text Bezeichnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9509b-154">Because the generated window text has no meaning to the user, Microsoft Active Accessibility ignores it and uses the accompanying static text label instead.</span></span>

## <a name="how-to-find-and-correct-naming-problems"></a><span data-ttu-id="9509b-155">Suchen und Beheben von Benennungs Problemen</span><span class="sxs-lookup"><span data-stu-id="9509b-155">How to Find and Correct Naming Problems</span></span>

<span data-ttu-id="9509b-156">In dem namens Eingabeformular, das unter wie falsche Benennung Probleme verursacht, besteht die Ursache der Probleme darin, dass die Aktivier Reihenfolge der Steuerelemente falsch ist.</span><span class="sxs-lookup"><span data-stu-id="9509b-156">In the name entry form shown in How Incorrect Naming Causes Problems, the cause of the problems is that the tab order of the controls is incorrect.</span></span> <span data-ttu-id="9509b-157">Wenn Sie die Benutzeroberfläche mit einem Testtool wie " [überprüfen"](inspect-objects.md) untersuchen, werden die Probleme mit der Objekthierarchie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9509b-157">Examining the UI with a testing tool such as [Inspect](inspect-objects.md) would reveal the problems with the object hierarchy.</span></span> <span data-ttu-id="9509b-158">Der folgende Screenshot zeigt die beschädigte Objekthierarchie des Namens Eingabeformulars, wie Sie in überprüfen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9509b-158">The following screen shot shows the broken object hierarchy of the name entry form as it appears in Inspect.</span></span>

![Screenshot des Überprüfungs Tools, das eine fehlerhafte Objekthierarchie des Namens Eingabeformulars anzeigt](images/incorrect-object-hierarchy.png)

<span data-ttu-id="9509b-160">Beachten Sie im vorherigen Screenshot, dass die Objekthierarchie nicht mit der Struktur der Steuerelemente identisch ist, wie Sie in der Benutzeroberfläche des Namens Eingabeformulars angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9509b-160">In the previous screen shot, notice that the object hierarchy does not match the structure of the controls as they appear in the user interface of the name entry form.</span></span> <span data-ttu-id="9509b-161">Beachten Sie auch [, dass die Überprüfung](inspect-objects.md) dem nächsten Element den falschen Namen zugewiesen hat (das Bearbeitungs Steuerelement zum Eingeben des Vornamen und sollte ein benannter Vorname sein).</span><span class="sxs-lookup"><span data-stu-id="9509b-161">Also notice that [Inspect](inspect-objects.md) has assigned the incorrect name to the next-to-last item (it is the edit control for entering the first name and should be a named "First Name:".</span></span> <span data-ttu-id="9509b-162">Beachten Sie schließlich, dass untersuchen keinen Namen für das letzte Element finden konnte (es ist das Bearbeitungs Steuerelement zum Eingeben des Nachnamen und sollte den Namen "Nachname:" aufweisen).</span><span class="sxs-lookup"><span data-stu-id="9509b-162">Finally, notice that Inspect could not find a name for the last item (it is the edit control for entering the last name and should have a name of "Last Name:".</span></span>

<span data-ttu-id="9509b-163">Das folgende Beispiel zeigt den Inhalt der Ressourcen Datei für das namens Eingabeformular.</span><span class="sxs-lookup"><span data-stu-id="9509b-163">The following example shows the contents of the resource file for the name entry form.</span></span> <span data-ttu-id="9509b-164">Beachten Sie, dass die Aktivier Reihenfolge nicht mit der logischen Struktur der Steuerelemente übereinstimmt, wie Sie in der Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9509b-164">Notice that the tab order is not consistent with the logical structure of the controls as they appear in the user interface.</span></span> <span data-ttu-id="9509b-165">Beachten Sie auch, dass für die beiden Bearbeitungs Steuerelemente keine Tastenkombinationen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9509b-165">Also notice that no shortcut keys are specified for the two edit controls.</span></span>

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
END
```

<span data-ttu-id="9509b-166">Zum Beheben der Probleme mit dem namens Eingabeformular sollte die Ressourcen Datei (. RC) bearbeitet werden, um Tastenkombinationen anzugeben, und die Steuerelemente müssen in der folgenden Reihenfolge platziert werden:</span><span class="sxs-lookup"><span data-stu-id="9509b-166">To correct the problems with the name entry form, the resource (.rc) file should be edited to specify keyboard shortcuts, and the controls should be placed in the following order:</span></span>

1.  <span data-ttu-id="9509b-167">Die statische Text Bezeichnung "&First Name:".</span><span class="sxs-lookup"><span data-stu-id="9509b-167">The "&First Name:" static text label.</span></span>
2.  <span data-ttu-id="9509b-168">Das Bearbeitungs Steuerelement für die Eingabe des Vornamen (IDC \_ Edit1).</span><span class="sxs-lookup"><span data-stu-id="9509b-168">The edit control for entering the first name (IDC\_EDIT1).</span></span>
3.  <span data-ttu-id="9509b-169">Die statische Text Bezeichnung "&Nachname:".</span><span class="sxs-lookup"><span data-stu-id="9509b-169">The "&Last Name:" static text label.</span></span>
4.  <span data-ttu-id="9509b-170">Das Bearbeitungs Steuerelement für die Eingabe des Nachnamen (IDC \_ Edit2).</span><span class="sxs-lookup"><span data-stu-id="9509b-170">The edit control for entering the last name (IDC\_EDIT2).</span></span>
5.  <span data-ttu-id="9509b-171">Die Standard-Schaltfläche "OK".</span><span class="sxs-lookup"><span data-stu-id="9509b-171">The "OK" default push button.</span></span>

<span data-ttu-id="9509b-172">Das folgende Beispiel zeigt die korrigierte Ressourcen Datei für das namens Eingabeformular:</span><span class="sxs-lookup"><span data-stu-id="9509b-172">The following example shows the corrected resource file for the name entry form:</span></span>

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```

<span data-ttu-id="9509b-173">Wenn Sie Korrekturen an einer Ressourcen Datei vornehmen möchten, können Sie entweder die Datei direkt bearbeiten, oder Sie können das Tab-Reihen folgen Tool in Microsoft Visual Studio verwenden.</span><span class="sxs-lookup"><span data-stu-id="9509b-173">To make corrections to a resource file, you can either edit the file directly, or you can use the Tab Order tool in Microsoft Visual Studio.</span></span> <span data-ttu-id="9509b-174">Sie können auf das Registerkarten-Bestell Tool in Visual Studio zugreifen, indem Sie entweder STRG + D drücken, oder indem Sie im Menü **Format** die Option **Tab-Reihenfolge** auswählen.</span><span class="sxs-lookup"><span data-stu-id="9509b-174">You can access the Tab Order tool in Visual Studio either by pressing CTRL+D, or by selecting **Tab Order** from the **Format** menu.</span></span>

<span data-ttu-id="9509b-175">Nachdem Sie die Anwendung korrigiert und neu erstellt haben, sieht die Benutzeroberfläche des Namens Eintrags Formulars wie zuvor aus.</span><span class="sxs-lookup"><span data-stu-id="9509b-175">After correcting and rebuilding the application, the UI of the names entry form will look the same as it did before.</span></span> <span data-ttu-id="9509b-176">Allerdings werden von Microsoft Active Accessibility jetzt die richtigen namens Eigenschaften für Client Anwendungen bereitgestellt, und der Fokus wird ordnungsgemäß festgelegt, wenn der Benutzer die Tastenkombinationen ALT + F oder ALT + L drückt.</span><span class="sxs-lookup"><span data-stu-id="9509b-176">However, Microsoft Active Accessibility will now provide the correct Name properties to client applications, and will set the focus correctly when the user presses the ALT+F or ALT+L keyboard shortcuts.</span></span> <span data-ttu-id="9509b-177">Über [prüfen](inspect-objects.md) wird außerdem die richtige Objekthierarchie angezeigt, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9509b-177">Also, [Inspect](inspect-objects.md) will show the correct object hierarchy, as the following screen shot shows.</span></span>

![Screenshot des Tools des zugänglichen Explorers, das eine korrekte Objekthierarchie des Namens Eingabeformulars anzeigt](images/correct-object-hierarchy.png)

## <a name="how-to-correctly-name-a-trackbar"></a><span data-ttu-id="9509b-179">So benennen Sie eine TrackBar ordnungsgemäß</span><span class="sxs-lookup"><span data-stu-id="9509b-179">How to Correctly Name a Trackbar</span></span>

<span data-ttu-id="9509b-180">Stellen Sie beim Definieren einer TrackBar (oder eines Schiebereglers) sicher, dass die statische Haupt Bezeichnung für die TrackBar vor der TrackBar angezeigt wird und dass die statischen Text Bezeichnungen für die minimalen und maximalen Bereiche nach der TrackBar angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9509b-180">When defining a trackbar (or slider), ensure that the main static text label for the trackbar appears before the trackbar, and that the static text labels for the minimum and maximum ranges appear after the trackbar.</span></span> <span data-ttu-id="9509b-181">Beachten Sie, dass Microsoft Active Accessibility die statische Text Bezeichnung verwendet, die direkt einem Steuerelement als [Name-Eigenschaft](name-property.md) für das Steuerelement vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="9509b-181">Remember that Microsoft Active Accessibility uses the static text label that immediately precedes a control as the [Name property](name-property.md) for the control.</span></span> <span data-ttu-id="9509b-182">Wenn Sie die statische Haupt Bezeichnung direkt vor der TrackBar und die anderen Bezeichnungen danach platzieren, wird sichergestellt, dass Microsoft Active Accessibility die richtige Namenseigenschaft für einen Client bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9509b-182">Placing the main static text label immediately before the trackbar, and the other labels after it, ensures that Microsoft Active Accessibility provides the correct Name property to a client.</span></span>

<span data-ttu-id="9509b-183">Die folgende Abbildung zeigt eine typische TrackBar mit einer statischen Haupt Bezeichnung namens "Geschwindigkeit" und statische Text Bezeichnungen für die minimalen ("min") und maximalen ("maximalen") Bereiche.</span><span class="sxs-lookup"><span data-stu-id="9509b-183">The following illustration shows a typical trackbar with a main static text label called "Speed", and static text labels for the minimum ("min") and maximum ("max") ranges.</span></span>

![Abbildung eines TrackBar-Steuer Elements, das über eine Haupt Bezeichnung und Bezeichnungen für die minimalen und maximalen Bereiche verfügt](images/speed-trackbar.png)

<span data-ttu-id="9509b-185">Das folgende Beispiel zeigt die korrekte Methode zum Definieren einer TrackBar und ihrer statischen Text Bezeichnungen in der Ressourcen Datei:</span><span class="sxs-lookup"><span data-stu-id="9509b-185">The following example shows the correct way to define a trackbar and its static text labels in the resource file:</span></span>

``` syntax
BEGIN
    ...

    LTEXT           "&Speed",IDC_STATIC,47,20,43,8
    CONTROL         "",IDC_SLIDER1,"msctls_trackbar32",
                    TBS_AUTOTICKS | TBS_BOTH | WS_TABSTOP,
                    32,32,62,23
    LTEXT           "min",IDC_STATIC,16,37,15,8
    LTEXT           "max",IDC_STATIC,94,38,43,8

    ...
END
```

## <a name="how-to-use-invisible-labels-to-name-controls"></a><span data-ttu-id="9509b-186">Verwenden von nicht sichtbaren Bezeichnungen zum Benennen von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="9509b-186">How to Use Invisible Labels to Name Controls</span></span>

<span data-ttu-id="9509b-187">Es ist nicht immer möglich oder wünschenswert, dass für jedes Steuerelement eine sichtbare Bezeichnung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9509b-187">It is not always possible or desirable to have a visible label for every control.</span></span> <span data-ttu-id="9509b-188">Beispielsweise kann es vorkommen, dass das Hinzufügen von Bezeichnungen unerwünschte Änderungen an der Darstellung der Benutzeroberfläche verursachen kann.</span><span class="sxs-lookup"><span data-stu-id="9509b-188">For example, sometimes adding labels can cause undesirable changes in the appearance of the UI.</span></span> <span data-ttu-id="9509b-189">In diesem Fall können Sie unsichtbare Bezeichnungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="9509b-189">In this case, you can use invisible labels.</span></span> <span data-ttu-id="9509b-190">Microsoft Active Accessibility nimmt weiterhin den Text an, der einer unsichtbaren Bezeichnung zugeordnet ist, aber die Bezeichnung wird nicht in der visuellen Benutzeroberfläche angezeigt, oder Sie wird nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="9509b-190">Microsoft Active Accessibility will still pick up the text associated with an invisible label, but the label will not appear in, or interfere with, the visual UI.</span></span>

<span data-ttu-id="9509b-191">Wie bei sichtbaren Bezeichnungen muss dem Steuerelement in der Aktivier Reihenfolge unmittelbar eine unsichtbare Bezeichnung vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9509b-191">As with visible labels, an invisible label must immediately precede the control in the tab order.</span></span> <span data-ttu-id="9509b-192">Um eine Bezeichnung in einer Ressourcen Datei (. RC) unsichtbar zu machen, fügen Sie `NOT WS_VISIBLE` oder dem Formatvorlagen `|~WS_VISIBLE` Teil des statischen Text-Steuer Elements hinzu.</span><span class="sxs-lookup"><span data-stu-id="9509b-192">To make a label invisible in a resource file (.rc), add `NOT WS_VISIBLE` or `|~WS_VISIBLE` to the style part of the static text control.</span></span> <span data-ttu-id="9509b-193">Wenn Sie den Ressourcen-Editor in Visual Studio verwenden, können Sie die Visible-Eigenschaft auf false festlegen.</span><span class="sxs-lookup"><span data-stu-id="9509b-193">If you are using the Resource Editor in Visual Studio, you can set the Visible property to False.</span></span>

## <a name="how-to-use-direct-annotation-to-specify-the-name-property"></a><span data-ttu-id="9509b-194">Verwenden der direkten Anmerkung zum Angeben der Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9509b-194">How to Use Direct Annotation to Specify the Name Property</span></span>

<span data-ttu-id="9509b-195">Die Standard Proxys, die in der Komponente Microsoft Active Accessibility Runtime enthalten sind, stellen Oleacc.dll automatisch ein [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt für alle standardmäßigen Windows-Steuerelemente bereit.</span><span class="sxs-lookup"><span data-stu-id="9509b-195">The default proxies included in the Microsoft Active Accessibility runtime component, Oleacc.dll, automatically provide an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for all of the standard Windows controls.</span></span> <span data-ttu-id="9509b-196">Wenn Sie ein standardmäßiges Windows-Steuerelement anpassen, sind die Standard Proxys am besten geeignet, um alle **IAccessible** -Eigenschaften für Ihr benutzerdefiniertes Steuerelement genau bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9509b-196">If you customize a standard Windows control, the default proxies do their best to accurately provide all of the **IAccessible** properties for your customized control.</span></span> <span data-ttu-id="9509b-197">Sie sollten ein angepasstes Steuerelement gründlich testen, um sicherzustellen, dass die Standardproxys exakte und vollständige Eigenschaftswerte</span><span class="sxs-lookup"><span data-stu-id="9509b-197">You should thoroughly test a customized control to ensure that the default proxies are providing accurate and complete property values.</span></span> <span data-ttu-id="9509b-198">Wenn beim Testen falsche oder unvollständige Eigenschaftswerte angezeigt werden, können Sie die dynamische Anmerkung-Technik mit der Bezeichnung "direkte Anmerkung" verwenden, um korrekte Eigenschaftswerte bereitzustellen und fehlende Werte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9509b-198">If testing reveals inaccurate or incomplete property values, you may be able to use the Dynamic Annotation technique called direct annotation to provide correct property values and add those that are missing.</span></span>

<span data-ttu-id="9509b-199">Beachten Sie, dass die dynamische Anmerkung nicht nur für Steuerelemente bestimmt ist, die von den Microsoft-Active Accessibility Proxys</span><span class="sxs-lookup"><span data-stu-id="9509b-199">Note that Dynamic Annotation is not just for controls supported by the Microsoft Active Accessibility proxies.</span></span> <span data-ttu-id="9509b-200">Sie können es auch verwenden, um Eigenschaften für ein beliebiges Steuerelement zu ändern oder anzugeben, das seine eigene [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9509b-200">You can also use it to modify or provide properties for any control that provides its own [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation.</span></span>

<span data-ttu-id="9509b-201">Dieser Abschnitt konzentriert sich auf die Verwendung der direkten Anmerkung, um einen korrekten Wert für die [Name-Eigenschaft](name-property.md) des [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekts für ein Steuerelement bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9509b-201">This section focuses on using direct annotation to provide a correct value for the [Name property](name-property.md) of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for a control.</span></span> <span data-ttu-id="9509b-202">Mit der direkten Anmerkung können auch andere Eigenschaftswerte bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9509b-202">You can use direct annotation to provide other properties values as well.</span></span> <span data-ttu-id="9509b-203">Außerdem sind andere dynamische Anmerkung-Techniken neben direkter Anmerkung verfügbar, und die Features und Funktionen der API für dynamische Anmerkungen werden weit über die in diesem Abschnitt beschriebenen Funktionen hinaus erweitert.</span><span class="sxs-lookup"><span data-stu-id="9509b-203">Also, other Dynamic Annotation techniques beside direct annotation are available, and the features and capabilities of the Dynamic Annotation API extend far beyond what is described in this section.</span></span> <span data-ttu-id="9509b-204">Weitere Informationen zur dynamischen Anmerkung finden Sie unter [Dynamic Annotation-API](dynamic-annotation-api.md).</span><span class="sxs-lookup"><span data-stu-id="9509b-204">For more information about Dynamic Annotation, see [Dynamic Annotation API](dynamic-annotation-api.md).</span></span>

### <a name="steps-for-annotating-the-name-property"></a><span data-ttu-id="9509b-205">Schritte zum Hinzufügen einer Anmerkung zu der Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9509b-205">Steps for Annotating the Name Property</span></span>

<span data-ttu-id="9509b-206">Die Verwendung der direkten Anmerkung zum Ändern der [Name-Eigenschaft](name-property.md) eines Steuer Elements umfasst die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="9509b-206">Using direct annotation to change the [Name Property](name-property.md) of a control involves the following steps.</span></span>

1.  <span data-ttu-id="9509b-207">Fügen Sie die folgenden Header Dateien ein:</span><span class="sxs-lookup"><span data-stu-id="9509b-207">Include the following header files:</span></span>
    -   <span data-ttu-id="9509b-208">Initguid. h</span><span class="sxs-lookup"><span data-stu-id="9509b-208">Initguid.h</span></span>
    -   <span data-ttu-id="9509b-209">Oleacc. h</span><span class="sxs-lookup"><span data-stu-id="9509b-209">Oleacc.h</span></span>

    > [!Note]  
    > <span data-ttu-id="9509b-210">Zum Definieren von GUIDs müssen Sie Initguid. h vor Oleacc. h in dieselbe Datei einschließen.</span><span class="sxs-lookup"><span data-stu-id="9509b-210">To define GUIDs, you must include Initguid.h before Oleacc.h in the same file.</span></span>

     

2.  <span data-ttu-id="9509b-211">Initialisieren Sie die Component Object Model (com)-Bibliothek, indem Sie die [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) -Funktion aufrufen, in der Regel während des Anwendungs Initialisierungs Prozesses.</span><span class="sxs-lookup"><span data-stu-id="9509b-211">Initialize the Component Object Model (COM) library by calling the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function, typically during the application initialization process.</span></span>
3.  <span data-ttu-id="9509b-212">Nachdem das Ziel Steuerelement erstellt wurde (in der Regel während der " [WM \_ InitDialog](../dlgbox/wm-initdialog.md) "-Meldung), erstellen Sie eine Instanz des Anmerkung-Managers und rufen einen Zeiger auf den [**zugehörigen IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) -Zeiger ab.</span><span class="sxs-lookup"><span data-stu-id="9509b-212">Soon after the target control is created (typically during the [WM\_INITDIALOG](../dlgbox/wm-initdialog.md) message), create an instance of the annotation manager and obtain a pointer to its [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
4.  <span data-ttu-id="9509b-213">Kommentieren Sie die [Name-Eigenschaft](name-property.md) des Ziel Steuer Elements mit der [**IAccPropServices::**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) ""-Methode.</span><span class="sxs-lookup"><span data-stu-id="9509b-213">Annotate the [Name Property](name-property.md) of the target control by using the [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) method.</span></span>

5.  <span data-ttu-id="9509b-214">Geben Sie den [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) -Zeiger frei.</span><span class="sxs-lookup"><span data-stu-id="9509b-214">Release the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
6.  <span data-ttu-id="9509b-215">Bevor das Ziel Steuerelement zerstört wird (in der Regel bei der Behandlung der WM-Lösch Nachricht), erstellen Sie eine Instanz des Anmerkung-Managers, und rufen Sie einen Zeiger auf seine [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) -Schnittstelle ab. [ \_](../winmsg/wm-destroy.md)</span><span class="sxs-lookup"><span data-stu-id="9509b-215">Before the target control is destroyed (typically when handling the [WM\_DESTROY](../winmsg/wm-destroy.md) message), create an instance of the annotation manager and obtain a pointer to its [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) interface.</span></span>
7.  <span data-ttu-id="9509b-216">Verwenden Sie die [**IAccPropServices:: clearhwnddie**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) -Methode, um die [Name-Eigenschafts](name-property.md) Anmerkungen aus dem Ziel Steuerelement zu löschen.</span><span class="sxs-lookup"><span data-stu-id="9509b-216">Use the [**IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) method to clear the [Name property](name-property.md) annotations from the target control.</span></span>
8.  <span data-ttu-id="9509b-217">Geben Sie den [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) -Zeiger frei.</span><span class="sxs-lookup"><span data-stu-id="9509b-217">Release the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
9.  <span data-ttu-id="9509b-218">Bevor die Anwendung beendet wird (in der Regel bei der Verarbeitung der WM-Lösch Nachricht), müssen Sie die com-Bibliothek freigeben, indem Sie die Funktion " [count](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) " aufrufen [ \_ ](../winmsg/wm-destroy.md)</span><span class="sxs-lookup"><span data-stu-id="9509b-218">Before your application exits (typically while processing the [WM\_DESTROY](../winmsg/wm-destroy.md) message), release the COM library by calling the [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>

<span data-ttu-id="9509b-219">Die [**IAccPropServices::-Funktion der Funktion "IAccPropServices::**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) " erfordert fünf Parameter.</span><span class="sxs-lookup"><span data-stu-id="9509b-219">The [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) function takes five parameters.</span></span> <span data-ttu-id="9509b-220">Die ersten drei –*HWND*, *idobject* und *idchild*– werden kombiniert, um das Steuerelement zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9509b-220">The first three—*hwnd*, *idObject*, and *idChild*—combine to identify the control.</span></span> <span data-ttu-id="9509b-221">Der vierte Parameter, *idProp*, gibt den Bezeichner der Eigenschaft an, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9509b-221">The fourth parameter, *idProp*, specifies the identifier of the property to be changed.</span></span> <span data-ttu-id="9509b-222">Um die [Name-Eigenschaft](name-property.md)zu ändern, legen Sie *idProp* auf den **\_ \_ Namen des PROPID-ACC** fest.</span><span class="sxs-lookup"><span data-stu-id="9509b-222">To change the [Name property](name-property.md), set *idProp* to **PROPID\_ACC\_NAME**.</span></span> <span data-ttu-id="9509b-223">(Eine Liste mit anderen Eigenschaften, die Sie über die direkte Anmerkung festlegen können, finden Sie unter [Verwenden der direkten](using-direct-annotation.md)Anmerkung.) Der letzte Parameter von " **ssthwndpropstr**, *Str*" ist die neue Zeichenfolge, die als "Name"-Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9509b-223">(For a list of other properties that you can set through direct annotation, see [Using Direct Annotation](using-direct-annotation.md).) The last parameter of **SetHwndPropStr**, *str*, is the new string to use as the Name property.</span></span>

### <a name="example-of-annotating-the-name-property"></a><span data-ttu-id="9509b-224">Beispiel für das kommentieren der Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9509b-224">Example of Annotating the Name Property</span></span>

<span data-ttu-id="9509b-225">Der folgende Beispielcode zeigt, wie Sie mit der direkten Anmerkung die [Name-Eigenschaft](name-property.md) des [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekts für ein-Steuerelement ändern können.</span><span class="sxs-lookup"><span data-stu-id="9509b-225">The following example code shows how to use direct annotation to change the [Name property](name-property.md) of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for a control.</span></span> <span data-ttu-id="9509b-226">Um dies zu gewährleisten, wird im Beispiel eine hart codierte Zeichenfolge ("neuer Steuerelement Name") verwendet, um die Name-Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9509b-226">To keep things simple, the example uses a hard-coded string ("New Control Name") to set the Name property.</span></span> <span data-ttu-id="9509b-227">Hart codierte Zeichen folgen sollten nicht in der endgültigen Version der Anwendung verwendet werden, da Sie nicht lokalisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="9509b-227">Hard-coded strings should not be used in the final version of your application because they cannot be localized.</span></span> <span data-ttu-id="9509b-228">Laden Sie stattdessen Zeichen folgen immer aus der Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="9509b-228">Instead, always load strings from your resource file.</span></span> <span data-ttu-id="9509b-229">Das Beispiel zeigt auch nicht die Aufrufe der Funktionen [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [zählinitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="9509b-229">Also, the example does not show the calls to the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) functions.</span></span>


```C++
#include <initguid.h>
#include <oleacc.h>

// AnnotateControlName - Uses direct annotation to change the Name property 
// of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose Name property is to be changed.
HRESULT AnnotateControlName(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;        

    IAccPropServices *pAccPropSvc = NULL;  

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Set the Name property for the control.
    // Note: A hard-coded string is used here to keep the example simple.
    // Always use localizable string resources in your applications. 
    hr = pAccPropSvc->SetHwndPropStr(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        PROPID_ACC_NAME, L"New Control Name");

    pAccPropSvc->Release();
    
    return hr;
}

// RemoveAnnotatedNameFromControl - Removes the annotated name from the 
// Name property of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose annotated name is to be removed.
HRESULT RemoveAnnotatedNameFromControl(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;

    IAccPropServices *pAccPropSvc = NULL;

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Remove the annotated name from the Name property for the control.
    MSAAPROPID propid = PROPID_ACC_NAME;
    hr = pAccPropSvc->ClearHwndProps(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        &propid, 1);

    // Release the annotation manager.
    pAccPropSvc->Release();

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="9509b-230">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9509b-230">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9509b-231">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9509b-231">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9509b-232">Dynamic-Annotation-API</span><span class="sxs-lookup"><span data-stu-id="9509b-232">Dynamic Annotation API</span></span>](dynamic-annotation-api.md)
</dt> <dt>

[<span data-ttu-id="9509b-233">Bereitstellen der Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9509b-233">Providing the Name Property</span></span>](providing-the-name-property.md)
</dt> <dt>

[<span data-ttu-id="9509b-234">TestTools</span><span class="sxs-lookup"><span data-stu-id="9509b-234">Testing Tools</span></span>](testing-tools.md)
</dt> </dl>

 

 