---
title: Ändern der Echo Dialog-Ressource
description: Ändern der Echo Dialog-Ressource
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Windows Media Player-Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample-Eigenschaften Seiten
- DSP-Plug-ins, Echo Sample-Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Dialog Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09caa800376a7962a11912bc582a091f0de52c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310644"
---
# <a name="modifying-the-echo-dialog-resource"></a><span data-ttu-id="c7549-109">Ändern der Echo Dialog-Ressource</span><span class="sxs-lookup"><span data-stu-id="c7549-109">Modifying the Echo Dialog Resource</span></span>

<span data-ttu-id="c7549-110">Sie müssen die Dialogfeld Ressource ändern, bei der es sich um die Benutzeroberfläche des Eigenschaften Seiten Objekts handelt.</span><span class="sxs-lookup"><span data-stu-id="c7549-110">You need to change the dialog resource that is the user interface for the property page object.</span></span> <span data-ttu-id="c7549-111">Sie können zuerst das vorhandene Bearbeitungsfeld und die Bezeichnung so ändern, dass Sie für die Eigenschaft Verzögerungszeit nützlich sind, und dann ein zweites Bearbeitungsfeld und eine Bezeichnung für die Eigenschaft "nass Mischung" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c7549-111">You can first change the existing edit box and label to be useful for the delay time property and then add a second edit box and label for the wet mix property.</span></span>

<span data-ttu-id="c7549-112">So bearbeiten Sie die Dialog Ressource in Visual C++:</span><span class="sxs-lookup"><span data-stu-id="c7549-112">To edit the dialog resource in Visual C++:</span></span>

1.  <span data-ttu-id="c7549-113">Klicken Sie im Projekt Arbeitsbereich auf die Registerkarte **resourceview** .</span><span class="sxs-lookup"><span data-stu-id="c7549-113">Click the **ResourceView** tab in the Project Workspace.</span></span>
2.  <span data-ttu-id="c7549-114">Erweitern Sie die strukturressourcen, indem Sie den Ordner auf oberster Ebene öffnen.</span><span class="sxs-lookup"><span data-stu-id="c7549-114">Expand the resources tree by opening the top level folder.</span></span>
3.  <span data-ttu-id="c7549-115">Öffnen Sie den **Dialog** Ordner.</span><span class="sxs-lookup"><span data-stu-id="c7549-115">Open the **Dialog** folder.</span></span>
4.  <span data-ttu-id="c7549-116">Doppelklicken Sie auf den Ressourcennamen des Dialog Felds, IDD \_ echoproppage.</span><span class="sxs-lookup"><span data-stu-id="c7549-116">Double-click the dialog resource name, IDD\_ECHOPROPPAGE.</span></span> <span data-ttu-id="c7549-117">Der Ressourcen-Editor wird im rechten Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c7549-117">The resource editor appears in the right pane.</span></span>

## <a name="changing-the-existing-resources"></a><span data-ttu-id="c7549-118">Ändern der vorhandenen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c7549-118">Changing the Existing Resources</span></span>

<span data-ttu-id="c7549-119">So ändern Sie die vorhandenen Eigenschaften Seiten Ressourcen für die Eigenschaft Verzögerungszeit:</span><span class="sxs-lookup"><span data-stu-id="c7549-119">To change the existing property page resources for the delay time property:</span></span>

