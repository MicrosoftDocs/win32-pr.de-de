---
title: Verwenden des Windows Media Player-Steuer Elements mit Microsoft Visual Studio
description: Verwenden des Windows Media Player-Steuer Elements mit Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player,. NET-Framework
- Windows Media Player-Objektmodell,. NET-Framework
- Objektmodell,. NET-Framework
- Windows Media Player Mobile,. NET-Framework
- Windows Media Player ActiveX-Steuerelement,. NET-Framework
- Windows Media Player Mobile ActiveX-Steuerelement,. NET-Framework
- ActiveX-Steuerelement,. NET-Framework
- Windows Media Player ActiveX-Steuerelement, Visual Studio
- Windows Media Player Mobile ActiveX-Steuerelement, Visual Studio
- ActiveX-Steuerelement, Visual Studio
- .NET Framework, Visual Studio-Programm Einbettung
- einbetten, Visual Studio-Programme
- Visual Studio, Programm Einbettung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b01fecd6acdfd5ccc9a7d823740ef3915bf9c6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "104037665"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a><span data-ttu-id="a36db-123">Verwenden des Windows Media Player-Steuer Elements mit Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a36db-123">Using the Windows Media Player Control with Microsoft Visual Studio</span></span>

<span data-ttu-id="a36db-124">Mithilfe der Toolbox in Visual Studio können Sie das Windows Media Player 9-oder spätere ActiveX-Steuerelement zu einer .NET Framework Anwendung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a36db-124">You can add the Windows Media Player 9 Series or later ActiveX control to a .NET Framework application through the Toolbox in Visual Studio.</span></span>

## <a name="adding-the-windows-media-player-control"></a><span data-ttu-id="a36db-125">Hinzufügen des Windows Media Player-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="a36db-125">Adding the Windows Media Player Control</span></span>

<span data-ttu-id="a36db-126">Stellen Sie vor dem Erstellen eines neuen Projekts sicher, dass die neueste Version von Windows Media Player und Windows Media Player SDK auf Ihrem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a36db-126">Before creating a new project, make sure that the latest version of Windows Media Player and the Windows Media Player SDK is installed on your computer.</span></span>

<span data-ttu-id="a36db-127">Starten Sie Visual Studio, und erstellen Sie dann ein neues Projekt.</span><span class="sxs-lookup"><span data-stu-id="a36db-127">Start Visual Studio, then create a new project.</span></span>

<span data-ttu-id="a36db-128">Öffnen Sie in Visual Studio die Toolbox.</span><span class="sxs-lookup"><span data-stu-id="a36db-128">In Visual Studio, open the Toolbox.</span></span>

<span data-ttu-id="a36db-129">Wenn Windows Media Player nicht im **Komponenten** Teil der Toolbox angezeigt wird, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="a36db-129">If Windows Media Player does not appear in the **Components** portion of the Toolbox, do the following:</span></span>

1.  <span data-ttu-id="a36db-130">Klicken Sie mit der rechten Maustaste in die Toolbox, und wählen Sie dann **Elemente auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="a36db-130">Right-click within the Toolbox, and then select **Choose Items**.</span></span> <span data-ttu-id="a36db-131">Dadurch wird das Dialogfeld **Toolbox anpassen** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a36db-131">This opens the **Customize Toolbox** dialog box.</span></span>
2.  <span data-ttu-id="a36db-132">Wählen Sie auf der Registerkarte **com-Komponenten** die Option Windows Media Player aus.</span><span class="sxs-lookup"><span data-stu-id="a36db-132">On the **COM Components** tab, select Windows Media Player.</span></span>

    <span data-ttu-id="a36db-133">Wenn Windows Media Player nicht in der Liste angezeigt wird, klicken Sie auf **Durchsuchen**, und öffnen Sie dann Wmp.dll, das sich im Ordner Windows System32 befinden sollte \\ .</span><span class="sxs-lookup"><span data-stu-id="a36db-133">If Windows Media Player does not appear in the list, click **Browse**, and then open Wmp.dll, which should be in the Windows\\System32 folder.</span></span>

3.  <span data-ttu-id="a36db-134">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a36db-134">Click **OK**.</span></span> <span data-ttu-id="a36db-135">Das Windows Media Player-Steuerelement wird auf der aktuellen Toolbox Registerkarte platziert.</span><span class="sxs-lookup"><span data-stu-id="a36db-135">The Windows Media Player control will be placed on the current Toolbox tab.</span></span>

