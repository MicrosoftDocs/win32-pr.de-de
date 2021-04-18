---
title: Einbetten des Windows Media Player-Steuer Elements in eine C-Lösung
description: Einbetten des Windows Media Player-Steuer Elements in eine C \-Lösung
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player, C
- Windows Media Player-Objektmodell, C
- Objektmodell, C
- Windows Media Player Mobile, C
- Windows Media Player ActiveX-Steuerelement, C
- Windows Media Player Mobile ActiveX-Steuerelement, C
- ActiveX-Steuerelement, C
- einbetten, C-Programme
- C-Programm Einbettung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c950bed9812cea0aa6ce28995fd6998bb8417ac
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "106337190"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a><span data-ttu-id="deb33-119">Einbetten des Windows Media Player-Steuer Elements in eine c#-Lösung</span><span class="sxs-lookup"><span data-stu-id="deb33-119">Embedding the Windows Media Player Control in a C# Solution</span></span>

<span data-ttu-id="deb33-120">Um die Funktionalität von Windows Media Player in einer c#-Anwendung zu verwenden, fügen Sie die Komponente zunächst einem Formular hinzu, wie unter [Verwenden des Windows Media Player-Steuer Elements mit Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span><span class="sxs-lookup"><span data-stu-id="deb33-120">To use the functionality of Windows Media Player in a C# application, first add the component to a form as described in [Using the Windows Media Player Control with Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span></span>

<span data-ttu-id="deb33-121">In den folgenden Abschnitten wird beschrieben, wie Sie eine Anwendung erstellen, die Video abgespielt und benutzerdefinierte Wiedergabe-und Schaltflächen verwendet.</span><span class="sxs-lookup"><span data-stu-id="deb33-121">The following sections describe how to create an application that plays video and uses custom play and stop buttons.</span></span>

## <a name="add-the-video-window"></a><span data-ttu-id="deb33-122">Hinzufügen des Video Fensters</span><span class="sxs-lookup"><span data-stu-id="deb33-122">Add the Video Window</span></span>

<span data-ttu-id="deb33-123">Fügen Sie das Windows Media Player ActiveX-Steuerelement zu einem Formular hinzu.</span><span class="sxs-lookup"><span data-stu-id="deb33-123">Add the Windows Media Player ActiveX control to a form.</span></span> <span data-ttu-id="deb33-124">Ändern Sie die Größe des Steuer Elements, und platzieren Sie es an der Stelle, an der das Videofenster angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="deb33-124">Resize the control, and then place it where you want the video window to appear.</span></span>

<span data-ttu-id="deb33-125">Wählen Sie das Windows Media Player-Steuerelement aus, und ändern Sie dann die **uiMode** -Eigenschaft in "None".</span><span class="sxs-lookup"><span data-stu-id="deb33-125">Select the Windows Media Player control, then change the **uiMode** property to "none".</span></span> <span data-ttu-id="deb33-126">Diese Einstellung blendet die UI-Steuerelemente aus.</span><span class="sxs-lookup"><span data-stu-id="deb33-126">This setting hides the UI controls.</span></span> <span data-ttu-id="deb33-127">Wenn der Benutzer ein Video wieder gibt, wird es im Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="deb33-127">When the user plays a video, it will appear in the window.</span></span> <span data-ttu-id="deb33-128">Bei reinen Audioinhalten wird eine Visualisierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="deb33-128">For audio-only content, a visualization will appear.</span></span>

## <a name="add-two-buttons-and-adjust-the-form"></a><span data-ttu-id="deb33-129">Zwei Schaltflächen hinzufügen und das Formular anpassen</span><span class="sxs-lookup"><span data-stu-id="deb33-129">Add Two Buttons and Adjust the Form</span></span>