1.  <span data-ttu-id="c7549-120">Ändern Sie zunächst den Text im vorhandenen statischen Text Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c7549-120">First, change the text in the existing static text control.</span></span> <span data-ttu-id="c7549-121">Klicken Sie mit der rechten Maustaste auf das Steuerelement und dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="c7549-121">Right-click the control and then choose **Properties**.</span></span> <span data-ttu-id="c7549-122">Geben Sie im Feld **Beschriftung** die neue Beschriftung ein:</span><span class="sxs-lookup"><span data-stu-id="c7549-122">In the **Caption** field, type the new caption:</span></span>
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  <span data-ttu-id="c7549-123">Schließen Sie das Dialogfeld Text Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c7549-123">Close the Text Properties dialog box.</span></span>
3.  <span data-ttu-id="c7549-124">Ändern Sie nun den Namen des Steuer Elements "Bearbeitungsfeld".</span><span class="sxs-lookup"><span data-stu-id="c7549-124">Now, change the name of the edit box control.</span></span> <span data-ttu-id="c7549-125">Klicken Sie hierzu mit der rechten Maustaste auf das Steuerelement, und wählen Sie dann **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="c7549-125">To do this, right-click the control and then choose **Properties**.</span></span> <span data-ttu-id="c7549-126">Geben Sie im Feld **ID** einen neuen Namen für das Steuerelement ein:</span><span class="sxs-lookup"><span data-stu-id="c7549-126">In the **ID** field, type a new name for the control:</span></span>
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  <span data-ttu-id="c7549-127">Schließen Sie das Dialogfeld Eigenschaften bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c7549-127">Close the Edit Properties dialog box.</span></span>
5.  <span data-ttu-id="c7549-128">Speichern Sie die Ressource.</span><span class="sxs-lookup"><span data-stu-id="c7549-128">Save the resource.</span></span>
6.  <span data-ttu-id="c7549-129">**Ja** , wenn Sie aufgefordert werden, die Datei "Resource. h" erneut zu laden</span><span class="sxs-lookup"><span data-stu-id="c7549-129">Answer **Yes** if prompted to reload the file resource.h.</span></span>
7.  <span data-ttu-id="c7549-130">Klicken Sie im Projekt Arbeitsbereich auf die Registerkarte **fileview** .</span><span class="sxs-lookup"><span data-stu-id="c7549-130">Click the **FileView** tab in the Project Workspace.</span></span> <span data-ttu-id="c7549-131">Ressource öffnen. h</span><span class="sxs-lookup"><span data-stu-id="c7549-131">Open resource.h</span></span>
8.  <span data-ttu-id="c7549-132">Suchen \# Sie die Ressource für das Bearbeitungsfeld für den Skalierungsfaktor (IDC \_ scalefactor), und löschen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="c7549-132">Locate the \#define for the scale factor edit box resource (IDC\_SCALEFACTOR) and delete it.</span></span> <span data-ttu-id="c7549-133">Er muss dieselbe ID-Nummer wie IDC \_ Delta Time aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c7549-133">It should have the same id number as IDC\_DELAYTIME.</span></span>

## <a name="adding-the-new-resources"></a><span data-ttu-id="c7549-134">Hinzufügen der neuen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c7549-134">Adding the New Resources</span></span>

<span data-ttu-id="c7549-135">Zum Hinzufügen der neuen Eigenschaften Seiten Ressourcen für die Eigenschaft "nass Mischung":</span><span class="sxs-lookup"><span data-stu-id="c7549-135">To add the new property page resources for the wet mix property:</span></span>

1.  <span data-ttu-id="c7549-136">Klicken Sie im Projekt Arbeitsbereich auf die Registerkarte **resourceview** , um Sie auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c7549-136">Click the **ResourceView** tab in the Project Workspace to select it.</span></span>
2.  <span data-ttu-id="c7549-137">Doppelklicken Sie auf den Namen des Dialog Felds Eigenschaften Seite, IDD \_ echoproppage.</span><span class="sxs-lookup"><span data-stu-id="c7549-137">Double-click the name of the property page dialog box, IDD\_ECHOPROPPAGE.</span></span> <span data-ttu-id="c7549-138">Der Ressourcen-Editor wird im rechten Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c7549-138">The resource editor appears in the right pane.</span></span>
3.  <span data-ttu-id="c7549-139">Verwenden Sie die Toolbox, um der Eigenschaften Seite ein statisches Text Steuerelement und ein Bearbeitungsfeld hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c7549-139">Use the toolbox to add a static text control and an edit box to the property page.</span></span>
4.  <span data-ttu-id="c7549-140">Klicken Sie mit der rechten Maustaste auf das statische Text Steuerelement, **und wählen Sie**</span><span class="sxs-lookup"><span data-stu-id="c7549-140">Right-click the static text control and choose **Properties**.</span></span>
5.  <span data-ttu-id="c7549-141">Geben Sie im Feld **ID** einen neuen Namen für das statische Text Steuerelement ein:</span><span class="sxs-lookup"><span data-stu-id="c7549-141">Type a new name for the static text control in the **ID** field:</span></span>
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  <span data-ttu-id="c7549-142">Geben Sie eine Beschriftung für die Bezeichnung ein:</span><span class="sxs-lookup"><span data-stu-id="c7549-142">Type a caption for the label:</span></span>
    ```C++
    Effect level (%):
    
    ```

    