<span data-ttu-id="a36db-136">Nun können Sie Windows Media Player in der Toolbox auswählen und einem Formular hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a36db-136">You can now select Windows Media Player in the Toolbox and add it to a form.</span></span>

<span data-ttu-id="a36db-137">Visual Studio erteilt dem Windows Media Player-Steuerelement einen Standardnamen, z. b. "axWindowsMediaPlayer1".</span><span class="sxs-lookup"><span data-stu-id="a36db-137">Visual Studio gives the Windows Media Player control a default name such as "axWindowsMediaPlayer1".</span></span> <span data-ttu-id="a36db-138">Möglicherweise möchten Sie den Namen in etwas leicht zu merken, z. b. "Player", ändern.</span><span class="sxs-lookup"><span data-stu-id="a36db-138">You may want to change the name to something more easily remembered, such as "Player".</span></span>

<span data-ttu-id="a36db-139">Durch das Hinzufügen des Windows Media Player-Steuer Elements aus der Toolbox werden auch Verweise auf zwei von Visual Studio, AxWMPLib und WMPLib erstellte Bibliotheken hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a36db-139">Adding the Windows Media Player control from the Toolbox also adds references to two libraries created by Visual Studio, AxWMPLib and WMPLib.</span></span> <span data-ttu-id="a36db-140">Sie finden Sie im Projektmappen-Explorer unter " **Verweise**".</span><span class="sxs-lookup"><span data-stu-id="a36db-140">You can find them in the Solution Explorer under **References**.</span></span>

<span data-ttu-id="a36db-141">Wenn Sie die Verwendung der Objekte im Player-Namespace vereinfachen möchten, sollten Sie den-Namespace in die using-oder Imports-Direktiven Ihrer Dateien wie folgt einschließen:</span><span class="sxs-lookup"><span data-stu-id="a36db-141">To make using the objects in the Player namespace easier, you should include the namespace in the using or imports directives of your files, as follows:</span></span>


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



<span data-ttu-id="a36db-142">Die-Direktive stellt sicher, dass Sie auf **Player** Objekte verweisen können, ohne ihre Namen vollständig zu qualifizieren.</span><span class="sxs-lookup"><span data-stu-id="a36db-142">The directive ensures that you can refer to **Player** objects without fully qualifying their names.</span></span>

> [!Note]  
> <span data-ttu-id="a36db-143">Das Windows Media Player-Steuerelement ist ein **AxWindowsMediaPlayer** -Objekt aus dem **AxWMPLib** -Namespace.</span><span class="sxs-lookup"><span data-stu-id="a36db-143">The Windows Media Player control is an **AxWindowsMediaPlayer** object from the **AxWMPLib** namespace.</span></span> <span data-ttu-id="a36db-144">Die Klasse **AxWindowsMediaPlayer** verwendet jedoch Datentypen, Schnittstellen und andere Elemente aus dem **WMPLib** -Namespace.</span><span class="sxs-lookup"><span data-stu-id="a36db-144">However, the **AxWindowsMediaPlayer** class uses data types, interfaces, and other elements from the **WMPLib** namespace.</span></span>

 

## <a name="configuring-visibility-of-the-control"></a><span data-ttu-id="a36db-145">Konfigurieren der Sichtbarkeit des Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="a36db-145">Configuring Visibility of the Control</span></span>

<span data-ttu-id="a36db-146">Wenn Sie das Windows Media Player-Steuerelement zum ersten Mal einem Formular hinzufügen, wird es angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a36db-146">When you first add the Windows Media Player control to a form, it will be visible.</span></span> <span data-ttu-id="a36db-147">Wenn Sie das sichtbare Bild des Players nicht in Ihrer Anwendung verwenden möchten, blenden Sie den Standard Player aus, indem Sie eine der folgenden Eigenschaften festlegen:</span><span class="sxs-lookup"><span data-stu-id="a36db-147">If you do not want to use the visible image of the Player in your application, hide the default Player by setting any one of the following properties:</span></span>