<span data-ttu-id="deb33-130">Fügen Sie dem Formular nun zwei Schaltflächen hinzu.</span><span class="sxs-lookup"><span data-stu-id="deb33-130">Now, add two buttons to the form.</span></span> <span data-ttu-id="deb33-131">Wählen Sie die erste Schaltfläche aus, und ändern Sie die **Text** -Eigenschaft in "Play".</span><span class="sxs-lookup"><span data-stu-id="deb33-131">Select the first button and change the **Text** property to "Play".</span></span> <span data-ttu-id="deb33-132">Wählen Sie die zweite Schaltfläche aus, und ändern Sie die **Text** -Eigenschaft in "Ende".</span><span class="sxs-lookup"><span data-stu-id="deb33-132">Select the second button and change its **Text** property to "Stop".</span></span>

## <a name="add-the-play-code"></a><span data-ttu-id="deb33-133">Hinzufügen des Wiedergabe Codes</span><span class="sxs-lookup"><span data-stu-id="deb33-133">Add the Play Code</span></span>

<span data-ttu-id="deb33-134">Doppelklicken Sie auf die **Wiedergabe** Schaltfläche, um das Code Fenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="deb33-134">Double-click the **Play** button to reveal the Code window.</span></span> <span data-ttu-id="deb33-135">In c# wird folgender Code angezeigt:</span><span class="sxs-lookup"><span data-stu-id="deb33-135">In C#, the following code will be displayed:</span></span>


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



<span data-ttu-id="deb33-136">Fügen Sie diese Zeile zwischen den beiden geschweiften Klammern ein:</span><span class="sxs-lookup"><span data-stu-id="deb33-136">Add this line between the two curly braces:</span></span>


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



<span data-ttu-id="deb33-137">Im vorangehenden Codebeispiel ist "axWindowsMediaPlayer1" der Standardname des Windows Media Player-Steuer Elements, und "c: \\ mediafile. wmv" ist ein Platzhalter für den Namen des Medien Elements, das Sie wiedergeben möchten.</span><span class="sxs-lookup"><span data-stu-id="deb33-137">In the preceding code example, "axWindowsMediaPlayer1" is the default name of the Windows Media Player control, and "c:\\mediafile.wmv" is a placeholder for the name of the media item you want to play.</span></span> <span data-ttu-id="deb33-138">Es kann ein beliebiger gültiger Dateipfad verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="deb33-138">Any valid file path can be used.</span></span> <span data-ttu-id="deb33-139">Das @-Symbol weist den Compiler an, keine umgekehrten Schrägstriche als Escapezeichen zu interpretieren.</span><span class="sxs-lookup"><span data-stu-id="deb33-139">The @ symbol instructs the compiler to not interpret backslashes as escape characters.</span></span>

<span data-ttu-id="deb33-140">Wenn Sie den Inhalt digitaler Medien aus dem Windows Media Player SDK der Bibliothek in Windows Media Player hinzugefügt haben, können Sie stattdessen den folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="deb33-140">If you have added the digital media content from the Windows Media Player SDK to the library in Windows Media Player, you can use this code instead:</span></span>


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



<span data-ttu-id="deb33-141">Da die **Autostart** -Eigenschaft standardmäßig auf true festgelegt ist, wird die Wiedergabe von Windows Media Player gestartet, wenn Sie die Eigenschaft **currentwiedergabe** oder **URL** festlegen.</span><span class="sxs-lookup"><span data-stu-id="deb33-141">Because the **autoStart** property is true by default, Windows Media Player will start playing when you set the **currentPlaylist** or **URL** property.</span></span>

## <a name="add-the-stop-code"></a><span data-ttu-id="deb33-142">Hinzufügen des endcodes</span><span class="sxs-lookup"><span data-stu-id="deb33-142">Add the Stop Code</span></span>

<span data-ttu-id="deb33-143">Doppelklicken Sie auf die Schaltfläche " **Abbrechen** ", um das Code Fenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="deb33-143">Double-click the **Stop** button to reveal the Code window.</span></span> <span data-ttu-id="deb33-144">In c# wird folgender Code angezeigt:</span><span class="sxs-lookup"><span data-stu-id="deb33-144">In C#, the following code will be displayed:</span></span>