7.  <span data-ttu-id="c7549-143">Schließen Sie das Dialogfeld Text Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c7549-143">Close the Text Properties dialog box.</span></span>
8.  <span data-ttu-id="c7549-144">Klicken Sie mit der rechten Maustaste, und wählen Sie **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="c7549-144">Right-click the edit box and choose **Properties**.</span></span>
9.  <span data-ttu-id="c7549-145">Geben Sie im Feld **ID** einen neuen Namen für das Bearbeitungsfeld ein:</span><span class="sxs-lookup"><span data-stu-id="c7549-145">Type a new name for the edit box in the **ID** field:</span></span>
    ```C++
    IDC_WETMIX
    
    ```

    

10. <span data-ttu-id="c7549-146">Schließen Sie das Dialogfeld Eigenschaften bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c7549-146">Close the Edit Properties dialog box.</span></span>

<span data-ttu-id="c7549-147">Wenn Sie das Projekt speichern, werden Sie möglicherweise aufgefordert, "Resource. h" neu zu laden.</span><span class="sxs-lookup"><span data-stu-id="c7549-147">When you save the project, you may be prompted to reload resource.h.</span></span> <span data-ttu-id="c7549-148">Klicken Sie in diesem Fall auf **Ja** .</span><span class="sxs-lookup"><span data-stu-id="c7549-148">Click **Yes** if this happens.</span></span> <span data-ttu-id="c7549-149">Der Ressourcen-Editor des Dialog Felds sollte "Resource. h" die Ressourcennamen und ID-Nummern für die hinzugefügten Elemente hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c7549-149">The dialog box resource editor should add the resource names and id numbers to resource.h for the items you added.</span></span> <span data-ttu-id="c7549-150">Wenn dies nicht der Fall ist, müssen Sie "Resource. h" öffnen und neue Einträge für das Steuerelement "Bezeichnung" und "Bearbeitungsfeld" eingeben und jedem eine eindeutige ID-Nummer zuweisen.</span><span class="sxs-lookup"><span data-stu-id="c7549-150">If for some reason this doesn't happen, you must open resource.h and type new entries for the label and edit box control, and assign each a unique id number.</span></span>

## <a name="modifying-and-adding-the-string-resources"></a><span data-ttu-id="c7549-151">Ändern und Hinzufügen der Zeichen folgen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c7549-151">Modifying and Adding the String Resources</span></span>

<span data-ttu-id="c7549-152">Der Beispielcode des Plug-in-Assistenten gibt eine Zeichen folgen Ressource mit dem Namen IDs \_ scalerangeerror an, die eine Meldung enthält, die angezeigt wird, wenn die Benutzereingabe außerhalb des gültigen Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="c7549-152">The plug-in wizard sample code specifies a string resource named IDS\_SCALERANGEERROR that contains a message to display when the user input is out of range.</span></span> <span data-ttu-id="c7549-153">Sie können diese Ressource so ändern, dass Sie Ihren Anforderungen für den Wert für Verzögerungszeit entspricht, indem Sie die folgenden Schritte in Visual C++ ausführen:</span><span class="sxs-lookup"><span data-stu-id="c7549-153">You can modify this resource to suit your needs for the delay time value by following these steps in Visual C++:</span></span>

