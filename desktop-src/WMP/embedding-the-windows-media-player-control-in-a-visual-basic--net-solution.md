---
title: Einbetten des Windows Media Player-Steuer Elements in eine Visual Basic .net-Lösung
description: Einbetten des Windows Media Player-Steuer Elements in eine Visual Basic .net-Lösung
ms.assetid: e6428b42-5d8b-48ef-9f7a-c90a4625b745
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player, Visual Basic .net
- Windows Media Player-Objektmodell, Visual Basic .net
- Objektmodell, Visual Basic .net
- Windows Media Player Mobile, Visual Basic .net
- Windows Media Player ActiveX-Steuerelement, Visual Basic .net
- Windows Media Player Mobile ActiveX-Steuerelement, Visual Basic .net
- ActiveX-Steuerelement, Visual Basic .net
- einbetten, Visual Basic .net-Programme
- Visual Basic .NET-Programm Einbettung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d578b456a5064f1846ead7f074f178753dbc7c97
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "104311688"
---
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a><span data-ttu-id="4ca2f-119">Einbetten des Windows Media Player-Steuer Elements in eine Visual Basic .net-Lösung</span><span class="sxs-lookup"><span data-stu-id="4ca2f-119">Embedding the Windows Media Player Control in a Visual Basic .NET Solution</span></span>