| <span data-ttu-id="a36db-148">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a36db-148">Property</span></span>        | <span data-ttu-id="a36db-149">Wert</span><span class="sxs-lookup"><span data-stu-id="a36db-149">Value</span></span>                                                 |
|-----------------|-------------------------------------------------------|
| <span data-ttu-id="a36db-150">**uiMode**</span><span class="sxs-lookup"><span data-stu-id="a36db-150">**uiMode**</span></span>      | <span data-ttu-id="a36db-151">"unsichtbar" (siehe [Player. uiMode](player-uimode.md).)</span><span class="sxs-lookup"><span data-stu-id="a36db-151">"invisible" (See [Player.uiMode](player-uimode.md).)</span></span> |
| <span data-ttu-id="a36db-152">**Visible**</span><span class="sxs-lookup"><span data-stu-id="a36db-152">**Visible**</span></span>     | <span data-ttu-id="a36db-153">„FALSE“</span><span class="sxs-lookup"><span data-stu-id="a36db-153">"false"</span></span>                                               |
| <span data-ttu-id="a36db-154">**Size. Width**</span><span class="sxs-lookup"><span data-stu-id="a36db-154">**Size.Width**</span></span>  | <span data-ttu-id="a36db-155">0</span><span class="sxs-lookup"><span data-stu-id="a36db-155">0</span></span>                                                     |
| <span data-ttu-id="a36db-156">**Size. Height**</span><span class="sxs-lookup"><span data-stu-id="a36db-156">**Size.Height**</span></span> | <span data-ttu-id="a36db-157">0</span><span class="sxs-lookup"><span data-stu-id="a36db-157">0</span></span>                                                     |



 

<span data-ttu-id="a36db-158">Sie können diese Eigenschaften entweder im Code oder im Fenster **Eigenschaften** festlegen, wenn das Windows-Media Player Steuerelement im Formular-Designer ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="a36db-158">You can set these properties either in code or in the **Properties** window when the Windows Media Player control is selected in the form designer.</span></span>

## <a name="object-model-compatibility-of-the-control"></a><span data-ttu-id="a36db-159">Objektmodell Kompatibilität des Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="a36db-159">Object Model Compatibility of the Control</span></span>

<span data-ttu-id="a36db-160">Das Objektmodell für das Windows Media Player-Steuerelement ist im .NET Framework identisch wie in nicht verwaltetem Code und Skript.</span><span class="sxs-lookup"><span data-stu-id="a36db-160">The object model for the Windows Media Player control is basically the same in the .NET Framework as in unmanaged code and script.</span></span> <span data-ttu-id="a36db-161">Es gibt jedoch Unterschiede in der Art, wie Elemente verfügbar gemacht werden:</span><span class="sxs-lookup"><span data-stu-id="a36db-161">However, there are differences in how elements are exposed:</span></span>