```CSharp
private void button2_Click(object sender, System.EventArgs e)
{

}

```



<span data-ttu-id="deb33-145">Fügen Sie diese Zeile zwischen den beiden geschweiften Klammern ein:</span><span class="sxs-lookup"><span data-stu-id="deb33-145">Add this line between the two curly braces:</span></span>


```CSharp
axWindowsMediaPlayer1.Ctlcontrols.stop();

```



> [!Note]  
> <span data-ttu-id="deb33-146">Der Wrapper für verwalteten Code für das Windows Media Player-Steuerelement macht das Steuer **Element Objekt als** **ctlcontrols** verfügbar, um einen Konflikt **mit der** Steuerelement Eigenschaft zu vermeiden, die von **System. Windows. Forms. Control** geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="deb33-146">The managed-code wrapper for the Windows Media Player control exposes the **Controls** object as **Ctlcontrols** to avoid collision with the **Controls** property inherited from **System.Windows.Forms.Control**.</span></span>

 

## <a name="add-error-handling"></a><span data-ttu-id="deb33-147">Fehlerbehandlung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="deb33-147">Add Error-handling</span></span>

<span data-ttu-id="deb33-148">Das Windows Media Player-Steuerelement gibt keine Ausnahme aus, wenn ein Fehler auftritt, z. b. eine ungültige URL.</span><span class="sxs-lookup"><span data-stu-id="deb33-148">The Windows Media Player control does not raise an exception when it encounters an error such as an invalid URL.</span></span> <span data-ttu-id="deb33-149">Stattdessen wird ein Ereignis signalisiert.</span><span class="sxs-lookup"><span data-stu-id="deb33-149">Instead, it signals an event.</span></span> <span data-ttu-id="deb33-150">Die Anwendung sollte vom Player gesendete Fehlerereignisse verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="deb33-150">Your application should handle error events sent by the Player.</span></span>

<span data-ttu-id="deb33-151">Um einen Ereignishandler zu erstellen, öffnen Sie zunächst die Eigenschaftenfenster für das Windows Media Player-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="deb33-151">To create an event handler, first open the Properties window for the Windows Media Player control.</span></span> <span data-ttu-id="deb33-152">Doppelklicken Sie in der Liste der Ereignisse auf **MediaError**.</span><span class="sxs-lookup"><span data-stu-id="deb33-152">In the list of events, double-click **MediaError**.</span></span> <span data-ttu-id="deb33-153">Der folgende Code wird angezeigt:</span><span class="sxs-lookup"><span data-stu-id="deb33-153">The following code is displayed:</span></span>


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



<span data-ttu-id="deb33-154">Der folgende Code kann in die-Methode eingefügt werden, um eine minimale Fehler Behandlungs Funktion bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="deb33-154">The following code could be inserted in the method to provide minimal error-handling capability.</span></span> <span data-ttu-id="deb33-155">Beachten Sie, dass Informationen über den Fehler vom **\_ wmpocxevents \_ mediaerrorevent** -Argument abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="deb33-155">Note that information about the error can be retrieved from the **\_WMPOCXEvents\_MediaErrorEvent** argument.</span></span>


```CSharp
try
// If the Player encounters a corrupt or missing file, 
// show the hexadecimal error code and URL.
{
    IWMPMedia2 errSource = e.pMediaObject as IWMPMedia2;
    IWMPErrorItem errorItem = errSource.Error;
    MessageBox.Show("Error " + errorItem.errorCode.ToString("X") 
                    + " in " + errSource.sourceURL);
}
catch(InvalidCastException)
// In case pMediaObject is not an IWMPMedia item.
{
    MessageBox.Show("Error.");
} 

```



## <a name="related-topics"></a><span data-ttu-id="deb33-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="deb33-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="deb33-157">**Einbetten des Windows Media Player-Steuer Elements in eine .NET Framework Lösung**</span><span class="sxs-lookup"><span data-stu-id="deb33-157">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




