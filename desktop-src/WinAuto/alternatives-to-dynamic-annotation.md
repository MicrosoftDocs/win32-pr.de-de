---
title: Alternativen zu dynamischer Anmerkung
description: Alternativen zu dynamischer Anmerkung
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0027cf9a9913efdff379d2f0c01e7bf22bc94f44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101883"
---
# <a name="alternatives-to-dynamic-annotation"></a><span data-ttu-id="58c90-103">Alternativen zu dynamischer Anmerkung</span><span class="sxs-lookup"><span data-stu-id="58c90-103">Alternatives to Dynamic Annotation</span></span>

<span data-ttu-id="58c90-104">Es gibt weitere Möglichkeiten, angepasste [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Unterstützung für Benutzeroberflächen Elemente bereitzustellen, und in einigen Fällen sind Sie die richtige Lösung.</span><span class="sxs-lookup"><span data-stu-id="58c90-104">There are other ways to provide customized [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support for UI elements, and in some cases, they are the correct solution.</span></span> <span data-ttu-id="58c90-105">Vor der dynamischen Anmerkung waren diese alternativen Techniken die einzigen Optionen, die Entwicklern zur Verfügung standen.</span><span class="sxs-lookup"><span data-stu-id="58c90-105">Prior to Dynamic Annotation, these alternative techniques were the only options available to developers.</span></span> <span data-ttu-id="58c90-106">Dazu gehört das Implementieren der gesamten **IAccessible** -Schnittstelle und der programmgesteuerten Techniken.</span><span class="sxs-lookup"><span data-stu-id="58c90-106">They include implementing all of the **IAccessible** interface and programmatic techniques.</span></span>

## <a name="implementing-all-of-the-iaccessible-interface"></a><span data-ttu-id="58c90-107">Implementieren der gesamten IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="58c90-107">Implementing All of the IAccessible Interface</span></span>

<span data-ttu-id="58c90-108">Eine alternative Methode besteht darin, die gesamte [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="58c90-108">One alternative technique is to implement all of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="58c90-109">Diese Vorgehensweise ist häufig für benutzerdefinierte Steuerelemente oder völlig unterschiedliche Elemente der Benutzeroberfläche erforderlich. die Entwicklungs-und Testkosten sind jedoch so groß, dass Sie nur vermieden werden sollten, wenn es wirklich notwendig ist.</span><span class="sxs-lookup"><span data-stu-id="58c90-109">This approach is often necessary for custom controls or radically different UI elements; however, the development and test costs are significant enough that it should be avoided unless truly necessary.</span></span> <span data-ttu-id="58c90-110">Wenn das Ziel darin besteht, eine einzelne Eigenschaft zu ändern, ist es schwierig, die Kosten zu rechtfertigen.</span><span class="sxs-lookup"><span data-stu-id="58c90-110">If the goal is to modify a single property, the cost is difficult to justify.</span></span>

## <a name="programmatic-techniques"></a><span data-ttu-id="58c90-111">Programmgesteuerte Techniken</span><span class="sxs-lookup"><span data-stu-id="58c90-111">Programmatic Techniques</span></span>

<span data-ttu-id="58c90-112">Eine andere Möglichkeit besteht darin, die Informationen, die für eine bestimmte Eigenschaft verfügbar gemacht werden, mithilfe von Unterklassen und Wrapping Techniken zu ändern.</span><span class="sxs-lookup"><span data-stu-id="58c90-112">Another option is to use subclassing and wrapping techniques to modify the information being exposed for a specific property.</span></span> <span data-ttu-id="58c90-113">Dies ist die Technik, die durch die dynamische Anmerkung ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="58c90-113">This is the technique that Dynamic Annotation is intended to replace.</span></span> <span data-ttu-id="58c90-114">Um eine einzelne Eigenschaft mithilfe von Unterklassen und Wrapping zu überschreiben, muss der Entwickler die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="58c90-114">To override a single property by using subclassing and wrapping, the developer must perform the following steps:</span></span>

1.  <span data-ttu-id="58c90-115">Unterklasse das HWND des [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="58c90-115">Subclass the HWND of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object.</span></span>
2.  <span data-ttu-id="58c90-116">Fangen Sie die [**WM- \_ GetObject**](wm-getobject.md) -Nachricht für den korrekten IParam/objID-Wert ab.</span><span class="sxs-lookup"><span data-stu-id="58c90-116">Intercept the [**WM\_GETOBJECT**](wm-getobject.md) message for the correct IParam/OBJID value.</span></span>
3.  <span data-ttu-id="58c90-117">Leiten Sie die [**WM \_ GetObject**](wm-getobject.md) -Nachricht mithilfe der [*callwndproc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) -Funktion an die Basisklasse weiter.</span><span class="sxs-lookup"><span data-stu-id="58c90-117">Forward the [**WM\_GETOBJECT**](wm-getobject.md) message to the base class using the [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) function.</span></span> <span data-ttu-id="58c90-118">Wenn 0 (null) zurückgegeben wird, aufrufen Sie " [**foratestdaccessibleobject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); Rufen Sie andernfalls [**lresultfrobobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) für den zurückgegebenen Wert auf, um den nativen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger des Steuer Elements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="58c90-118">If zero is returned, call [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); otherwise, call [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) on the returned value to obtain the control's native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>
4.  <span data-ttu-id="58c90-119">Erstellen Sie eine Wrapper Klasse, die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementiert und den **IAccessible** -Schnittstellen Zeiger umschließt, der aus dem vorherigen Schritt zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="58c90-119">Create a wrapper class, which implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and wraps the **IAccessible** interface pointer returned from the previous step.</span></span> <span data-ttu-id="58c90-120">Diese Wrapper Klasse sendet alle Methoden und Eigenschaften an den ursprünglichen **IAccessible** -Schnittstellen Zeiger, mit Ausnahme derjenigen, die überschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="58c90-120">This wrapper class sends all methods and properties to the original **IAccessible** interface pointer, except those that are to be overridden.</span></span> <span data-ttu-id="58c90-121">Dies umfasst das Schreiben von Weiterleitungs Code für alle 21 Eigenschaften und Methoden der **IAccessible** -Schnittstelle, unabhängig davon, wie viele tatsächlich überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="58c90-121">This involves writing forwarding code for all of the **IAccessible** interface's 21 properties and methods, regardless of how many are actually overridden.</span></span>

<span data-ttu-id="58c90-122">Außerdem müssen Entwickler die folgenden Bedingungen überprüfen:</span><span class="sxs-lookup"><span data-stu-id="58c90-122">Also, developers must verify the following conditions:</span></span>

-   <span data-ttu-id="58c90-123">Die überschriebene Methode oder Eigenschaft darf nur die erforderlichen untergeordneten IDs verarbeiten und alle anderen an den ursprünglichen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="58c90-123">The overridden method or property must only handle the required child IDs, and forward all others to the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>
-   <span data-ttu-id="58c90-124">Beim umwickeln müssen auch [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) -und [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) -Schnittstellen weiterleiten, wenn Sie vom ursprünglichen Objekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="58c90-124">Wrapping must also forward [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) and [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) interfaces only if the original object supports them.</span></span>
-   <span data-ttu-id="58c90-125">Die Verweis Zählung muss korrekt gehandhabt werden, insbesondere, wenn andere Schnittstellen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="58c90-125">Reference counting must be handled correctly, especially if other interfaces are supported.</span></span>
-   <span data-ttu-id="58c90-126">[**IDispatch**](idispatch-interface.md) -Rückgabewerte müssen ordnungsgemäß behandelt werden, insbesondere bei der [**ITypeInfo:: Aufrufen**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) -Methode, die mit einem Schnittstellen Zeiger auf die Wrapper Schnittstelle aufgerufen werden muss, nicht mit einem Zeiger auf die ursprüngliche [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="58c90-126">[**IDispatch**](idispatch-interface.md) return values must be handled correctly, especially with the [**ITypeInfo::Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) method, which must be called with an interface pointer to the wrapper interface, not a pointer to the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span>

<span data-ttu-id="58c90-127">Diese Techniken erfordern eine beträchtliche Menge an Arbeit, auch wenn nur eine oder zwei Eigenschaften überschrieben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="58c90-127">These techniques require a considerable amount of work, even if only one or two properties need to be overridden.</span></span> <span data-ttu-id="58c90-128">Der Großteil des resultierenden Codes beschäftigt sich mit dem Unterklassen-und Wrapping Vorgang, und nur ein kleiner Bruchteil bietet tatsächlich die überschriebenen Informationen an.</span><span class="sxs-lookup"><span data-stu-id="58c90-128">The majority of the resulting code is concerned with subclassing and wrapping, and only a small fraction is actually providing the overridden information.</span></span>

<span data-ttu-id="58c90-129">Es gibt jedoch Szenarios, in denen diese Techniken benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="58c90-129">However, there are scenarios in which these techniques are needed.</span></span> <span data-ttu-id="58c90-130">Wenn Sie z. b. strukturelle Änderungen vornehmen, um ein Platzhalter-Benutzeroberflächen Element zu erstellen, sollten Sie diese Techniken anstelle der dynamischen Anmerkung verwenden.</span><span class="sxs-lookup"><span data-stu-id="58c90-130">For example, if you are making structural changes to create a placeholder UI element, then you should use these techniques rather than Dynamic Annotation.</span></span>

## <a name="fixing-names-derived-from-labels"></a><span data-ttu-id="58c90-131">Von Bezeichnungen abgeleitete Namen werden repariert.</span><span class="sxs-lookup"><span data-stu-id="58c90-131">Fixing Names Derived from Labels</span></span>

<span data-ttu-id="58c90-132">Einige allgemeine Microsoft Win32-Steuerelemente, wie z. b. das Bearbeitungsfeld-Steuerelement, werden fast immer mit einer Bezeichnung (einem LTEXT-Eintrag in der Ressourcen Datei) oder einem Gruppenfeld (GroupBox in der Ressourcen Datei) verwendet.</span><span class="sxs-lookup"><span data-stu-id="58c90-132">Some Microsoft Win32 common controls, such as the edit box control, are nearly always used with a label (an LTEXT entry in the resource file) or a group box (GROUPBOX in the resource file).</span></span> <span data-ttu-id="58c90-133">Die Name-Eigenschaft des Steuer Elements wird von Microsoft Active Accessibility automatisch von der Bezeichnung abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="58c90-133">Microsoft Active Accessibility automatically derives the name property of the control from its label.</span></span> <span data-ttu-id="58c90-134">Bei solchen Steuerelementen wird der Fenster Text (in Microsoft Visual Studio als Name oder ID-Eigenschaft angezeigt) ignoriert, da er in der Regel automatisch generiert und selten sehr beschreibend ist. Beispiel: "IDC \_ Edit1".</span><span class="sxs-lookup"><span data-stu-id="58c90-134">For such controls, the window text (shown in Microsoft Visual Studio as the Name or ID property) is ignored, because it is usually autogenerated and seldom very descriptive; for example, "IDC\_EDIT1".</span></span>

<span data-ttu-id="58c90-135">Wenn die Benutzeroberfläche der Anwendung nicht ordnungsgemäß entworfen wurde, kann Microsoft Active Accessibility den Namen möglicherweise nicht ordnungsgemäß festlegen.</span><span class="sxs-lookup"><span data-stu-id="58c90-135">If the user interface of the application is not designed correctly, Microsoft Active Accessibility might not be able to set the name correctly.</span></span> <span data-ttu-id="58c90-136">Um einem-Steuerelement zugeordnet zu werden, muss die Bezeichnung oder das Gruppenfeld direkt vor dem dynamischen Steuerelement in der Aktivier Reihenfolge platziert werden.</span><span class="sxs-lookup"><span data-stu-id="58c90-136">To be associated with a control, the label or group box must be placed immediately before the dynamic control in the tab order.</span></span>

<span data-ttu-id="58c90-137">Die Aktivier Reihenfolge kann geändert werden, indem Sie das Tool in Visual Studio verwenden (im Menü **Format** , wenn der Ressourcen-Editor geöffnet ist), oder indem Sie die Ressourcen Datei direkt bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="58c90-137">Tab order can be changed by using the tool in Visual Studio (on the **Format** menu when the resource editor is open) or by directly editing the resource file.</span></span>

<span data-ttu-id="58c90-138">Das folgende Beispiel zeigt die Beschreibung eines Dialog Felds einer Ressourcen Datei, das zwei beschriftete Bearbeitungsfelder enthält.</span><span class="sxs-lookup"><span data-stu-id="58c90-138">The following example shows a resource file's description of a dialog box that contains two labeled edit boxes.</span></span>


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
END
```



<span data-ttu-id="58c90-139">In diesem Beispiel werden die Bezeichnungen und Steuerelemente nicht in der richtigen Aktivier Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="58c90-139">In this example, the labels and controls are not listed in the correct tab order.</span></span> <span data-ttu-id="58c90-140">Demzufolge weist Microsoft Active Accessibility den Namen "Nachname" dem Eingabefeld "First-Name" und dem Bearbeitungsfeld "Last Name" überhaupt keinen Namen zu.</span><span class="sxs-lookup"><span data-stu-id="58c90-140">As a result, Microsoft Active Accessibility assigns the name "Last Name" to the first-name edit box, and no name at all to the last-name edit box.</span></span>

<span data-ttu-id="58c90-141">Das folgende Beispiel zeigt die richtige Ressourcen Auflistung.</span><span class="sxs-lookup"><span data-stu-id="58c90-141">The following example shows the correct resource listing.</span></span> <span data-ttu-id="58c90-142">Beachten Sie auch, dass die Tastenkombination in den Bezeichnungen festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="58c90-142">Note also that shortcut keys have been designated in the labels.</span></span>


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```



<span data-ttu-id="58c90-143">Wenn Steuerelemente über ergänzende Bezeichnungen verfügen, z. b. für Mindest-und Höchstwerte auf einer TrackBar, sollten diese Bezeichnungen nach dem-Steuerelement in der Aktivier Reihenfolge platziert werden.</span><span class="sxs-lookup"><span data-stu-id="58c90-143">When controls have supplementary labels, such as for minimum and maximum values on a trackbar, these labels should be placed after the control in the tab order.</span></span> <span data-ttu-id="58c90-144">Die Haupt Bezeichnung des Steuer Elements muss direkt vor dem Steuerelement selbst angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="58c90-144">The main label of the control must appear immediately before the control itself.</span></span>

## <a name="naming-controls-without-labels"></a><span data-ttu-id="58c90-145">Benennen von Steuerelementen ohne Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="58c90-145">Naming Controls Without Labels</span></span>

<span data-ttu-id="58c90-146">Es ist nicht immer möglich oder wünschenswert, dass für jedes Steuerelement eine sichtbare Bezeichnung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="58c90-146">It is not always possible or desirable to have a visible label for every control.</span></span> <span data-ttu-id="58c90-147">Sie können jedoch weiterhin einen Namen für das Steuerelement angeben, indem Sie eine unsichtbare Bezeichnung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="58c90-147">However, you can still provide a name for the control by adding an invisible label.</span></span> <span data-ttu-id="58c90-148">Wie immer muss die unsichtbare Bezeichnung unmittelbar vor dem-Steuerelement in der Aktivier Reihenfolge stehen.</span><span class="sxs-lookup"><span data-stu-id="58c90-148">As always, the invisible label must immediately precede the control in the tab order.</span></span>

<span data-ttu-id="58c90-149">Wenn Sie den Ressourcen-Editor in Microsoft Visual Studio .NET verwenden, können Sie die Visible-Eigenschaft auf false festlegen.</span><span class="sxs-lookup"><span data-stu-id="58c90-149">If you are using the Resource Editor in Microsoft Visual Studio .NET, you can set the Visible property to False.</span></span> <span data-ttu-id="58c90-150">Um die Bezeichnung beim Bearbeiten der Ressourcen Datei (RC) unsichtbar zu machen, fügen Sie Not WS \_ Visible oder den Formatvorlagen Teil des Label-Steuer Elements hinzu, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="58c90-150">To make the label invisible when editing the resource file (.rc), add NOT WS\_VISIBLE or to the style part of the label control, as shown in the following example.</span></span>


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



<span data-ttu-id="58c90-151">Beachten Sie, dass alle festgelegten Tastenkombinationen funktionieren, auch wenn die Bezeichnung unsichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="58c90-151">Note that any designated shortcut key works even though the label is invisible.</span></span>

 

 