<span data-ttu-id="4ca2f-120">Um die Funktionen von Windows Media Player 9 oder höher in einer Visual Basic .NET-Anwendung zu verwenden, fügen Sie die Komponente zunächst einem Formular hinzu, wie unter [Verwenden des Windows Media Player-Steuer Elements mit beschrieben Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span><span class="sxs-lookup"><span data-stu-id="4ca2f-120">To use the functionality of Windows Media Player 9 Series or later in a Visual Basic .NET application, first add the component to a form as described in [Using the Windows Media Player Control with Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span></span>

<span data-ttu-id="4ca2f-121">In diesem Abschnitt wird beschrieben, wie Sie eine Anwendung erstellen, die Videos wieder gibt und über benutzerdefinierte Wiedergabe-und Schaltflächen verfügt.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-121">This section describes how to create an application that plays video and has custom play and stop buttons.</span></span>

## <a name="add-the-video-window"></a><span data-ttu-id="4ca2f-122">Hinzufügen des Video Fensters</span><span class="sxs-lookup"><span data-stu-id="4ca2f-122">Add the Video Window</span></span>

<span data-ttu-id="4ca2f-123">Fügen Sie das Windows Media Player-Steuerelement einem Formular hinzu.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-123">Add the Windows Media Player control to a form.</span></span> <span data-ttu-id="4ca2f-124">Ändern Sie die Größe des Steuer Elements, und platzieren Sie es an der Stelle, an der das Videofenster angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-124">Resize the control, and then place it where you want the video window to appear.</span></span>

<span data-ttu-id="4ca2f-125">Wählen Sie das Windows Media Player-Steuerelement aus, und ändern Sie dann die **uiMode** -Eigenschaft in "None".</span><span class="sxs-lookup"><span data-stu-id="4ca2f-125">Select the Windows Media Player control, then change the **uiMode** property to "none".</span></span> <span data-ttu-id="4ca2f-126">Diese Einstellung blendet die UI-Steuerelemente aus.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-126">This setting hides the UI controls.</span></span> <span data-ttu-id="4ca2f-127">Wenn der Benutzer ein Video wieder gibt, wird es im Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-127">When the user plays a video, it will appear in the window.</span></span> <span data-ttu-id="4ca2f-128">Bei reinen Audioinhalten wird eine Visualisierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-128">For audio-only content, a visualization will appear.</span></span>

## <a name="add-two-buttons-and-adjust-the-form"></a><span data-ttu-id="4ca2f-129">Zwei Schaltflächen hinzufügen und das Formular anpassen</span><span class="sxs-lookup"><span data-stu-id="4ca2f-129">Add Two Buttons and Adjust the Form</span></span>

<span data-ttu-id="4ca2f-130">Fügen Sie dem Formular nun zwei Schaltflächen hinzu.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-130">Now add two buttons to the form.</span></span> <span data-ttu-id="4ca2f-131">Wählen Sie die erste Schaltfläche aus, und ändern Sie die **Text** -Eigenschaft in "Play".</span><span class="sxs-lookup"><span data-stu-id="4ca2f-131">Select the first button and change the **Text** property to "Play".</span></span> <span data-ttu-id="4ca2f-132">Wählen Sie die zweite Schaltfläche aus, und ändern Sie die **Text** -Eigenschaft in "Ende".</span><span class="sxs-lookup"><span data-stu-id="4ca2f-132">Select the second button and change its **Text** property to "Stop".</span></span>

## <a name="add-the-play-code"></a><span data-ttu-id="4ca2f-133">Hinzufügen des Wiedergabe Codes</span><span class="sxs-lookup"><span data-stu-id="4ca2f-133">Add the Play Code</span></span>

<span data-ttu-id="4ca2f-134">Doppelklicken Sie auf die **Wiedergabe** Schaltfläche, um das Code Fenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-134">Double-click the **Play** button to reveal the Code window.</span></span> <span data-ttu-id="4ca2f-135">Der folgende Code wird angezeigt:</span><span class="sxs-lookup"><span data-stu-id="4ca2f-135">The following code is displayed:</span></span>


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



<span data-ttu-id="4ca2f-136">Fügen Sie die folgende Zeile zur Unterroutine hinzu:</span><span class="sxs-lookup"><span data-stu-id="4ca2f-136">Add this line to the subroutine:</span></span>


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



<span data-ttu-id="4ca2f-137">Im vorangehenden Codebeispiel ist "axWindowsMediaPlayer1" der Standardname des Windows Media Player-Steuer Elements und "c: \\ mediafile. wmv" ein Platzhalter für den Namen des Mediums, das Sie wiedergeben möchten.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-137">In the preceding code example, "axWindowsMediaPlayer1" is the default name of the Windows Media Player control and "c:\\mediafile.wmv" is a placeholder for the name of the media you want to play.</span></span>

<span data-ttu-id="4ca2f-138">Wenn Sie den Inhalt digitaler Medien aus dem Windows Media Player SDK der Bibliothek in Windows Media Player hinzugefügt haben, können Sie stattdessen den folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="4ca2f-138">If you have added the digital media content from the Windows Media Player SDK to the library in Windows Media Player, you can use this code instead:</span></span>


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



<span data-ttu-id="4ca2f-139">Da die **Autostart** -Eigenschaft standardmäßig auf true festgelegt ist, wird die Wiedergabe von Windows Media Player gestartet, wenn Sie die Eigenschaft **currentwiedergabe** oder **URL** festlegen.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-139">Because the **autoStart** property is true by default, Windows Media Player will start playing when you set the **currentPlaylist** or **URL** property.</span></span>

## <a name="add-the-stop-code"></a><span data-ttu-id="4ca2f-140">Hinzufügen des endcodes</span><span class="sxs-lookup"><span data-stu-id="4ca2f-140">Add the Stop Code</span></span>

<span data-ttu-id="4ca2f-141">Doppelklicken Sie auf die Schaltfläche " **Abbrechen** ", um das Code Fenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-141">Double-click the **Stop** button to reveal the Code window.</span></span> <span data-ttu-id="4ca2f-142">Der folgende Code wird angezeigt:</span><span class="sxs-lookup"><span data-stu-id="4ca2f-142">The following code is displayed:</span></span>


```VB
Private Sub Button2_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub

```



<span data-ttu-id="4ca2f-143">Fügen Sie die folgende Zeile zur Unterroutine hinzu:</span><span class="sxs-lookup"><span data-stu-id="4ca2f-143">Add this line to the subroutine:</span></span>


```VB
AxWindowsMediaPlayer1.Ctlcontrols.stop()

```



> [!Note]  
> <span data-ttu-id="4ca2f-144">Der Wrapper für verwalteten Code für das Windows Media Player-Steuerelement macht das Steuer **Element Objekt als** **ctlcontrols** verfügbar, um einen Konflikt **mit der** Steuerelement Eigenschaft zu vermeiden, die von **System. Windows. Forms. Control** geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-144">The managed-code wrapper for the Windows Media Player control exposes the **Controls** object as **Ctlcontrols** to avoid collision with the **Controls** property inherited from **System.Windows.Forms.Control**.</span></span>

 

## <a name="add-error-handling"></a><span data-ttu-id="4ca2f-145">Fehlerbehandlung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="4ca2f-145">Add Error-handling</span></span>

<span data-ttu-id="4ca2f-146">Das Windows Media Player-Steuerelement gibt keine Ausnahme aus, wenn ein Fehler auftritt, z. b. eine ungültige URL.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-146">The Windows Media Player control does not raise an exception when it encounters an error such as an invalid URL.</span></span> <span data-ttu-id="4ca2f-147">Stattdessen signalisiert das Steuerelement ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-147">Instead, the control signals an event.</span></span> <span data-ttu-id="4ca2f-148">Die Anwendung sollte vom Player gesendete Fehlerereignisse verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-148">Your application should handle error events sent by the Player.</span></span>

<span data-ttu-id="4ca2f-149">Um einen Ereignishandler zu erstellen, öffnen Sie das Code Fenster für die Formular Klasse.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-149">To create an event handler, open the code window for your form class.</span></span> <span data-ttu-id="4ca2f-150">Wählen Sie in der Dropdown Liste am oberen Rand des Fensters das Windows Media Player-Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-150">From the drop-down list at the top of the window, select the Windows Media Player control.</span></span> <span data-ttu-id="4ca2f-151">In der Dropdown Liste auf der rechten Seite wird eine Liste der Ereignisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-151">A list of events appears in the drop-down list to the right.</span></span> <span data-ttu-id="4ca2f-152">Wählen Sie in dieser Liste die Option [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md)aus.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-152">From that list, select [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md).</span></span> <span data-ttu-id="4ca2f-153">Der folgende Code wird angezeigt:</span><span class="sxs-lookup"><span data-stu-id="4ca2f-153">The following code is displayed:</span></span>


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



<span data-ttu-id="4ca2f-154">Der folgende Code kann in die Unterroutine eingefügt werden, um eine minimale Fehler Behandlungs Funktion bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-154">The following code could be inserted in the subroutine to provide minimal error-handling capability.</span></span> <span data-ttu-id="4ca2f-155">Beachten Sie, dass Informationen über den Fehler vom **\_ wmpocxevents \_ mediaerrorevent** -Argument abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-155">Note that information about the error can be retrieved from the **\_WMPOCXEvents\_MediaErrorEvent** argument.</span></span>


```VB
Try
    ' If the file is corrupt or missing, show the 
    ' hexadecimal error code and URL.
    Dim errSource As WMPLib.IWMPMedia2 = e.pMediaObject
    Dim errorItem As WMPLib.IWMPErrorItem = errSource.Error
    MessageBox.Show("Media error " + errorItem.errorCode.ToString("X") _
                    + " in " + errSource.sourceURL)
Catch ex As InvalidCastException
    ' In case pMediaObject is not an IWMPMedia item.
    MessageBox.Show("Player error.")
End Try

```



## <a name="related-topics"></a><span data-ttu-id="4ca2f-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4ca2f-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ca2f-157">**Einbetten des Windows Media Player-Steuer Elements in eine .NET Framework Lösung**</span><span class="sxs-lookup"><span data-stu-id="4ca2f-157">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