1.  <span data-ttu-id="c7549-154">Klicken Sie auf die Registerkarte **resourceview** .</span><span class="sxs-lookup"><span data-stu-id="c7549-154">Click the **ResourceView** tab.</span></span>
2.  <span data-ttu-id="c7549-155">Öffnen Sie den Zeichen folgen- **Tabellen** Ordner.</span><span class="sxs-lookup"><span data-stu-id="c7549-155">Open the **String Table** folder.</span></span>
3.  <span data-ttu-id="c7549-156">Doppelklicken Sie auf das Symbol **Zeichen folgen Tabelle** , um den Ressourcen-Editor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c7549-156">Double-click the **String Table** icon to open the resource editor.</span></span>
4.  <span data-ttu-id="c7549-157">Doppelklicken Sie auf den Namen der Ressource, die Sie bearbeiten möchten, in diesem Fall IDs \_ scalerangeerror.</span><span class="sxs-lookup"><span data-stu-id="c7549-157">Double-click the name of the resource you want to edit, in this case, IDS\_SCALERANGEERROR.</span></span> <span data-ttu-id="c7549-158">Das Dialogfeld Zeichen folgen Eigenschaften wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c7549-158">The String Properties dialog box appears.</span></span>
5.  <span data-ttu-id="c7549-159">Ändern Sie den Namen im Feld ID in IDs Delta- **ID** - \_ Fehler.</span><span class="sxs-lookup"><span data-stu-id="c7549-159">Change the name in the **ID** field to IDS\_DELAYRANGEERROR.</span></span>
6.  <span data-ttu-id="c7549-160">Ändern Sie den Text im **Beschriftungs** Feld:</span><span class="sxs-lookup"><span data-stu-id="c7549-160">Change the text in the **Caption** field:</span></span>
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  <span data-ttu-id="c7549-161">Schließen Sie das Dialogfeld Zeichen folgen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c7549-161">Close the String Properties dialog box.</span></span>

<span data-ttu-id="c7549-162">Fügen Sie als nächstes eine neue Zeichen folgen Ressource für die Fehlermeldung der nass Mischungs Eigenschaft hinzu.</span><span class="sxs-lookup"><span data-stu-id="c7549-162">Next, add a new string resource for the wet mix property error message.</span></span>

1.  <span data-ttu-id="c7549-163">Doppelklicken Sie auf die leere Zeile am unteren Rand des Ressourcen-Editors.</span><span class="sxs-lookup"><span data-stu-id="c7549-163">Double-click the empty line at the bottom of the resource editor.</span></span>
2.  <span data-ttu-id="c7549-164">Ändern Sie den Namen im Feld **ID** in IDs \_ mixrangeerror.</span><span class="sxs-lookup"><span data-stu-id="c7549-164">Change the name in the **ID** field to IDS\_MIXRANGEERROR.</span></span>
3.  <span data-ttu-id="c7549-165">Fügen Sie dem **Beschriftungs** Feld den folgenden Text hinzu:</span><span class="sxs-lookup"><span data-stu-id="c7549-165">Add the following text to the **Caption** field:</span></span>
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  <span data-ttu-id="c7549-166">Schließen Sie das Dialogfeld Zeichen folgen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c7549-166">Close the String Properties dialog box.</span></span>

<span data-ttu-id="c7549-167">Es gibt zwei weitere Werte, die Sie in der Zeichen folgen Tabelle ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="c7549-167">There are two other values you will want to change in the String Table.</span></span> <span data-ttu-id="c7549-168">IDs \_ FriendlyName ist der Name, der in der Windows Media Player-Benutzeroberfläche angezeigt wird, um das Plug-in zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c7549-168">IDS\_FRIENDLYNAME is the name that appears in the Windows Media Player user interface to identify the plug-in.</span></span> <span data-ttu-id="c7549-169">\_Mit der ID-Beschreibung können Sie den Benutzer über Ihr Plug-in informieren.</span><span class="sxs-lookup"><span data-stu-id="c7549-169">IDS\_DESCRIPTION lets you tell the user about your plug-in.</span></span> <span data-ttu-id="c7549-170">Beide Zeichen folgen werden als Parameter an die **iwmpmediapluginregistrar:: wmpregisterplayerplugin** -Funktion übergeben, die in der DllRegisterServer-Methode in Echo dll. cpp aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c7549-170">Both of these strings are passed as parameters to the **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** function, which is called in the DllRegisterServer method in Echodll.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7549-171">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c7549-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7549-172">**Ändern der Eigenschaften Seite Echo Sample**</span><span class="sxs-lookup"><span data-stu-id="c7549-172">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