-   <span data-ttu-id="a36db-162">Die meisten Objekte werden unter dem Namen Ihrer zugrunde liegenden COM-Schnittstelle verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="a36db-162">Most objects are exposed under the name of their underlying COM interface.</span></span> <span data-ttu-id="a36db-163">Beispielsweise wird das **Wiedergabe** Listen Objekt als **iwmpwiedergabe** verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="a36db-163">For example, the **Playlist** object is exposed as **IWMPPlaylist**.</span></span>
-   <span data-ttu-id="a36db-164">Einige Schnittstellen verfügen über spätere Versionen.</span><span class="sxs-lookup"><span data-stu-id="a36db-164">Some interfaces have later versions.</span></span> <span data-ttu-id="a36db-165">Beispielsweise wurde **iwmpmedia** zusätzliche Funktionalität in **IWMPMedia2** und **IWMPMedia3** erhalten.</span><span class="sxs-lookup"><span data-stu-id="a36db-165">For example, **IWMPMedia** was given additional functionality in **IWMPMedia2** and **IWMPMedia3**.</span></span> <span data-ttu-id="a36db-166">Wenn Sie ein Objekt als **iwmpmedia** deklarieren, haben Sie in der Regel Zugriff auf die Funktionalität aller Versionen der-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a36db-166">If you declare an object as **IWMPMedia**, you usually have access to the functionality of all versions of the interface.</span></span> <span data-ttu-id="a36db-167">Der IntelliSense-® erkennt die Methoden oder Eigenschaften der Schnittstellen der neueren Version jedoch nicht, und der Visual Basic .net-Editor korrigiert nicht automatisch die Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="a36db-167">However, IntelliSense® will not recognize the methods or properties of the later-version interfaces, and the Visual Basic .NET editor will not automatically correct capitalization.</span></span> <span data-ttu-id="a36db-168">Um den vollständigen Vorteil von IntelliSense und anderen Features von Visual Studio zu erhalten, deklarieren Sie das-Objekt, indem Sie die neueste Version der-Schnittstelle verwenden, z. b. **IWMPMedia3**.</span><span class="sxs-lookup"><span data-stu-id="a36db-168">To get the full benefit of IntelliSense and other features of Visual Studio, declare the object by using the latest version of the interface, such as **IWMPMedia3**.</span></span>
-   <span data-ttu-id="a36db-169">Es sind keine indizierten Eigenschaften (c#) oder Standardeigenschaften (Visual Basic .net) vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a36db-169">There are no indexed properties (C#) or default properties (Visual Basic .NET).</span></span> <span data-ttu-id="a36db-170">Wenn Sie z **. b. ein Wiedergabelisten Element** abrufen möchten, müssen Sie in c# die **iwmwiedergabe. get \_ Item** -Accessor-Methode aufrufen oder die **iwmplayist. Item** -Eigenschaft in Visual Basic .net abrufen.</span><span class="sxs-lookup"><span data-stu-id="a36db-170">For example, to retrieve a **Playlist.item**, you must call the **IWMPlaylist.get\_Item** accessor method in C# or retrieve the **IWMPlayist.Item** property in Visual Basic .NET.</span></span>
-   <span data-ttu-id="a36db-171">Aufgrund eines Namens Konflikts zwischen der Windows Media Player **Controls** -Eigenschaft und der Steuerelement Eigenschaft **, die von** jedem Steuerelement verfügbar gemacht wird, wird die Spieler Version dieser Eigenschaft im Kontext des ActiveX-Steuer Elements als **ctlcontrols** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a36db-171">Because of a naming conflict between the Windows Media Player **Controls** property and the **Controls** property exposed by every control, the Player version of this property is called **CtlControls** in the context of the ActiveX control.</span></span> <span data-ttu-id="a36db-172">(Dies ist jedoch nicht der Fall, wenn Sie den Player Programm gesteuert anstelle von als ActiveX-Steuerelement erstellen.)</span><span class="sxs-lookup"><span data-stu-id="a36db-172">(However, this is not the case when you create the Player programmatically rather than as an ActiveX control.)</span></span>

<span data-ttu-id="a36db-173">Verwenden Sie die Objektkatalog in Visual Studio, um die richtigen API-Namen für Methoden und Objekte in den Namespaces " **AxWMPLib** " und " **WMPLib** " zu finden.</span><span class="sxs-lookup"><span data-stu-id="a36db-173">Use the Object Browser in Visual Studio to locate the correct API names for methods and objects in the **AxWMPLib** and **WMPLib** namespaces.</span></span>

## <a name="distributing-your-application"></a><span data-ttu-id="a36db-174">Verteilen Ihrer Anwendung</span><span class="sxs-lookup"><span data-stu-id="a36db-174">Distributing Your Application</span></span>

<span data-ttu-id="a36db-175">Wenn Sie Ihre Anwendung verteilen, achten Sie darauf, dass Sie AxInterop.WMPLib.dll und Interop.WMPLib.dll im Anwendungsordner installieren.</span><span class="sxs-lookup"><span data-stu-id="a36db-175">When you distribute your application, be sure to install AxInterop.WMPLib.dll and Interop.WMPLib.dll in the application folder.</span></span> <span data-ttu-id="a36db-176">Außerdem müssen Sie sicherstellen, dass die erforderliche Windows Media Player-Version auf dem Computer des Benutzers installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a36db-176">You will also need to make sure that the required Windows Media Player version is installed on the user's computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a36db-177">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a36db-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a36db-178">**Programm gesteuertes Erstellen des Windows Media Player-Steuer Elements**</span><span class="sxs-lookup"><span data-stu-id="a36db-178">**Creating the Windows Media Player Control Programmatically**</span></span>](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[<span data-ttu-id="a36db-179">**Einbetten des Windows Media Player-Steuer Elements in eine c#-Lösung**</span><span class="sxs-lookup"><span data-stu-id="a36db-179">**Embedding the Windows Media Player Control in a C# Solution**</span></span>](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[<span data-ttu-id="a36db-180">**Einbetten des Windows Media Player-Steuer Elements in eine Visual Basic .net-Lösung**</span><span class="sxs-lookup"><span data-stu-id="a36db-180">**Embedding the Windows Media Player Control in a Visual Basic .NET Solution**</span></span>](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




